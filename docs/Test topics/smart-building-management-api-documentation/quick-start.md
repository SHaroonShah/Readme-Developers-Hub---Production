---
title: Quick Start
deprecated: false
hidden: true
icon: fad fa-alarm-exclamation
metadata:
  robots: index
---
# Quick Start

Make your first authenticated request to the Smart Building Management API and retrieve building details.

## Prerequisites

Complete these steps before you send a request:

- Sign in to an active Smart Building account.
- Get your OAuth 2.0 client credentials: a `client_id` and `client_secret`.
- Install or open a REST client such as Postman, or use cURL.
- Find the Building ID you want to retrieve.

## Create Request

To make your first authentication request, perform the steps as explained in the following procedure.

<Accordion title="1. Obtain an access token">

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

<Accordion title="2. Call the Buildings endpoint">

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

***

### See also

<Cards columns={3}>
  <Card title="Authentication" href="/docs/authentication" icon="key">
    Learn how to authenticate requests with OAuth 2.0.
  </Card>
  <Card title="API" href="/docs/api" icon="code">
    Explore the available API resources and endpoints.
  </Card>
  <Card title="Troubleshooting" href="/docs/troubleshooting" icon="wrench">
    Diagnose common integration issues.
  </Card>
</Cards>

<br />