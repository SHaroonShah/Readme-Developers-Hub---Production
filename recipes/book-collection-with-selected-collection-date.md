---
title: Book collection with selected collection date
description: Arrange for shipment collections by specifying a preferred date for pickup.
hidden: false
recipe:
  color: '#939495'
  icon: 📅
---
```csharp C#
namespace MCSS.CodeForRecipes.Recipes
{
		using MCSS.CodeForRecipes.Schema;
		using RestSharp;
		using System;
		using System.Linq;
		using System.Threading.Tasks;
		public class BookCollectionWithSelectedCollectionDate
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

						// Get the shipment ID of the created shipment
						var shipmentResponse = await client.PostAsync<ShipmentResponse>(shipmentRequest);
						var shipmentId = shipmentResponse.Packages.First().ShipmentId;

						/* 
 			 			 * Shipments must be manifested before a collection can be booked.
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
    						ShippingLocationId = shippingLocationId,
                ShippingAccountId = shippingAccountId
						});
						await client.ExecuteAsync(manifestRequest);

						// Get the collection time slots available using the shipment ID, barcode number, or tracking number, and chose a time slot
						// Each timeslot reservation ID is valid for 15 minutes from the time of the request
						var getTimeslotsRequest = new RestRequest($"/v4/collections/rm/timeslots/{shipmentId}", Method.Get);

						var timeslotsResponse = await client.GetAsync<GetCollectionsTimeslotsReponse>(getTimeslotsRequest);

						// Store the timeslot response data for later use
						var slotReservationId = timeslotsResponse.SlotReservationId;
						var slotReservationExpiryTime = timeslotsResponse.SlotReservationExpiryTime;
						var slots = timeslotsResponse.Slots;

						// Book collection with the chosen collection date
						var collectionRequest = new RestRequest($"v4/collections/rm/{shipmentId}", Method.Post);
						collectionRequest.AddJsonBody(new
						{
    						SlotReservationId = slotReservationId,
    						SlotDate = slots.First().slotDate,
						});

						var collectionResponse = await client.PostAsync<CollectionResponse>(collectionRequest);

						// Cancel Collection
						var cancelCollectionRequest = new RestRequest($"v4/collections/rm/{shipmentId}/cancel", Method.Put);
						var cancelCollectionResponse = await client.PutAsync(cancelCollectionRequest);
				}
		}
}

```

```json Response Example
{"success":true}
```

# Set up environment

<!-- csharp@1-20 -->

Set up your environment using your authentication and shipping details.

# Get an authentication token

<!-- csharp@22-43 -->

Try and get the token from the cache.  If it does not exist, then retrieve it from authentication server and cache it.

# Set up API Client

<!-- csharp@45-47 -->

Pass the token to your API client.

# Create a shipment using the Royal Mail return service (Tracked Returns 24 (T24), Enhanced TSN, or Tracked Returns 48 (T48) Enhanced TSS)

<!-- csharp@49-123 -->

First, request to get available slot dates for collection. 

After, book the collection with a selected date. 

Slots are reserved for a maximum of 15 minutes, which means there cannot be more than 15 minutes between when the available slots are received and the request for booking the collection with the selected slot is sent.

# Get the shipment ID

<!-- csharp@125-127 -->

Get the shipmentId of the created shipment.

# Manifest shipment

<!-- csharp@138-144 -->

Manifested shipment are ready to be picked up by the carrier.

# Get collection timeslots

<!-- csharp@146-150 -->

Get the collection time slots available using the shipment ID, barcode number, or tracking number, and chose a time slot.

# Save the timeslot response

<!-- csharp@152-155 -->

Save the timeslot returned in the response for later use.

# Book collection

<!-- csharp@157-165 -->

Book shipment collection with the chosen collection date.