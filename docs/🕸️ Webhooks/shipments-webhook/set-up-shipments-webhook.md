---
title: Set up Shipment Webhook connection
excerpt: >-
  Shipment Webhook is a customer-configured webhook endpoint that receives the
  results of asynchronous shipment creation requests. Instead of waiting for the
  shipment to be processed synchronously, SAPIENT immediately returns a Request
  ID and then sends the completed shipment response (including labels and
  carrier details) to the customer's webhook endpoint once processing finishes.
deprecated: false
hidden: true
icon: fad fa-webhook
metadata:
  robots: index
---
This functionality helps reduce API response-time dependency, improve scalability during high-volume periods, and provide greater flexibility for customers who wish to separate shipment creation from downstream label generation, documentation generation, and fulfilment processes

# How it works

1. The customer calls the [Create Shipment Async](https://docs.intersoftsapient.net/reference/post_v4-shipments-async-rm) endpoint.
2. SAPIENT performs initial validation and immediately returns a **Request ID**.
3. The shipment is processed in the background.
4. Once complete, SAPIENT sends the shipment result to the customer's configured webhook URL. The response can contain successful shipment details, labels, carrier information, or processing errors.

<Callout icon="🚧" theme="warn">
  ### _Important_

  _Before calling the Create shipment Async endpoint, you must configure the shipment webhook via the SAPIENT UI._
</Callout>

## How to set up shipment webhook connection

To set up the shipment webhook connection in SAPIENT, perform the steps as explained in the following procedure.


<Image src="https://files.readme.io/964792810eaa120e94a1b00aa2c61af71856be5ae5244fbf6644b00f2fc191ea-Selecting_Shipment_Webhook_tab.png" align="center" caption="Accessing shipment webhook" border={true} />


<br />

<ToggleList>
  <ToggleListItem title={<strong>1. Access tracking webhook </strong>} icon="fa-rocket">
    <br />

    On the SAPIENT **Home** page, navigate to **API** > **Webhooks** in the left panel. On the page that opens, select the **Shipment Webhook** tab.

    <Image src="https://files.readme.io/964792810eaa120e94a1b00aa2c61af71856be5ae5244fbf6644b00f2fc191ea-Selecting_Shipment_Webhook_tab.png" align="center" caption="Accessing shipment webhook" border={true} />

    ***
  </ToggleListItem>

  <br />

  <ToggleListItem title={<strong>2. Configure webhook details</strong>} icon="fa-rocket">
    <br />

    In the **WEBHOOK DETAILS** block, enter the required information based on your authentication type:

    <Image align="center" border={true} src="https://files.readme.io/9ce50f6d2ac1bc058b72b5232cf2b81a2ed76a909088ca2512d01f617884f1c4-Adding_tracking_webhook.png" width="500px" caption="Entering webhook details" />

    <br />

    <AsteridkForMandatoryElements />

    <Tabs>
      <Tab title="Basic Authentication">
        **Authentication Type**: Simple HTTP protocol authentication using encoded credentials (Base64)

        | Field              | Description                                             |
        | ------------------ | ------------------------------------------------------- |
        | **Endpoint URL**\* | Enter the endpoint URL for connection identification.         |
        | **Username**\*     | Enter the username to identify and authenticate INTERSOFT payload. |
        | **Password**\*     | Enter the password for the specified username.           |
| **Notification Email**\*     | Enter the email address where you want to receive the notifications when the webhook is suspended.           |
      </Tab>

      <Tab title="OAuth2 Authentication">
        **Authentication Type**: Authorization protocol allowing third-party access without exposing credentials

        | Field              | Description                                            |
        | ------------------ | ------------------------------------------------------ |
        | **Endpoint URL**\* | Enter the endpoint URL for connection identification.        |
        | **Token URL**\*    | Enter the endpoint to connect and retrieve security token.        |
        | **Client ID**\*    | Enter the client identifier for INTERSOFT payload authentication |
        | **Secret**\*       | Enter the secret key for INTERSOFT payload authentication        |
| **Notification Email**\*     | Enter the email address where you want to receive the notifications when the webhook is suspended.           |
      </Tab>
    </Tabs>

    ***
  </ToggleListItem>

  <br />

  <ToggleListItem title={<strong>3. Test your configuration </strong>} icon="fa-rocket">
    <br />

    After entering all the necessary details, select ![](https://files.readme.io/dcabcea774e82fdcf39f03bfcdcd2d95520a6aead65cb9bd47e7ccc32a8c085c-Test_button.png) to check if the setup is configured correctly. Once the test has been completed, and the setup configuration is correct, the webhook is activated and the following success response is displayed:

    <Image align="center" border={true} src="https://files.readme.io/0994fa6-image.png" width="660px" caption="Success response" />

    <br />

    If for some reason, the connectivity test fails, the following message is displayed:

    <Image align="center" border={true} src="https://files.readme.io/65a4983-image.png" width="660px" caption="Failed connection response" />

    <br />

    > 🚧 *Important*
    >
    > *The connectivity test fails when SAPIENT is unable to call the configured endpoint with the credentials provided by the customer. To avoid that, it is recommended for the customers to check the credentials and endpoint URL for correctness—update it, if necessary, and try again. If the credentials and URL are correct and the test still fails, then the customers need to check whether the endpoint is working correctly on their side.*

    ***
  </ToggleListItem>

  <br />

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

    <br />

    <Callout icon="💡" theme="default">
      ### *Tip*

      *Find detailed lists of milestones and tracking events in the[Tracking events and milestones](https://docs.intersoftsapient.net/docs/tracking-events-and-milestones) section.*
    </Callout>

    ***
  </ToggleListItem>

  <br />

  <ToggleListItem title={<strong>5. Activate and save </strong>} icon="fa-rocket">
    <br />

    Turn on the **Active** toggle to enable the webhook

    <Image align="center" border={true} src="https://files.readme.io/a76feb6-image.png" width="660px" caption="Activating tracking webhook" />

    <br />

    Once activated, click ![Save changes](https://files.readme.io/2f9b4304c20f01f6272a39bbdeef71a6abc9242aec6337ed7c3926401517f2f1-save_changes_button_2.png) to complete setup.

    > 🚧 *Important*
    >
    > *The webhook only works in**Active** state. Configuration changes deactivate it, so ensure the toggle is **Active** after any updates.*

    ***
  </ToggleListItem>
</ToggleList>

***

### See also

<Cards columns="2">
  <Card title="Add Tracking Account" href="https://docs.intersoftsapient.net/docs/create-tracking-account" icon="fa-solid fa-alarm-plus" target="_blank">
    Establish your tracking account for seamless integration.
  </Card>

  <Card title="Set Up Manifest Webhook" href="https://docs.intersoftsapient.net/docs/manifest-webhook" icon="fa-solid fa-webhook" target="_blank">
    Enable webhook notifications for manifest-level tracking operations.
  </Card>

  <Card title="Track Events and Milestones" href="https://docs.intersoftsapient.net/docs/tracking-events-and-milestones" icon="fa-solid fa-chart-line-up" target="_blank">
    Understand tracking events and milestone data.
  </Card>

  <Card title="Handle Webhook Suspension" href="https://docs.intersoftsapient.net/docs/webhook-suspension" icon="fa-solid fa-dial-max" target="_blank">
    Manage and resolve webhook suspension scenarios.
  </Card>
</Cards>
