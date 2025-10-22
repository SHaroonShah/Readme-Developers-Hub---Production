---
title: Welcome to SAPIENT Developers Hub
excerpt: >-
  Welcome to Intersoft SAPIENT, a scalable carrier management platform designed
  to facilitate seamless integration with various shipping carriers, third-party
  logistics provider, and other eCommerce platforms. By leveraging APIs, SAPIENT
  enhances its adaptability and user friendliness, providing a simple, reliant
  shipping API to easily create and manage shipments, generate labels, and more.
deprecated: false
hidden: false
icon: fad fa-diagram-lean-canvas
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
  pages:
    - type: basic
      slug: integration-activation
      title: Integration Activation
---
# Introduction

APIs play a crucial role in the SAPIENT system by facilitating seamless integration with various shipping carriers, third party logistics providers, and other eCommerce platforms. This connectivity allows businesses to automate data exchange, streamline workflows, and ensure real-time updates on shipping performance.

<Image align="center" border={true} src="https://files.readme.io/82fb0cbe41a890f07d419cd0f39a19ec47336cd51e97fe6969efdb6b26a4d82d-Sapient.png" className="border" />

If you are looking to build an integration, then our API solution will help you incorporate the intelligence of Intersoft SAPIENT into your software with minimal integration effort.

The Intersoft SAPIENT Developers Hub provides both new and current users with a step-by-step guide on how to set up a <Glossary>shipping account</Glossary> , <Glossary>shipments</Glossary> , and get started as a new user. Furthermore, this section covers the vital processes on how the business clients can utilise the API to carry out shipping activities with available carriers, as well as the technical details required to build this integration.

## Getting started

This section outlines the essential information on our APIs and steps to begin utilising the SAPIENT APIs, including setup instructions, authentication processes, and key functionalities that can be accessed through the API and SAPIENT's UI. Whether you are a developer or a business user, this section offers the necessary resources to seamlessly connect and optimise your processes within the SAPIENT platform.

**Intersoft SAPIENT API** enables you to create and manage shipments, produce labels and customs documentation, generate and print collection manifests. The API also allows you to retrieve reference data such as carriers supported by the platform and the countries where shipments can be sent, maintain your own data required for these, such as adding and managing shipping accounts and <Glossary>shipping location</Glossary> details.

**Intersoft API**is a fully RESTful service implemented using JSON messaging. You, as the customer, are responsible for sending JSON messages and for maintaining the capability of receiving JSON messages in the format described in this documentation.

<Image align="center" border={false} width="500px" src="https://files.readme.io/c388f57ddfed471dccc9c49befdedf8da79a14260f9ffbbc5e7f5996226f2022-Intersoft_api_art.png" />

### Seamless integration awaits: Get started with SAPIENT

Get ready to integrate our powerful API into your existing systems. Whether you are looking to streamline shipping management, monitor performance metrics, or customise your logistics workflows, our APIs provide the flexibility and scalability you need to succeed.

Let us dive in and explore how to get started on SAPIENT

* [ ] [Create API credentials](https://docs.intersoftsapient.net/docs/create-api-credentials)
* [ ] [Activate integration](doc:integration-activation)
* [ ] [Add users](doc:add-users-to-your-organisation-to-begin-collaborating-with-your-team)
* [ ] [Add shipping location(s)](https://docs.intersoftsapient.net/docs/add-a-shipping-location)
* [ ] [Add shipping account(s)](https://docs.intersoftsapient.net/docs/add-a-shipping-account)

> 🚧 _Important_
>
> _The API requires the user to provide a[Bearer token](https://docs.intersoftsapient.net/docs/bearer-token-generation-1). To learn more about the bearer token and its generation, refer to the [Authentication](https://docs.intersoftsapient.net/docs/authentication) section._

***

## Further reading

This section provides you with the complimentary information that you might find useful for further insights into the SAPIENT system.

* [User guides](https://docs.intersoftsapient.net/docs/maintenance-guides)
* [Shipment creation and manifesting](https://docs.intersoftsapient.net/docs/shipment-creation-and-manifesting)
* [Additional services](https://docs.intersoftsapient.net/docs/additional-services-user-guides)
* [Carrier specific guides](https://docs.intersoftsapient.net/docs/carrier-specific-user-guides)
* [Glossary](https://docs.intersoftsapient.net/docs/glossary-1)
* [Archived release notes](https://docs.intersoftsapient.net/docs/archived-release-notes)

<AdvancedTable
  data={[
    {
      'code': 'APIKEY_EMPTY',
      'status': 'Unauthorized',
      'description': 'An API key was not supplied.',
      'message': 'You must pass in an API key.'
    },
    {
      'code': 'APIKEY_MISMATCH',
      'status': 'Forbidden',
      'description': "The API key doesn't match the project.",
      'message': "The API key doesn't match the project."
    },
    {
      'code': 'APIKEY_NOTFOUND',
      'status': 'Unauthorized',
      'description': "The API key couldn't be located.",
      'message': "We couldn't find your API key."
    },
    {
      'code': 'API_ACCESS_REVOKED',
      'status': 'Forbidden',
      'description': 'Your ReadMe API access has been revoked.',
      'message': 'Your ReadMe API access has been revoked.'
    },
    {
      'code': 'API_ACCESS_UNAVAILABLE',
      'status': 'Forbidden',
      'description': 'Your ReadMe project does not have access to this API. Please reach out to support@readme.io.',
      'message': 'Your ReadMe project does not have access to this API. Please reach out to support@readme.io.'
    },
    {
      'code': 'APPLY_INVALID_EMAIL',
      'status': 'Bad Request',
      'description': 'You need to provide a valid email.',
      'message': 'You need to provide a valid email.'
    },
    {
      'code': 'APPLY_INVALID_JOB',
      'status': 'Bad Request',
      'description': 'You need to provide a job.',
      'message': 'You need to provide a job.'
    },
    {
      'code': 'APPLY_INVALID_NAME',
      'status': 'Bad Request',
      'description': 'You need to provide a name.',
      'message': 'You need to provide a name.'
    },
    {
      'code': 'CATEGORY_INVALID',
      'status': 'Bad Request',
      'description': "The category couldn't be saved.",
      'message': "We couldn't save this category ({error})."
    },
    {
      'code': 'CATEGORY_NOTFOUND',
      'status': 'Not Found',
      'description': "The category couldn't be found.",
      'message': "The category with the slug '{category}' couldn't be found."
    },
    {
      'code': 'CHANGELOG_INVALID',
      'status': 'Bad Request',
      'description': "The changelog couldn't be saved.",
      'message': "We couldn't save this changelog ({error})."
    },
    {
      'code': 'CHANGELOG_NOTFOUND',
      'status': 'Not Found',
      'description': "The changelog couldn't be found.",
      'message': "The changelog with the slug '{slug}' couldn't be found."
    }
  ]}
/>
