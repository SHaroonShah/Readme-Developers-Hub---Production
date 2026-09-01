---
title: Set up Shipment Webhook connection
excerpt: >-
  Shipment Webhook is a customer-configured webhook endpoint that receives the
  results of asynchronous shipment creation requests. Instead of waiting for the
  shipment to be processed synchronously, SAPIENT immediately returns a Request
  ID and then sends the completed shipment response (including labels and
  carrier details) to the customer's webhook endpoint once processing finishes.
deprecated: false
hidden: false
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

    <Image src="https://files.readme.io/b52b8bc9102dccbba515db81a71706b00d76d1a36fb89df2e68ce05a067b03d8-Shipment_Webhook_OAuth_screen.png" align="center" caption="Entering webhook details" border={true} />

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

  <ToggleListItem title={<strong>4. Activate and save </strong>} icon="fa-rocket">
    <br />

    Turn on the **Active** toggle to enable the webhook

    <Image align="center" border={true} src="https://files.readme.io/a76feb6-image.png" width="660px" caption="Activating shipment webhook" />

    <br />

    Once activated, click ![Save changes](https://files.readme.io/2f9b4304c20f01f6272a39bbdeef71a6abc9242aec6337ed7c3926401517f2f1-save_changes_button_2.png) to complete setup.

    > 🚧 *Important*
    >
    > *The webhook only works in **Active** state. Configuration changes deactivate it, so ensure the toggle is **Active** after any updates.*

    ***
  </ToggleListItem>
</ToggleList>

***

### See also

  <Card title="Handle Webhook Suspension" href="https://docs.intersoftsapient.net/docs/webhook-suspension" icon="fa-solid fa-dial-max" target="_blank">
    Manage and resolve webhook suspension scenarios.
  </Card>
 <Card title="Shipment Webhook" href="https://docs.intersoftsapient.net/docs/webhook-suspension" icon="fa-solid fa-webhook" target="_blank">
    Explore and learn more on how to create a async shipment request.
  </Card>

</Cards>
