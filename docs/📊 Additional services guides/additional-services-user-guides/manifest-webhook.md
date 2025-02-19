---
title: Set up manifest webhook
excerpt: >-
  A _Manifest Webhook_ is a tool used particularly in API integrations, to
  receive real-time updates or notifications whenever specific events occur in
  the system (such as shipping updates, status changes, and so on). It is
  commonly used in shipping software to keep track of shipments and their
  statuses without the need for constant polling or manual checking.
deprecated: false
hidden: true
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
The manifest webhook feature has several purposes: 

- **Real-time Updates**: to receive immediate notifications about shipment activities or status changes, ensuring that the information is up-to-date.
- **Automation**: to automate the processing of shipping events, reducing manual work and enhances efficiency.
- **Integration**: to better integration with various services and APIs by providing a mechanism to push data and initiate workflows based on shipping events.
- **Error Handling**: to notify systems about issues or failures in shipment processing, allowing for timely corrections.

> 🚧 _Important_
> 
> _The manifest webhook is only used if you are using the manifest async endpoint to manifest asynchronously._

To set up the manifest webhook connection in SAPIENT, follow the instructions as explained in the following procedure.

1. On the SAPIENT **Home** page, in the left navigation panel, select **API** > **Webhooks**. In the page that opens,  select the **Manifest Webhook** tab.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/2e9bf0ceab366ca1de8ba425c319222ec683bf3338c285a74952d5d9baae6c05-Manifest_webhook_tab.png",
        "",
        "Accessing tracking webhook"
      ],
      "align": "center",
      "border": true,
      "caption": "Accessing tracking webhook"
    }
  ]
}
[/block]


2. In the **WEBHOOK DETAILS** block of the **Tracking Webhook** tab, enter the necessary information as described in the following table. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/f1b9e78c168e83ad35f8c5df9fccd857c57a045811daba57e58b2512f11b42f6-Manifest_webhook_details_block.png",
        "",
        ""
      ],
      "align": "center",
      "sizing": "500px",
      "border": true
    }
  ]
}
[/block]


<AsteridkForMandatoryElements />

[block:parameters]
{
  "data": {
    "h-0": "Element",
    "h-1": "Basic authentication ",
    "h-2": "OAuth2 authentication",
    "0-0": "**Authentication type\\***",
    "0-1": "From the dropdown menu, if applicable, select the **Basic** authentication type.  \n  \nBasic is a simple authentication type built into the HTTP protocol. It involves sending the user's credentials (username and password) in an encoded format (Base64) within an HTTP header.",
    "0-2": "From the dropdown menu, if applicable, select the **OAuth2** authentication type.  \n  \noAuth2 is a specific protocol used for authorisation that allows third-party applications to access the user's data without exposing their credentials.",
    "1-0": "**Endpoint URL\\***",
    "1-1": "Enter your endpoint URL. This is the URL that we use to connect for identification purposes.",
    "1-2": "Enter your endpoint URL. This is the URL that we use to connect for identification purposes.",
    "2-0": "**Username\\***",
    "2-1": "Enter your username to identify and authenticate the INTERSOFT payload.",
    "2-2": "❌ Not applicable",
    "3-0": "**Password\\***",
    "3-1": "Enter the password for the username you entered to identify and authenticate the INTERSOFT payload.",
    "3-2": "❌ Not applicable",
    "4-0": "**Token URL\\***",
    "4-1": "❌ Not applicable",
    "4-2": "Enter your token URL. This is an endpoint we use to connect and get the security token.",
    "5-0": "**Client ID\\***",
    "5-1": "❌ Not applicable",
    "5-2": "Enter your client ID  to identify and authenticate the INTERSOFT payload.",
    "6-0": "**Secret\\***",
    "6-1": "❌ Not applicable",
    "6-2": "Enter your secret to identify and authenticate the INTERSOFT payload"
  },
  "cols": 3,
  "rows": 7,
  "align": [
    "center",
    "left",
    "left"
  ]
}
[/block]


3. After entering all the necessary details, select ![alt text](https://files.readme.io/dcabcea774e82fdcf39f03bfcdcd2d95520a6aead65cb9bd47e7ccc32a8c085c-Test_button.png) to check if the setup is configured correctly. Once the test has been completed, and the setup configuration is correct, the webhook is activated and the following success response is displayed:

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/0994fa6-image.png",
        null,
        "Success response"
      ],
      "align": "center",
      "sizing": "660px",
      "border": true,
      "caption": "Success response"
    }
  ]
}
[/block]


Following the success response, a test tracking payload is sent to the webhook as follows:

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/6b06c9d-image.png",
        null,
        "tracking payload response example"
      ],
      "align": "center",
      "border": true,
      "caption": "tracking payload response example"
    }
  ]
}
[/block]


If for some reason, the connectivity test fails, the following message is displayed:

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/65a4983-image.png",
        null,
        "Failed connection response"
      ],
      "align": "center",
      "sizing": "660px",
      "border": true,
      "caption": "Failed connection response"
    }
  ]
}
[/block]


4. After, turn on the **Active** toggle if you wany to activate the manifest webhook.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/a76feb6-image.png",
        null,
        "Activating tracking webhook"
      ],
      "align": "center",
      "sizing": "660px",
      "border": true,
      "caption": "Activating manifest webhook"
    }
  ]
}
[/block]


> 🚧 _Important_
> 
> _The webhook only works if it is in the **Active** state. Any changes made to the webhook configuration deactivates it. Therefore, make sure the toggle is set to **Active** whenever the configuration is updated._

5. Select ![alt text](https://files.readme.io/2f9b4304c20f01f6272a39bbdeef71a6abc9242aec6337ed7c3926401517f2f1-save_changes_button_2.png) to confirm the setup completion.