---
title: API
excerpt: >-
  The API section in the SAPIENT GUI is dedicated to the tools, resources, and
  functionalities for developers to integrate and interact with the shipping
  system programmatically.
deprecated: false
hidden: false
icon: fad fa-gear
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
This section allows external applications to communicate with the shipping software, providing access to the features like webhooks, centralised repository of countries, currencies and time zones, and detailed API documentation. It is a crucial component for businesses looking to automate their shipping processes and enhance interoperability with other systems.


<Image src="https://files.readme.io/ea95f0e26805cab264809f551589c0132329000fbd8b38cb7b2a3da167c9b5bc-clideo_editor_54ac2c759571401ebfeda5f11f3b9abd-ezgif.com-crop.gif" align="center" />


## API components

In this section, you can find information on the following components:

<Cards columns="2">
  <Card title="Credentials" href="https://docs.intersoftsapient.net/docs/create-api-credentials" icon="fa-solid fa-key" target="_blank">
    Authentication details required to create and access the shipping API, including API keys, tokens, or OAuth credentials. Ensures only authorised users or applications can make requests to the API.
  </Card>

  <Card title="Documentation" href="https://api.test.intersoftsapient.net/docs/v4/api/index.html" icon="fa-solid fa-book-open" target="_blank">
    Detailed reference materials on how to use the shipping API, including endpoints, request/response formats, error handling, and example use cases.
  </Card>

  <Card title="Reference Data" href="## Accessing reference data" icon="fa-solid fa-database" target="_blank">
    Standardised read-only reference data for shipping attributes, including lists of countries, supported currencies, and time zone information. Essential for correct address formatting, currency conversions, and scheduling.
  </Card>

  <Card title="Webhooks" href="https://docs.intersoftsapient.net/docs/tracking-webhook-1" icon="fa-solid fa-webhook" target="_blank">
    Set up tracking webhooks, tracking accounts, and manifest webhooks. Enables asynchronous communication between SAPIENT and external applications.
  </Card>
</Cards>

***

## Accessing reference data

<Accordion title="How to Access Reference Data">
  To access the reference data, perform the following steps:

  1. In the left navigation panel, select **API** > **Reference Data**
  2. In the dropdown menu that opens, choose any of the following options:
     - **Countries**
     - **Currencies**
     - **Time Zones**


  <Image src="https://files.readme.io/d62554750f2d281c61e5434998a59109ab17c6a50e394fb984a16a02f8ad976f-Reference_data.png" alt="Accessing reference data" align="center" border={true} />

</Accordion>
