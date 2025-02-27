---
title: Process shipment created with the action "Create"
description: Recipe Description
hidden: true
recipe:
  color: '#f9b411'
  icon: ➕
---
```csharp C#
namespace MCSS.CodeForRecipes.Recipes
{
	using MCSS.CodeForRecipes.Schema;
	using RestSharp;

	public class ProcessShipmentWithActionCreate
	{
		public async Task RunTheCodeAsync()
		{
			var authenticationUrl = "AUTHENTICATION_URL";

			var clientId = "my-client-id";
			var clientSecret = "my-client-secret";

			var apiUrl = "API_URL";

			var shippingAccountId = "my-shipping-account-id-or-alias";

			// Please note this code excludes all error handling
			// This code uses the RestSharp NuGet package
			// dotnet add package RestSharp

			// Get authentication token
			// remember to only get a new token once the old token has expired
			using var authClient = new RestClient(authenticationUrl);
			var authRequest = new RestRequest("/connect/token", Method.Post);

			authRequest.AddParameter("grant_type", "client_credentials");
			authRequest.AddParameter("client_id", clientId);
			authRequest.AddParameter("client_secret", clientSecret);

			var authResponse = await authClient.PostAsync<TokenResponse>(authRequest);
			var token = authResponse.AccessToken;

			// Setup API Client
			using var client = new RestClient(apiUrl);
			client.AddDefaultHeader("Authorization", "Bearer " + token);

			// Create a shipment with Action: "Create".
			// This creates a shipment, but does not allocate a tracking number, print the label(s), or return the label(s) in the response.
			var shipmentRequest = new RestRequest("/v4/shipments/rm", Method.Post);
			shipmentRequest.AddJsonBody(new
			{
				ShipmentInformation = new
				{
					Action = "Create",
					ContentType = "NDX",
					ServiceCode = "CRL1",
					DescriptionOfGoods = "Clothes",
					ShipmentDate = "2023-09-07",
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
						DeclaredWeight = 1.5,
						Dimensions = new
						{
							Length = 40,
							Width = 30,
							Height = 20
						}
					}
				}
			});
			var shipmentResponse = await client.PostAsync<ShipmentResponse>(shipmentRequest);

			// Store the Shipment ID for the created shipments.
			var shipmentId = shipmentResponse.Packages[0].ShipmentId;

			// Print the labels for the shipment.
			// Shipments must be updated to "Printed" status before they are manifested.
			var printLabelsRequest = new RestRequest($"/v4/shipments/printLabel/rm/{shipmentId}", Method.Get);

			var printLabelsResponse = await client.GetAsync<PrintLabelsResponse>(printLabelsRequest);

			/* 
			* Once the labels are printed the shipment will be ready for manifest.
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

<!-- csharp@ -->



# Get an authenication token

<!-- csharp@ -->



# Set up API Client

<!-- csharp@ -->



# Create shipment with the action "Create"

<!-- csharp@ -->



# Manifest shipment

<!-- csharp@ -->

