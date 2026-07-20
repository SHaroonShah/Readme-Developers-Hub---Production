---
title: '# Quick Start'
excerpt: >-
  Make your first authenticated request to the Smart Building Management API and
  retrieve building details.
deprecated: false
hidden: true
metadata:
  robots: index
---
Make an authenticated request to retrieve information about a building.

## Prerequisites

Complete these steps before you send a request:

- Sign in to an active Smart Building account.
- Get your OAuth 2.0 client credentials: a `client_id` and `client_secret`.
- Install or open a REST client such as Postman, or use cURL.
- Find the Building ID you want to retrieve.

## Make your first request

To make your first authentication request, perform the steps as explained in the following procedure.

1. Get an access token.

<Accordion title="Step 1: Obtain an access token">

Send a `POST` request to `/oauth/token` with your OAuth 2.0 client credentials. The `client_credentials` grant exchanges your client credentials for a bearer token.

```json Request body
{
  "client_id": "your-client-id",
  "client_secret": "your-client-secret",
  "grant_type": "client_credentials"
}
```

A successful response includes the token to use in the next request and its lifetime in seconds.

```json Successful response
{
  "access_token": "eyJhbGciOi...",
  "expires_in": 3600,
  "token_type": "Bearer"
}
```

Copy the value of `access_token`.

</Accordion>

2. Retrieve a building.

<Accordion title="Step 2: Call the Buildings endpoint">

Replace `1023` with your Building ID and `YOUR_ACCESS_TOKEN` with the access token from step 1.

```http Request
GET /api/v1/buildings/1023
Authorization: Bearer YOUR_ACCESS_TOKEN
```

A successful response returns the building details.

```json Successful response
{
  "id": 1023,
  "name": "London Headquarters",
  "status": "Online",
  "floors": 12
}
```

</Accordion>

## Optional: Continue learning

<Accordion title="What to read next" icon="arrow-right">

- **Authentication Guide** for more detail about OAuth 2.0 authentication.
- **API Reference** to explore available endpoints.
- **Troubleshooting** if your request does not return the expected result.

</Accordion>

<br />
