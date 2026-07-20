---
title: Authentication
excerpt: >-
  _Authentication_ refers to the process of verifying the identity of a user or
  application that is trying to access an API. This is crucial for ensuring that
  only authorised users can interact with the API and access sensitive data or
  perform actions.
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

<Accordion title="1. Request an access token" icon="key">

Send your Client ID and Client Secret to the token endpoint.

```json Request body
{
  "client_id": "CLIENT_ID",
  "client_secret": "CLIENT_SECRET",
  "grant_type": "client_credentials"
}
```

```http
POST /oauth/token
```

The API returns an access token after it validates your credentials.

</Accordion>

<Accordion title="2. Add the token to each request" icon="lock">

Include the access token in the `Authorization` header of every API request.

```http
Authorization: Bearer eyJhbGciOi...
```

</Accordion>

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