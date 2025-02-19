---
title: API
excerpt: >-
  The API section in the SAPIENT GUI is dedicated to the tools, resources, and
  functionalities for developers to integrate and interact with the shipping
  system programmatically.
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
This section allows external applications to communicate with the shipping software, providing access to the features like webhooks, centralised repository of countries, currencies and time zones, and detailed API documentation. It is a crucial component for businesses looking to automate their shipping processes and enhance interoperability with other systems.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/ea95f0e26805cab264809f551589c0132329000fbd8b38cb7b2a3da167c9b5bc-clideo_editor_54ac2c759571401ebfeda5f11f3b9abd-ezgif.com-crop.gif",
        null,
        "alt text"
      ],
      "align": "center"
    }
  ]
}
[/block]


In this section, you can find information on the following components: 

- [Credentials](https://docs.intersoftsapient.net/docs/create-api-credentials): this section outlines the authentication details required to create and access the shipping API, such as API keys, tokens, or OAuth credentials. This ensures that only authorized users or applications can make requests to the API.
- [Documentation](https://api.test.intersoftsapient.net/docs/v4/api/index.html): this section provides detailed reference materials on how to use the shipping API, including endpoints, request/response formats, error handling, and example use cases. 
- **Reference Data**: this section includes the standardised read-only reference data for various attributes relevant to shipping, such as lists of countries, supported currencies, and time zone information. This data is essential for ensuring correct address formatting, currency conversions, and scheduling.

> 💡 _Tip_
> 
> _To access the reference data, in the left navigation panel, select **API** > **Reference Data**. In the dropdown menu that opens, choose any of the following options whose data that you need to view: _
> 
> - _**Countries**_
> - _**Currencies**_
> - _**Time Zones**_
> 
> [block:image]{"images":[{"image":["https://files.readme.io/d62554750f2d281c61e5434998a59109ab17c6a50e394fb984a16a02f8ad976f-Reference_data.png","","Accessing reference data"],"align":"center","border":true,"caption":"Accessing reference data"}]}[/block]

- [Webhooks](https://docs.intersoftsapient.net/docs/tracking-webhook-1): this section allows users to set up <<glossary:tracking webhook>>, tracking accounts, and manifest webhook. Webhooks enable asynchronous communication between SAPIENT and external applications.