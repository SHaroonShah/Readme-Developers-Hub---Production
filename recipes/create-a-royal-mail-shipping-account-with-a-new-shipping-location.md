---
title: Create a shipping account with a new shipping location
description: >-
  Create a new Royal Mail shipment account from scratch and add a shipping
  location to it for future dispatches.
hidden: false
recipe:
  color: '#8d8f91'
  icon: 🏦
---
```csharp C#
namespace MCSS.CodeForRecipes.Recipes
{
		using MCSS.CodeForRecipes.Schema;
		using RestSharp;
    using System;
    using System.Threading.Tasks;

    public class AddRoyalMailShippingAccountWithNewLocation
    {
        public async Task RunTheCodeAsync()
        {
            var authenticationUrl = "AUTHENTICATION_URL";

            var clientId = "my-client-id";
            var clientSecret = "my-client-secret";

            var apiUrl = "API_URL";

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

            // Create a Royal Mail shipping account
            var shippingAccountRequest = new RestRequest("/v4/shippingAccounts/rm", Method.Post);
            shippingAccountRequest.AddJsonBody(new
            {
                AccountNumber = "9912347707",
                AccountRegisteredEmail = "my.email@example.com",
                AccountName = "AB VideoGames",
                AccountAlias = "RM-99112347707",
                AccountType = "Sandbox",
                ContactName = "John Smith",
                ContactNumber = "0123456789",
                ShippingLocations = new []
                {
                    new 
                    {
                        ShippingLocation = new
                        {
                            LocationAlias = "Main Warehouse",
                            Timezone = "Europe/London",
                            IsDefaultLocation = false,
                            Address = new
                            {
                                ContactPhone = "07123887422",
                                Line1 = "10 Sky Lane",
                                Town = "Christchurch",
                                Postcode = "TW20 0HJ",
                                County = "Surrey",
                                CountryCode = "GB"
                            }
                        },
                        PostingLocationCode = "2345654321",
                        ObaAccessCode = "123456",
                        ReceivingHubCode = "002610"
                    }
                }
               
            });
            var shippingAccountResponse = await client.PostAsync<ShippingAccountResponse>(shippingAccountRequest);

            // retrieve and store the created identifiers for future use (or use your alias's).
            var shippingAccountId = shippingAccountResponse.ShippingAccountId;
          	var shippingLocationId = shippingAccountResponse.ShippingLocationId;
          	public class ShippingAccountResponse
						{
						/// <summary>
						/// The SAPIENT Identifier assigned to the new shipping account.
						/// </summary>
						public Guid ShippingAccountId { get; set; }

						/// <summary>
						/// The SAPIENT Identifier assigned to the new shipping location.
						/// </summary>
						public Guid ShippingLocationId { get; set; }
						}

						public record TokenResponse
						{
						/// <summary>
						/// The Access Token
						/// </summary>
						[JsonPropertyName("access_token")]
           	public string AccessToken { get; init;}
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

Try and get the token from the cache.  If it does not exist, then retrieve it from authentication server and cache it.

# Set up API Client

<!-- csharp@41-43 -->

Pass the token to your API Client.

# Define account

<!-- csharp@45-56 -->

Define your Royal Mail shipping account information. This information is validated in the Royal Mail backend systems.

# Define shipping location

<!-- csharp@60-72 -->

Provide information on your shipping location.

# Define link info

<!-- csharp@75-77 -->

For Royal Mail, you must supply carrier-specific information for the shipping account and shipping location link. This includes your Online Business Account (OBA) access code and posting location code, respectively.

# Receive system ID's

<!-- csharp@84-87 -->

After successfully creating the shipping account with the new shipping location, you receive two unique system ids. Store them in your own system for future use.