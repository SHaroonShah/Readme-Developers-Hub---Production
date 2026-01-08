---
title: Process deferred shipments
description: ' Specify which shipments you would like to defer and provide new shipment dates, and manifest them when they are ready.'
hidden: false
recipe:
  color: '#939495'
  icon: 🔂
---
```csharp C#
namespace MCSS.CodeForRecipes.Recipes
{
	using MCSS.CodeForRecipes.Schema;
	using RestSharp;

	public class DeferShipments
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
					ShipmentDate = "2023-08-15",
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

			// Defer the shipment for a maximum of 28 days. This can be repeated if necessary.
			// When you are ready to ship, simply defer the shipment again to the current date and manifest as usual.
			var deferShipmentsRequest = new RestRequest("/v4/shipments/defer", Method.Put);
			deferShipmentsRequest.AddJsonBody(new[]
			{
				new
				{
					ShipmentId = shipmentId,
					ShipmentDate = "2023-09-05"
				}
			});

			// Receive the 200 OK response - All shipments deferred successfully
			var deferShipmentsResponse = await client.ExecuteAsync(deferShipmentsRequest);

			// When ready, manifest the shipments as usual. Shipments deferred with the current date will be included.
			var manifestRequest = new RestRequest($"/v4/manifests/RM", Method.Post);
			manifestRequest.AddJsonBody(new
			{
				ShippingAccountId = shippingAccountId
			});
			await client.ExecuteAsync(manifestRequest);
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

<!-- csharp@24-40 -->

Try and get the token from the cache. If it does not exist, then retrieve it from authentication server and cache it.

# Set up API Client

<!-- csharp@43-44 -->

Pass the token to your API Client.

# Create a shipment

<!-- csharp@46-87 -->

Create a shipment with all the necessary details.

# Get shipment ID

<!-- csharp@89-90 -->

Get the shipment ID of the created shipment and save it.

# Defer shipment

<!-- csharp@92-105 -->

Defer the shipment for a maximum of 28 days. This can be repeated if necessary.

When you are ready to ship, simply defer the shipment again to the current date and manifest as usual.

# Manifest shipment

<!-- csharp@107-116 -->

When ready, manifest the shipments as usual. Shipments deferred with the current date will be included.

Manifested shipments are ready to be picked up by the carrier.