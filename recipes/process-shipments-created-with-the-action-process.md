---
title: Process shipments created with the action “Process”
description: >-
  Execute actions on shipments that have been created and marked for processing
  within Sapient.
hidden: false
recipe:
  color: '#939495'
  icon: 📮
---
```csharp C#
namespace MCSS.CodeForRecipes.Recipes
{
    using RestSharp;

    public class CreateShipment
    {
        public async Task RunTheCodeAsync()
        {
            var authenticationUrl = "AUTHENTICATION_URL";

            var clientId = "my-client-id";
            var clientSecret = "my-client-secret";

            var apiUrl = "API_URL";

            var shippingAccountId = "my-shipping-account-id-or-alias";
            var shippingLocationId = "my-shipping-location-id-or-alias";

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
                    Action = "Process",
                    ContentType = "NDX",
                    ServiceCode = "CRL1",
                    DescriptionOfGoods = "Clothes",
                    ShipmentDate = "2023-08-07",
                    WeightUnitOfMeasure = "KG",
                    DimensionsUnitOfMeasure = "CM"
                },

                Shipper = new
                {
                    ShippingAccountId = shippingAccountId,
                    ShippingLocationId = shippingLocationId,
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
          /* 
			 * Once the labels are printed the shipment will be ready for manifest.
			 * Shipments must be manifested before they are handed over to the carrier.
			 * Shipments must be manifested a minimum of once a day, normally in line with the final collection of the day.
			 * They can be manifested more frequently if needed e.g. If a carrier makes several collections per day.
			 * Shipments should be manifested in bulk before they are collected.
			 * Shipments must not be manifested individually once the label is printed.
			 */

            // Manifested shipments are ready to be picked up by the carrier.
            var manifestRequest = new RestRequest($"/v4/manifests/RM", Method.Post);
            manifestRequest.AddJsonBody(new
            {
                ShippingLocationId = shippingLocationId,
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

Set-up your environment using your authentication and shipping details.

# Get an authentication token

<!-- csharp@9-40 -->

Try and get the token from the cache.  If it does not exist, then retrieve it from authentication server and cache it.

# Set up API Client

<!-- csharp@42-44 -->

Pass the token to your API Client.

# Create shipments with the action “Process”

<!-- csharp@46-86 -->

Create shipments with the action “Process”.

If applicable, this action returns a label and CN23 in the success API response.

# Manifest Shipments

<!-- csharp@89-107 -->

Manifested shipments are ready to be picked up by the carrier.