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
## Overview

This guide helps you make your first successful request to the Smart Building Management API.
You'll learn how to:

- Obtain API credentials
- Authenticate
- Send your first API request
- Interpret the response

***

## Prerequisites

Before you begin, ensure you have:

- An active Smart Building account
- OAuth 2.0 client credentials
- A REST client such as Postman or cURL
- Access to your Building ID

***

## Step 1: Obtain an Access Token

Send a POST request to the authentication endpoint.
_Endpoint_
POST /oauth/token
_Request Body_
json {
  "client_id": "your-client-id",
  "client_secret": "your-client-secret",
  "grant_type": "client_credentials"
}

_Successful Response_
json {
  "access_token": "eyJhbGciOi...",
  "expires_in": 3600,
  "token_type": "Bearer"
}

***

## Step 2: Call Your First Endpoint

Retrieve information about a building.
GET /api/v1/buildings/{buildingId}
Example:
http
GET /api/v1/buildings/1023
Authorization: Bearer YOUR_ACCESS_TOKEN

***

## Example Response

json {
  "id": 1023,
  "name": "London Headquarters",
  "status": "Online",
  "floors": 12
}

***

## See also

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