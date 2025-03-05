---
title: Release and manifest held shipment
description: >-
  Modify the current status of one or more shipments in the system, such as
  cancelling them or releasing them for delivery.
hidden: false
recipe:
  color: '#939495'
  icon: ✅
---
```csharp C#
namespace MCSS.CodeForRecipes.Recipes
{
	using MCSS.CodeForRecipes.Schema;
	using RestSharp;

	public class ReleaseAndManifestHoldShipments
	{
		public async Task RunTheCodeAsync()
		{
			var authenticationUrl = "AUTHENTICATION_URL";

			var clientId = "my-client-id";
			var clientSecret = "my-client-secret";

			var apiUrl = "API_URL";

			var shippingAccountId = "my-shipping-account-id-or-alias";
      
       var token = "";
			// Please note this code excludes all error handling
			// This code uses the Microsoft Memory Cache
			// dotnet add package Microsoft.Extensions.Caching.Memory
			// Try and get the token from the cache.  If it does not exist, then retrieve it from authentication server and cache it.
			if (!Cache.TryGetValue(AUTH_CACHE_KEY, out string cachedToken))
			{
				using var authClient = new RestClient(authenticationUrl);
				var authRequest = new RestRequest("/connect/token", Method.Post);
				authRequest.AddParameter("grant_type", "client_credentials");
				authRequest.AddParameter("client_id", clientId);
				authRequest.AddParameter("client_secret", clientSecret);
				var authResponse = await authClient.PostAsync<TokenResponse>(authRequest);
				// Store the token in the cache, calculate the cache expiry from the tokens expiry
				var tokenValidForSeconds = GetTokenExpiryInSeconds(authResponse);
				Cache.Set(AUTH_CACHE_KEY, authResponse.AccessToken, TimeSpan.FromSeconds(tokenValidForSeconds));
				token = authResponse.AccessToken;
			}
			else
			{
				token = cachedToken;
			}
      
      // Setup API Client
			using var client = new RestClient(apiUrl);
			client.AddDefaultHeader("Authorization", "Bearer " + token);

			// Create a shipment
			var shipmentRequest = new RestRequest("/v4/shipments/rm", Method.Post);
			shipmentRequest.AddJsonBody(new
			{
				ShipmentInformation = new
				{
					ContentType = "NDX",
					ServiceCode = "CRL1",
					DescriptionOfGoods = "Clothes",
					ShipmentDate = "2023-06-27",
					WeightUnitOfMeasure = "KG",
					DimensionsUnitOfMeasure = "CM"
				},

				Shipper = new
				{
					ShippingAccountId = shippingAccountId,
					Reference1 = "OrderRef56"
				},
				Destination = new
				{
					Address = new
					{
						ContactName = "John Smith",
						ContactEmail = "john.smith@example.com",
						ContactPhone = "07123456789",
						Line1 = "10 Sky Road",
						Town = "Woking",
						Postcode = "GU21 4TE",
						CountryCode = "GB"
					}
				},
				Packages = new[]
				{
					new
					{
						PackageType = "Parcel",
						DeclaredWeight = 1.5
					}
				}
			});
			var shipmentResponse = await client.PostAsync<ShipmentResponse>(shipmentRequest);

			// Store the Shipment ID for the created shipments
			var shipmentId = shipmentResponse.Packages[0].ShipmentId;

			// Update the shipment with the status "Hold"
			var updateShipmentStatusRequest = new RestRequest("/v4/shipments/status", Method.Put);
			updateShipmentStatusRequest.AddJsonBody(new
			{
				ShipmentIds = new[] { shipmentId },
				Status = "Hold",
				Reason = "Awaiting Payment"
			});

			// Receive the 200 OK response - All shipments set to "Hold" successfully
			var updateShipmentStatusResponse = await client.ExecuteAsync(updateShipmentStatusRequest);

			// Update the shipment with the status "Release"
			var releaseShipmentStatusRequest = new RestRequest("/v4/shipments/status", Method.Put);
			releaseShipmentStatusRequest.AddJsonBody(new
			{
				ShipmentIds = new[] { shipmentId },
				Status = "Release"
			});

			// Receive the 200 OK response - All shipments have been Released successfully
			var releaseShipmentStatusResponse = await client.ExecuteAsync(releaseShipmentStatusRequest);

			/* 
			* Shipments must be manifested before they are handed over to the carrier.
			* Shipments must be manifested a minimum of once a day, normally in line with the final collection of the day.
			* They can be manifested more frequently if needed e.g. If a carrier makes several collections per day.
			* Shipments should be manifested in bulk before they are collected.
			* Shipments must not be manifested individually once the label is printed.
			*/
			var manifestRequest = new RestRequest($"/v4/manifests/RM", Method.Post);
			manifestRequest.AddJsonBody(new
			{
				ShippingAccountId = shippingAccountId,
			});
			await client.PostAsync<ManifestResponse[]>(manifestRequest);
		}
	}
}
```

```json Response Example
{"success":true}
```

# Set up environment

<!-- csharp@1-17 -->

Set up your environment using your authentication and shipping details.

# Get an authentication token

<!-- csharp@19-40 -->

Try and get the token from the cache. If it does not exist, then retrieve it from authentication server and cache it.

# Set up API Client

<!-- csharp@42-44 -->

Pass the token to your API Client.

# Create a shipment

<!-- csharp@46-87 -->

Create a shipment with all the necessary details.

# Get shipment ID

<!-- csharp@89-90 -->

Get the shipment ID of the created shipment and save it.

# Update the shipment status to Hold

<!-- csharp@92-102 -->

Update the shipment status to Hold.

# Update the shipment status to Release

<!-- csharp@104-113 -->

Update the shipment by changing the status of the held shipment to Release.

# Manifest shipment

<!-- csharp@115-130 -->

When ready, manifest the shipments as usual.

Manifested shipments are ready to be picked up by the carrier.