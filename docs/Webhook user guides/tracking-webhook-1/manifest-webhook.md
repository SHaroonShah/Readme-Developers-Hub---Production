---
title: Set up manifest webhook
excerpt: >-
  A _Manifest Webhook_ is a tool used particularly in API integrations, to
  receive real-time updates or notifications whenever specific events occur in
  the system (such as shipping updates, status changes, and so on). It is
  commonly used in shipping software to keep track of shipments and their
  statuses without the need for constant polling or manual checking.
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
The manifest webhook feature has several purposes: 

* **Real-time Updates**: to receive immediate notifications about shipment activities or status changes, ensuring that the information is up-to-date.
* **Automation**: to automate the processing of shipping events, reducing manual work and enhances efficiency.
* **Integration**: to better integration with various services and APIs by providing a mechanism to push data and initiate workflows based on shipping events.
* **Error Handling**: to notify systems about issues or failures in shipment processing, allowing for timely corrections.

> 🚧 *Important*
>
> *The manifest webhook is only used if you are using the manifest async endpoint to manifest asynchronously.*

To set up the manifest webhook connection in SAPIENT, follow the instructions as explained in the following procedure.

1. On the SAPIENT **Home** page, in the left navigation panel, select **API** > **Webhooks**. In the page that opens,  select the **Manifest Webhook** tab.

<Image alt="Accessing tracking webhook" align="center" border={true} src="https://files.readme.io/2e9bf0ceab366ca1de8ba425c319222ec683bf3338c285a74952d5d9baae6c05-Manifest_webhook_tab.png">
  Accessing tracking webhook
</Image>

2. In the **WEBHOOK DETAILS** block of the **Tracking Webhook** tab, enter the necessary information as described in the following table. 

<Image align="center" className="border" width="500px" border={true} src="https://files.readme.io/f1b9e78c168e83ad35f8c5df9fccd857c57a045811daba57e58b2512f11b42f6-Manifest_webhook_details_block.png" />

<AsteridkForMandatoryElements />

<Table align={["center","left","left"]}>
  <thead>
    <tr>
      <th style={{ textAlign: "center" }}>
        Element
      </th>

      <th style={{ textAlign: "left" }}>
        Basic authentication 
      </th>

      <th style={{ textAlign: "left" }}>
        OAuth2 authentication
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td style={{ textAlign: "center" }}>
        **Authentication type\***
      </td>

      <td style={{ textAlign: "left" }}>
        From the dropdown menu, if applicable, select the **Basic** authentication type.  

        Basic is a simple authentication type built into the HTTP protocol. It involves sending the user's credentials (username and password) in an encoded format (Base64) within an HTTP header.
      </td>

      <td style={{ textAlign: "left" }}>
        From the dropdown menu, if applicable, select the **OAuth2** authentication type.  

        oAuth2 is a specific protocol used for authorisation that allows third-party applications to access the user's data without exposing their credentials.
      </td>
    </tr>

    <tr>
      <td style={{ textAlign: "center" }}>
        **Endpoint URL\***
      </td>

      <td style={{ textAlign: "left" }}>
        Enter your endpoint URL. This is the URL that we use to connect for identification purposes.
      </td>

      <td style={{ textAlign: "left" }}>
        Enter your endpoint URL. This is the URL that we use to connect for identification purposes.
      </td>
    </tr>

    <tr>
      <td style={{ textAlign: "center" }}>
        **Username\***
      </td>

      <td style={{ textAlign: "left" }}>
        Enter your username to identify and authenticate the INTERSOFT payload.
      </td>

      <td style={{ textAlign: "left" }}>
        ❌ Not applicable
      </td>
    </tr>

    <tr>
      <td style={{ textAlign: "center" }}>
        **Password\***
      </td>

      <td style={{ textAlign: "left" }}>
        Enter the password for the username you entered to identify and authenticate the INTERSOFT payload.
      </td>

      <td style={{ textAlign: "left" }}>
        ❌ Not applicable
      </td>
    </tr>

    <tr>
      <td style={{ textAlign: "center" }}>
        **Token URL\***
      </td>

      <td style={{ textAlign: "left" }}>
        ❌ Not applicable
      </td>

      <td style={{ textAlign: "left" }}>
        Enter your token URL. This is an endpoint we use to connect and get the security token.
      </td>
    </tr>

    <tr>
      <td style={{ textAlign: "center" }}>
        **Client ID\***
      </td>

      <td style={{ textAlign: "left" }}>
        ❌ Not applicable
      </td>

      <td style={{ textAlign: "left" }}>
        Enter your client ID  to identify and authenticate the INTERSOFT payload.
      </td>
    </tr>

    <tr>
      <td style={{ textAlign: "center" }}>
        **Secret\***
      </td>

      <td style={{ textAlign: "left" }}>
        ❌ Not applicable
      </td>

      <td style={{ textAlign: "left" }}>
        Enter your secret to identify and authenticate the INTERSOFT payload
      </td>
    </tr>
  </tbody>
</Table>

3. After entering all the necessary details, select ![alt text](https://files.readme.io/dcabcea774e82fdcf39f03bfcdcd2d95520a6aead65cb9bd47e7ccc32a8c085c-Test_button.png) to check if the setup is configured correctly. Once the test has been completed, and the setup configuration is correct, the webhook is activated and the following success response is displayed:

<Image alt="Success response" align="center" width="660px" border={true} src="https://files.readme.io/0994fa6-image.png">
  Success response
</Image>

Following the success response, a test tracking payload is sent to the webhook as follows:

<Image alt="tracking payload response example" align="center" border={true} src="https://files.readme.io/6b06c9d-image.png">
  tracking payload response example
</Image>

If for some reason, the connectivity test fails, the following message is displayed:

<Image alt="Failed connection response" align="center" width="660px" border={true} src="https://files.readme.io/65a4983-image.png">
  Failed connection response
</Image>

4. After, turn on the **Active** toggle if you wany to activate the manifest webhook.

<Image alt="Activating tracking webhook" align="center" width="660px" border={true} src="https://files.readme.io/a76feb6-image.png">
  Activating manifest webhook
</Image>

> 🚧 *Important*
>
> *The webhook only works if it is in the**Active** state. Any changes made to the webhook configuration deactivates it. Therefore, make sure the toggle is set to **Active** whenever the configuration is updated.*

5. Select ![alt text](https://files.readme.io/2f9b4304c20f01f6272a39bbdeef71a6abc9242aec6337ed7c3926401517f2f1-save_changes_button_2.png) to confirm the setup completion.