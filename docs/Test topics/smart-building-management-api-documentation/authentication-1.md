---
title: Authentication
deprecated: false
hidden: true
metadata:
  robots: index
---
## Overview

The Smart Building API uses OAuth 2.0 Client Credentials authentication.
Every request must include a valid Bearer token.
------------------------------------------------

## Authentication Flow

1. Send your Client ID and Client Secret.
2. Receive an Access Token.
3. Include the token in every API request.

***

## Request

POST /oauth/token
json {
  "client_id": "CLIENT_ID",
  "client_secret": "CLIENT_SECRET",
  "grant_type": "client_credentials"
}

***

## Header Example

http
Authorization: Bearer eyJhbGciOi...

***

## Token Expiration

Access tokens expire after 60 minutes.
Generate a new token before expiration.
---------------------------------------

## Common Authentication Errors

| Status | Meaning      | Resolution                         |
| ------ | ------------ | ---------------------------------- |
| 401    | Unauthorized | Check Client ID or Secret          |
| 403    | Forbidden    | Verify API permissions             |
| 429    | Rate Limited | Retry after the specified interval |

***

## Best Practices

- Never expose Client Secrets.
- Store credentials securely.
- Rotate credentials regularly.
- Use HTTPS for all requests.

<br />
