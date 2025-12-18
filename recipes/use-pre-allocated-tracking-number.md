---
title: Use pre-allocated tracking number
description: >-
  Utilise a predefined tracking number for a shipment , ensuring seamless and
  consistent tracking across the logistics process.
hidden: false
recipe:
  color: '#a5a9ac'
  icon: 🗃️
---
```csharp C#
namespace MCSS.CodeForRecipes.Recipes
{
    using MCSS.CodeForRecipes.Schema;
    using RestSharp;

    public class PreAllocatedTrackingNumber
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

            // Get pre-allocated tracking number
            var preAllocatedTrackingNumberRequest = new RestRequest("/v4/shipments/preallocateTrackingNumber/rm", Method.Post);
            preAllocatedTrackingNumberRequest.AddJsonBody(new
            {
                ShippingAccountId = shippingAccountId,
                ShippingLocationId = shippingLocationId,
                ServiceCode = "CRL1",
                ServiceLevel = "01",
                ServiceEnhancementCode = "SIGNED",
                Destination = new
                {
                    CountryCode = "GB",
                    Postcode = "GU21 4TE"
                }
            });

            var preAllocatedTrackingNumber = await client.PostAsync<string>(preAllocatedTrackingNumberRequest);

            // Create a shipment with a pre-allocated tracking number
            var shipmentRequest = new RestRequest("/v4/shipments/rm", Method.Post);
            shipmentRequest.AddJsonBody(new
            {
                ShipmentInformation = new
                {
                    Action = "Process",
                    ContentType = "NDX",
                    ServiceCode = "CRL1",
                    DescriptionOfGoods = "Clothes"
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
                CarrierSpecifics = new
                {
                    ServiceEnhancements = new[]
                    {
                        new
                        {
                        Code = "SIGNED"
                    		},
                       
                    },
                    PreAllocatedTrackingNumber = preAllocatedTrackingNumber,
                },
                Packages = new[]
                {
                    new
                    {
                        PackageType = "Parcel",
                        PackageOccurrence = 1,
                        DeclaredWeight = 1.5,
                        DeclaredValue =  98.99,
                        Dimensions = new
                     		{
                            Length = 40,
                            Width = 30,
                            Height = 20
                        },
                    },
                }
            });
            var shipmentResponse = await client.PostAsync<ShipmentResponse>(shipmentRequest);
        }
    }
}	
```

```json Response Example
{"success":true}
```

# Set up environment

<!-- csharp@1-18 -->

Set up your environment with your authentication and shipping details.

# Get an authentication token

<!-- csharp@21-42 -->

Try and get the token from the cache.  If it does not exist, then retrieve it from authentication server and cache it.

# Set up API Client

<!-- csharp@44-46 -->

Pass the token to your API Client.

# Get pre-allocated tracking number

<!-- csharp@48-64 -->

Get a pre-allocated tracking number for the same service and destination that will be used to create the shipment.

# Create shipment with pre-allocated tracking number

<!-- csharp@66-126 -->

Create shipment with a pre-allocated tracking number.