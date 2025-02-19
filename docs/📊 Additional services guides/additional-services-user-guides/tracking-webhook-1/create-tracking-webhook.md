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
The primary purpose of a tracking webhook is to automate the flow of information regarding the status of <Glossary>shipments</Glossary> . Instead of relying on periodic updates (where one system constantly checks another for updates)—webhooks enable instantaneous updates.

In SAPIENT, you can set up your <Glossary>tracking webhook</Glossary> connection to enhance the overall efficiency of logistics by ensuring that all stakeholders have immediate and accurate information on their shipments.

To set up the tracking webhook connection in SAPIENT, follow the instructions as explained in the following procedure.

1. On the SAPIENT **Home** page, in the left navigation panel, select **API** > **Webhooks**. In the page that opens,  the **Tracking Webhook** tab is opened by default.

<Image alt="Accessing tracking webhook" align="center" border={true} src="https://files.readme.io/7becde66bf84f680af845714283a1b1f8b8d4a236c27df0d5feea8e22b2fa051-Tracking_webhok_tab.png">
  Accessing tracking webhook
</Image>

2. In the **WEBHOOK DETAILS** block of the **Tracking Webhook** tab, enter the necessary information as described in the following table. 

<Image align="center" className="border" width="500px" border={true} src="https://files.readme.io/d873f90ef33c4bce7de7f58c3e11cd7319daa8a1e523e7beebb40ca17319faf8-Tracking_Webhook_form.png" />

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

        oAuth2 is a specific protocol used for authorisation that allows third-party applications to access the user's data without exposing their credentials. It also involves exchanging credentials for an authorisation token, which is then used to authenticate in other API calls.
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

> 🚧 *Important*
>
> *The connectivity test fails when SAPIENT is unable to call the configured endpoint with the credentials provided by the customer. To avoid that, it is recommended for the customers to check the credentials and endpoint URL for correctness—update it, if necessary, and try again. If the credentials and URL are correct and the test still fails, then the customers need to check whether the endpoint is working correctly on their side.*

<br />

4. Now, from the **Select to receive either Milestones or Full Tracking Events** dropdown, select one of the following options: 
   * **Milestones**: to receive tracking <Glossary>milestones</Glossary> only.
   * **Full Tracking Events**: to receive <Glossary>all tracking events</Glossary> throughout the shipping journey.

> 💡 *Tip*
>
> *A list of milestones and full tracking events can be found in the[Tracking events and milestones](https://docs.intersoftsapient.net/docs/tracking-events-and-milestones) section.*

4. After, turn on the **Active** toggle if you wany to activate the tracking webhook.

<Image alt="Activating tracking webhook" align="center" width="660px" border={true} src="https://files.readme.io/a76feb6-image.png">
  Activating tracking webhook
</Image>

> 🚧 *Important*
>
> *The webhook only works if it is in the**Active** state. Any changes made to the webhook configuration deactivates it. Therefore, make sure the toggle is set to **Active** whenever the configuration is updated.*

5. Select ![alt text](https://files.readme.io/2f9b4304c20f01f6272a39bbdeef71a6abc9242aec6337ed7c3926401517f2f1-save_changes_button_2.png) to confirm the setup completion.
