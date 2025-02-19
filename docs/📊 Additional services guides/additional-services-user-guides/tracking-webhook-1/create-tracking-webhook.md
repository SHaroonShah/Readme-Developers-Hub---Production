---
title: Set up tracking webhook connection
excerpt: >-
  _Tracking webhook_ is a mechanism that enables real-time communication between
  shipping platforms and the systems or applications of shippers via API.
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
The primary purpose of a tracking webhook is to automate the flow of information regarding the status of <<glossary:shipments>> . Instead of relying on periodic updates (where one system constantly checks another for updates)—webhooks enable instantaneous updates.

In SAPIENT, you can set up your <<glossary:tracking webhook>> connection to enhance the overall efficiency of logistics by ensuring that all stakeholders have immediate and accurate information on their shipments.

To set up the tracking webhook connection in SAPIENT, follow the instructions as explained in the following procedure.

1. On the SAPIENT **Home** page, in the left navigation panel, select **API** > **Webhooks**. In the page that opens,  the **Tracking Webhook** tab is opened by default.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/7becde66bf84f680af845714283a1b1f8b8d4a236c27df0d5feea8e22b2fa051-Tracking_webhok_tab.png",
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
        "https://files.readme.io/d873f90ef33c4bce7de7f58c3e11cd7319daa8a1e523e7beebb40ca17319faf8-Tracking_Webhook_form.png",
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
    "0-2": "From the dropdown menu, if applicable, select the **OAuth2** authentication type.  \n  \noAuth2 is a specific protocol used for authorisation that allows third-party applications to access the user's data without exposing their credentials. It also involves exchanging credentials for an authorisation token, which is then used to authenticate in other API calls.",
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


> 🚧 _Important_
> 
> _The connectivity test fails when SAPIENT is unable to call the configured endpoint with the credentials provided by the customer. To avoid that, it is recommended for the customers to check the credentials and endpoint URL for correctness—update it, if necessary, and try again. If the credentials and URL are correct and the test still fails, then the customers need to check whether the endpoint is working correctly on their side._

<br />

4. Now, from the **Select to receive either Milestones or Full Tracking Events** dropdown, select one of the following options: 
   - **Milestones**: to receive tracking <<glossary:milestones>> only.
   - **Full Tracking Events**: to receive <<glossary:all tracking events>> throughout the shipping journey.

> 💡 _Tip_
> 
> _A list of milestones and full tracking events can be found in the [Tracking events and milestones](https://docs.intersoftsapient.net/docs/tracking-events-and-milestones) section._

4. After, turn on the **Active** toggle if you wany to activate the tracking webhook.

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
      "caption": "Activating tracking webhook"
    }
  ]
}
[/block]


> 🚧 _Important_
> 
> _The webhook only works if it is in the **Active** state. Any changes made to the webhook configuration deactivates it. Therefore, make sure the toggle is set to **Active** whenever the configuration is updated._

5. Select ![alt text](https://files.readme.io/2f9b4304c20f01f6272a39bbdeef71a6abc9242aec6337ed7c3926401517f2f1-save_changes_button_2.png) to confirm the setup completion.