---
title: Set up tracking webhook connection
excerpt: >-
  _Tracking webhook_ is a mechanism that enables real-time communication between
  shipping platforms and the systems or applications of shippers via API.
deprecated: false
hidden: false
icon: fad fa-code-pull-request-draft
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
Instead of periodic updates, webhooks provide instantaneous updates, enhancing logistics efficiency with immediate and accurate shipment information.

In SAPIENT, you can set up your <Glossary>tracking webhook</Glossary> connection to enhance the overall efficiency of logistics by ensuring that all stakeholders have immediate and accurate information on their shipments.

## How to set up tracking webhook connection

To set up the tracking webhook connection in SAPIENT, perform the steps as explained in the following procedure.

<ToggleList>
  <ToggleListItem title={<strong>1. Access tracking webhook </strong>} icon="fa-rocket">
    

    On the SAPIENT **Home** page, navigate to **API** > **Webhooks** in the left panel. The **Tracking Webhook** tab opens by default.

    <Image align="center" border={true} src="https://files.readme.io/7becde66bf84f680af845714283a1b1f8b8d4a236c27df0d5feea8e22b2fa051-Tracking_webhok_tab.png" alt="Accessing tracking webhook" />

    ***
  </ToggleListItem>
<br />
    

  <ToggleListItem title={<strong>2. Configure webhook details</strong>} icon="fa-rocket">
    

    In the **WEBHOOK DETAILS** block, enter the required information based on your authentication type:

    <Image align="center" src="https://files.readme.io/173014ddedd58a4c42eed5d291d03fa7455d10b511675e72f8e7434b6333186d-image.png" />
<br />
    

    <AsteridkForMandatoryElements />

    <Tabs>
      <Tab title="Basic Authentication">
        **Authentication Type**: Simple HTTP protocol authentication using encoded credentials (Base64)

        | Field              | Description                                             |
        | ------------------ | ------------------------------------------------------- |
        | **Endpoint URL**\* | Enter your endpoint URL for connection identification         |
        | **Username**\*     | Enter the username to identify and authenticate INTERSOFT payload |
        | **Password**\*     | Enter the password for the specified username                     |
| **Notification Email**\*     | Enter the email address to receive the webhook suspension notifications.                       |
      </Tab>

      <Tab title="OAuth2 Authentication">
        **Authentication Type**: Authorization protocol allowing third-party access without exposing credentials

        | Field              | Description                                            |
        | ------------------ | ------------------------------------------------------ |
        | **Endpoint URL**\* | Enter your endpoint URL for connection identification        |
        | **Token URL**\*    | Enter the endpoint url to connect and retrieve security token        |
        | **Client ID**\*    | Enter the client identifier for INTERSOFT payload authentication |
        | **Secret**\*       | Enter the secret key for INTERSOFT payload authentication        |
| **Notification Email**\*     | Enter the email address to receive the webhook suspension notifications. 
      </Tab>
    </Tabs>

    ***
  </ToggleListItem>
<br />
    

  <ToggleListItem title={<strong>3. Test your configuration </strong>} icon="fa-rocket">
    

    After entering all the necessary details, select ![](https://files.readme.io/dcabcea774e82fdcf39f03bfcdcd2d95520a6aead65cb9bd47e7ccc32a8c085c-Test_button.png) to check if the setup is configured correctly. Once the test has been completed, and the setup configuration is correct, the webhook is activated and the following success response is displayed:

    <Image align="center" border={true} src="https://files.readme.io/0994fa6-image.png" width="660px" alt="Success response" />
<br />
    

    Following the success response, a test tracking payload is sent to the webhook as follows:

    <Image align="center" border={true} src="https://files.readme.io/6b06c9d-image.png" alt="tracking payload response example" />
<br />
    

    If for some reason, the connectivity test fails, the following message is displayed:

    <Image align="center" border={true} src="https://files.readme.io/65a4983-image.png" width="660px" alt="Failed connection response" />
<br />
    

    > 🚧 *Important*
    >
    > *The connectivity test fails when SAPIENT is unable to call the configured endpoint with the credentials provided by the customer. To avoid that, it is recommended for the customers to check the credentials and endpoint URL for correctness—update it, if necessary, and try again. If the credentials and URL are correct and the test still fails, then the customers need to check whether the endpoint is working correctly on their side.*

    ***
  </ToggleListItem>

    

  <ToggleListItem title={<strong>4. Select tracking event type </strong>} icon="fa-rocket">
    <br />

    Choose your preferred tracking event level from the dropdown:

    <Cards columns={2}>
      <Card title="Milestones" icon="flag">
        Receive tracking milestones only, allowing key status updates throughout the shipping journey.
      </Card>

      <Card title="Full Tracking Events" icon="stream">
        Receive all tracking events with optional **Received Expired Event** toggle for shipments without tracking numbers after set days.
      </Card>
    </Cards>

    

    <Callout icon="💡" theme="default">
      ### *Tip*

      *Find detailed lists of milestones and tracking events in the[Tracking events and milestones](https://docs.intersoftsapient.net/docs/tracking-events-and-milestones) section.*
    </Callout>

    ***
  </ToggleListItem>

    

  <ToggleListItem title={<strong>5. Activate and save </strong>} icon="fa-rocket">
    

    Turn on the **Active** toggle to enable the webhook

    <Image align="center" border={true} src="https://files.readme.io/a76feb6-image.png" width="660px" alt="Activating tracking webhook" />

    

    Once activated, click ![Save changes](https://files.readme.io/2f9b4304c20f01f6272a39bbdeef71a6abc9242aec6337ed7c3926401517f2f1-save_changes_button_2.png) to complete setup.

    > 🚧 *Important*
    >
    > *The webhook only works in**Active** state. Configuration changes deactivate it, so ensure the toggle is **Active** after any updates.*

    ***
  </ToggleListItem>
</ToggleList>

***

### See also

<Cards>
  <Card title="Add Tracking Account" href="https://docs.intersoftsapient.net/docs/create-tracking-account" icon="fa-solid fa-alarm-plus">
    Establish your tracking account for seamless integration.
  </Card>

  <Card title="Set Up Manifest Webhook" href="https://docs.intersoftsapient.net/docs/manifest-webhook" icon="fa-solid fa-webhook">
    Enable webhook notifications for manifest-level tracking operations.
  </Card>

  <Card title="Track Events and Milestones" href="https://docs.intersoftsapient.net/docs/tracking-events-and-milestones" icon="fa-solid fa-chart-line-up">
    Understand tracking events and milestone data.
  </Card>

  <Card title="Handle Webhook Suspension" href="https://docs.intersoftsapient.net/docs/webhook-suspension" icon="fa-solid fa-dial-max">
    Manage and resolve webhook suspension scenarios.
  </Card>
</Cards>

<br />

<br />
