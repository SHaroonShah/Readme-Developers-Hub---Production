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
  description: >-
    _Authentication_ refers to the process of verifying the identity of a user
    or application that is trying to access an API. This is crucial for ensuring
    that only authorised users can interact with the API and access sensitive
    data or perform actions.
  robots: index
next:
  pages:
    - slug: bearer-token-generation-1
      title: Bearer Token Generation
      type: basic
---
# Best practises

Intersoft SAPIENT API uses the **OAuth2** authentication, which is a specific protocol used for authorisation that allows third-party applications to access the user's data without exposing their credentials.

OAuth2 works by obtaining limited access rights to a resource on behalf of the user.  Before you can use the **API** and generate the <Glossary>bearer token</Glossary> , you need to create your [API Credentials](https://docs.intersoftsapient.net/docs/create-api-credentials).

API credentials are used to generate an access token, JWT (JSON Web Token) or bearer token. To generate the token, refer to the [Bearer Token Generation](https://docs.intersoftsapient.net/docs/bearer-token-generation-1) section using the **Try it** function.

> 💡 *Tip*
>
> *The API credentials are unique for each customer. Keep these credentials safe as they cannot be viewed after being generated. If you lose these credentials you need to generate new ones.*

Please be aware that the token expires after 60 minutes. In such cases, you need to request a new access token to continue making API calls. 

> 🚧 *Important*
>
> *Make sure you cache the authentication token before requesting a new one*.

When using the **Try It** function, make sure you are in the **Production** environment and any shipping accounts that you create or use for testing have the <Glossary>account type</Glossary> set to **Sandbox**.