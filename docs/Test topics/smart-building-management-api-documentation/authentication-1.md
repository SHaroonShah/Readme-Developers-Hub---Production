---
title: Authentication
deprecated: false
hidden: true
metadata:
  robots: index
---
Use OAuth 2.0 Client Credentials to obtain a bearer token and authenticate each Smart Building API request.

## Prepare your credentials

Obtain your **Client ID** and **Client Secret** before requesting a token.

<Callout icon="⚠️" theme="warning">
  ### _Important_

  _Keep your Client Secret private. Do not expose it in client-side applications or source control._
</Callout>

## Authenticate a request

To authenticate a request, perform the steps as explained in the following procedure.

1. Send your Client ID and Client Secret to the token endpoint.

   ```json Request body
   {
     "client_id": "CLIENT_ID",
     "client_secret": "CLIENT_SECRET",
     "grant_type": "client_credentials"
   }
   ```

   Send the body with this request:

   ```http
   POST /oauth/token
   ```

2. Receive an access token from the API.

3. Add the access token as a Bearer token in the `Authorization` header of every API request.

   ```http
   Authorization: Bearer eyJhbGciOi...
   ```

<Columns layout="auto">
  <Column>

### Token expiration

Access tokens expire after 60 minutes. Generate a new token before the current token expires.

  </Column>
  <Column>

### Use HTTPS

Send credentials and bearer tokens only over HTTPS to protect them while they are transmitted.

  </Column>
</Columns>

## Common authentication errors

| Status | Meaning      | Resolution                                          |
| ------ | ------------ | --------------------------------------------------- |
| `401`  | Unauthorized | Check your Client ID or Client Secret.              |
| `403`  | Forbidden    | Verify that your API permissions allow the request. |
| `429`  | Rate limited | Retry after the specified interval.                 |

## Optional: Credential management

<Callout icon="💡" theme="info">
  ### _Tip_

  Please bear in mind the following:&#x20;

  - _Store credentials securely._

  - _Rotate credentials regularly._

  - _Generate a new access token before it expir&#x65;_&#x73;
</Callout>

<br />
