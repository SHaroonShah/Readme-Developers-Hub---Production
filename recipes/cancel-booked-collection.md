---
title: Cancel booked collection
description: >-
  Terminate a previously scheduled collection for shipment pickup, freeing the
  allocated resources.
hidden: false
recipe:
  color: '#939495'
  icon: 🚚
---
```shell Shell
using MCSS.CodeForRecipes.Schema;
using RestSharp;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

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

// Create the shipment for which you would like to book a collection
var shipmentRequest = new RestRequest("/v4/shipments/rm", Method.Post);
shipmentRequest.AddJsonBody(new
{
    ShipmentInformation = new
    {
        Action = "Process",
        ContentType = "NDX",
        ServiceCode = "TSN",
        DescriptionOfGoods = "Clothes",
        ShipmentDate = "2024-04-18",
        WeightUnitOfMeasure = "KG",
        DimensionsUnitOfMeasure = "CM",
        CurrencyCode = "GBP"
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
            DeclaredWeight = 2,
            Dimensions = new
            {
                Height = 10,
                Width = 10,
                Length = 10
            }
        }
    },
    Items = new[]
    {
        new
        {
            SkuCode = "SKU10348",
            Description = "TestDesc",
            PackageOccurrence = "1",
            Quantity = 1,
            Weight = 1,
            Value = 10,
            CountryOfOrigin = "GB",
            HSCode = "HS1231"
        },
        new
        {
            SkuCode = "SKU11111",
            Description = "TD2",
            PackageOccurrence = "1",
            Quantity = 1,
            Weight = 1,
            Value = 10,
            CountryOfOrigin = "GB",
            HSCode = "HS3211"
        }
    }
});

//// Get the shipment ID of the created shipment
var shipmentResponse = await client.PostAsync<ShipmentResponse>(shipmentRequest);
var shipmentId = shipmentResponse.Packages.First().ShipmentId;

// Book collection with the earliest available collection time
var collectionRequest = new RestRequest($"v4/collections/rm/{shipmentId}", Method.Post);
var collectionResponse = await client.PostAsync<CollectionResponse>(collectionRequest);

// Retrieve and store the collection data for reference or future use
string collectionOrderId = collectionResponse.CollectionOrderId;
DateTime collectionDate = collectionResponse.CollectionDate;

// Cancel the booked collection
var cancelCollectionRequest = new RestRequest($"v4/collections/rm/{shipmentId}/cancel", Method.Put);

// Receive the 200 OK response - Collection cancelled successfully
var cancelCollectionResponse = await client.ExecuteAsync(cancelCollectionRequest);
```

```json Response Example
{"success":true}
```

# Set up environment

<!-- shell@1-17 -->

Set up your environment using your authentication and shipping details.

# Get an authentication token

<!-- shell@24-40 -->

Try and get the token from the cache.  If it does not exist, then retrieve it from authentication server and cache it.

# Set up API Client



Pass the token to your API Client.

# Cancel booked collection

<!-- shell@136-193 -->

Request to cancel your booked collection.