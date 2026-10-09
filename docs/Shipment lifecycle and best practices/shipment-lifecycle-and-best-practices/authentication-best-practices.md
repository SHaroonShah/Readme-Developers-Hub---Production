---
title: Authentication best practices
excerpt: >-
  Authentication is the first step in communicating securely with the SAPIENT
  APIs. Before making API requests, you must obtain a bearer token using your
  API credentials and include the token in the Authorization header of
  subsequent requests.
deprecated: false
hidden: false
icon: fad fa-truck-fast
metadata:
  robots: index
---
To ensure optimal performance and reduce unnecessary authentication traffic, you should store and reuse valid bearer tokens rather than generating a new token before every API request.&#x20;

Several internal integration designs and authentication implementations used within SAPIENT follow this approach by storing access tokens and refreshing them only when they expire or become invalid.

## Authentication flow

```mermaid
flowchart TD

    A[Generate Bearer Token] --> B[Store Token Securely]

    B --> C{Token Still Valid?}

    C -->|Yes| D[Reuse Existing Token]
    C -->|No| E[Generate New Token]

    D --> F[Call SAPIENT APIs]
    E --> G[Store New Token]
    G --> F

    F --> H{Authentication Failed?}

    H -->|No| I[Continue Processing]
    H -->|Yes| E
```
