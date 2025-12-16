---
title: Containerise shipments
description: >-
  Group multiple individual shipments into a single container for more efficient
  shipping management.
hidden: false
recipe:
  color: '#a5a9ac'
  icon: 📥
---
```csharp C#
namespace MCSS.CodeForRecipes.Recipes
{
	using MCSS.CodeForRecipes.Schema;
	using RestSharp;

    public class ContaineriseShipments
    {
        public async Task RunTheCodeAsync()
        {

						var authenticationUrl = "AUTHENTICATION_URL";
						var clientId = "my-client-id";
						var clientSecret = "my-client-secret";

						var apiUrl = "API_URL";

						var shippingAccountId = "my-shipping-account-id-or-alias";
						var shippingLocationId = "my-shipping-location-id-or-alias";
						var containerId = "my-container-id";

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
            var shipmentId = shipmentResponse.Packages.First().ShipmentId;


						// Create the container
						var containerRequest = new RestRequest("/v4/containers", Method.Post);
						containerRequest.AddJsonBody(new
						{
								CarrierCode = "RM",
								ShippingLocationId = shippingLocationId,
								ContainerId = containerId
						});
						await client.ExecuteAsync(containerRequest);

						// Add Shipment to the new container
						var addShipmentToContainerRequest = new RestRequest($"/v4/containers/{containerId}", Method.Put);
						addShipmentToContainerRequest.AddJsonBody(new
						{
								ShipmentIds = new string[] { shipmentId },
								Mode = "Add"
						});
						await client.ExecuteAsync(addShipmentToContainerRequest);

						// Manifest Container (this will also remove the container once the container is manifested successfully)
						var manifestRequest = new RestRequest($"/v4/manifests/RM", Method.Post);
						manifestRequest.AddJsonBody(new
						{
								ContainerId = containerId,
								ShippingLocationId = shippingLocationId
						});
          await client.ExecuteAsync(manifestRequest);
        }
    }
}

							
```

```json Response Example
{"success":true}
```

# Environment set-up

<!-- csharp@11-19 -->

Set up your environment using your authentication and shipping details.

# Get an authentication token

<!-- csharp@21-42 -->

Try and get the token from the cache.  If it does not exist, then retrieve it from authentication server and cache it.

# Set up API Client

<!-- csharp@45-47 -->

Pass the token to your API Client.

# Create a Shipment

<!-- csharp@50-89 -->

In this example, we will create a simple shipment.  

Shipments can be created before or after creating the container. You can add the shipments =to the container at any point before the container is manifested.

# Create a Container

<!-- csharp@92-100 -->

Create the container and allocate a unique container ID to it.

The "containerId" is your reference to the container and is used to add shipments to the container.

# Add shipments to the container

<!-- csharp@102-109 -->

Add the previously created shipment to your container. You can repeat this process until you want to close the container and manifest it.

# Manifest container

<!-- csharp@111-118 -->

At this stage, the system manifests the container and closes it.