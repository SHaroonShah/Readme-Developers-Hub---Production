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
Use OAuth 2.0 Client Credentials to obtain a Bearer token and authenticate each Smart Building API request.

## Authentication flow

<Accordion title="1. Request an access token" icon="key">

Send your Client ID and Client Secret to the token endpoint.

```http
POST /oauth/token
Content-Type: application/json
```

```json Request body
{
  "client_id": "CLIENT_ID",
  "client_secret": "CLIENT_SECRET",
  "grant_type": "client_credentials"
}
```

The API validates your credentials and returns an access token.

</Accordion>

<Accordion title="2. Add the token to each request" icon="lock">

Include the access token in the `Authorization` header of every API request.

```http
Authorization: Bearer eyJhbGciOi...
```

</Accordion>

## Token expiration

<Callout icon="clock" theme="info">
Access tokens expire after 60 minutes. Generate a new token before the current token expires.
</Callout>

## Common authentication errors

| Status | Meaning | What to do |
| --- | --- | --- |
| `401` | Unauthorized | Check your Client ID and Client Secret. |
| `403` | Forbidden | Verify that your credentials have the required API permissions. |
| `429` | Rate limited | Retry after the interval specified by the API. |

## Best practices

- Keep Client Secrets out of client-side code and source control.
- Store credentials securely.
- Rotate credentials regularly.
- Send all API requests over HTTPS.