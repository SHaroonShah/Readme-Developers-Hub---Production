---
title: Authentication
excerpt: >-
  Learn about OAuth2 authentication, API credentials, bearer token generation,
  and best practices for secure API access with the Intersoft SAPIENT API.
deprecated: false
hidden: false
icon: fad fa-check-double
link:
  new_tab: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  pages:
    - slug: bearer-token-generation-1
      title: Bearer Token Generation
      type: basic
---
# Best Practises

<Cards columns={2}>
  <Card title="OAuth2 Authentication" icon="shield-alt">
    Intersoft SAPIENT API uses **OAuth2** authentication - a specific protocol for authorisation that allows third-party applications to access user data without exposing credentials.
    
    OAuth2 works by obtaining limited access rights to a resource on behalf of the user.
  </Card>
  
  <Card title="API Credentials Required" href="https://docs.intersoftsapient.net/docs/create-api-credentials" icon="key">
    Before using the API and generating the <Glossary>bearer token</Glossary>, you need to create your API Credentials.
    
    These credentials are used to generate access tokens (JWT or bearer tokens).
  </Card>
</Cards>

<Accordion title="Token Generation & Management" icon="cog">

## Bearer Token Generation

To generate your bearer token, refer to the [Bearer Token Generation](https://docs.intersoftsapient.net/docs/bearer-token-generation-1) section using the **Try it** function.

## Token Security & Storage

> 💡 **Tip**
>
> The API credentials are unique for each customer. Keep these credentials safe as they cannot be viewed after being generated. If you lose these credentials you need to generate new ones.

## Token Expiration

Please be aware that the token expires after **60 minutes**. In such cases, you need to request a new access token to continue making API calls.

> 🚧 **Important**
>
> Make sure you cache the authentication token before requesting a new one.

</Accordion>

<Accordion title="Testing Environment Setup" icon="flask">

When using the **Try It** function, make sure you are in the **Production** environment and any shipping accounts that you create or use for testing have the <Glossary>account type</Glossary> set to **Sandbox**.

</Accordion>