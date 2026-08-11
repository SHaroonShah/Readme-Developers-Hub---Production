---
title: Set up manifest webhook connection
excerpt: >-
  A _Webhook_ is a tool used particularly in API integrations, to receive
  real-time updates or notifications whenever specific events occur in the
  system (such as shipping updates, status changes, and so on). It is commonly
  used in shipping software to keep track of shipments and their statuses
  without the need for constant polling or manual checking.
deprecated: false
hidden: false
icon: fad fa-spider-web
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

<Callout icon="🚧" theme="warn">
  ### _Important_

  _The manifest webhook is only used if you are using the manifest async endpoint to manifest asynchronously._
</Callout>

## How to set up manifest webhook connection

To set up the manifest webhook connection in SAPIENT, follow the instructions as explained in the following procedure.

<ToggleList>
  <ToggleListItem title={<strong>1. Access manifest webhook page</strong>} icon="fa-rocket">
    <br />

    On the SAPIENT **Home** page, in the left navigation panel, select **API** > **Webhooks**. In the page that opens,  select the **Manifest Webhook** tab.

    <Image align="center" border={true} src="https://files.readme.io/2e9bf0ceab366ca1de8ba425c319222ec683bf3338c285a74952d5d9baae6c05-Manifest_webhook_tab.png" caption="Accessing tracking webhook" />

    ***
  </ToggleListItem>

  <br />

  <ToggleListItem title={<strong>2. Enter webhook details</strong>} icon="fa-rocket">
    <br />

    In the **WEBHOOK DETAILS** block of the **Tracking Webhook** tab, enter the necessary information as described in the following table.

    <Image align="center" border={true} src="https://files.readme.io/f1b9e78c168e83ad35f8c5df9fccd857c57a045811daba57e58b2512f11b42f6-Manifest_webhook_details_block.png" width="500px" caption="Entering webhook details"/>
    <br />
    <AsteridkForMandatoryElements />

    <table>
      <thead>
        <tr>
          <th>Element</th>
          <th>Basic authentication</th>
          <th>OAuth2 authentication</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td><strong>Authentication type</strong>&#42;</td>
          <td>
            <p>From the dropdown menu, if applicable, select the <strong>Basic</strong> authentication type.</p>
            <p>Basic is a simple authentication type built into the HTTP protocol. It involves sending the user's credentials (username and password) in an encoded format (Base64) within an HTTP header.</p>
          </td>
          <td>
            <p>From the dropdown menu, if applicable, select the <strong>OAuth2</strong> authentication type.</p>
            <p>OAuth2 is a specific protocol used for authorisation that allows third-party applications to access the user's data without exposing their credentials.</p>
          </td>
        </tr>
        <tr>
          <td><strong>Endpoint URL</strong>&#42;</td>
          <td>Enter your endpoint URL. This is the URL that we use to connect for identification purposes.</td>
          <td>Enter your endpoint URL. This is the URL that we use to connect for identification purposes.</td>
        </tr>
        <tr>
          <td><strong>Username</strong>&#42;</td>
          <td>Enter your username to identify and authenticate the INTERSOFT payload.</td>
          <td>❌ Not applicable</td>
        </tr>
        <tr>
          <td><strong>Password</strong>&#42;</td>
          <td>Enter the password for the username you entered to identify and authenticate the INTERSOFT payload.</td>
          <td>❌ Not applicable</td>
        </tr>
        <tr>
          <td><strong>Token URL</strong>&#42;</td>
          <td>❌ Not applicable</td>
          <td>Enter your token URL. This is an endpoint we use to connect and get the security token.</td>
        </tr>
        <tr>
          <td><strong>Client ID</strong>&#42;</td>
          <td>❌ Not applicable</td>
          <td>Enter your client ID to identify and authenticate the INTERSOFT payload.</td>
        </tr>
        <tr>
          <td><strong>Secret</strong>&#42;</td>
          <td>❌ Not applicable</td>
          <td>Enter your secret to identify and authenticate the INTERSOFT payload.</td>
        </tr>
      </tbody>
    </table>

    ***
  </ToggleListItem>

  <br />

  <ToggleListItem title={<strong>3. Test your configuration </strong>} icon="fa-rocket">
    <br />

    After entering all the necessary details, select ![](https://files.readme.io/dcabcea774e82fdcf39f03bfcdcd2d95520a6aead65cb9bd47e7ccc32a8c085c-Test_button.png) to check if the setup is configured correctly. Once the test has been completed, and the setup configuration is correct, the webhook is activated and the following success response is displayed:
    <br />
    <Image align="center" border={true} src="https://files.readme.io/0994fa6-image.png" width="660px" caption="Success response" />
    <br />

    Following the success response, a test tracking payload is sent to the webhook as follows:

    <Image align="center" border={true} src="https://files.readme.io/6b06c9d-image.png" caption="tracking payload response example" />
    <br />

    If for some reason, the connectivity test fails, the following message is displayed:

    <Image align="center" border={true} src="https://files.readme.io/65a4983-image.png" width="660px" caption="Failed connection response" />

    ***
  </ToggleListItem>

  <br />

  <ToggleListItem title={<strong>4. Activate webhook</strong>} icon="fa-rocket">
    <br />

    After, turn on the **Active** toggle if you wany to activate the manifest webhook.

    <Image align="center" border={true} src="https://files.readme.io/a76feb6-image.png" width="660px" caption="Activating tracking webhook" />
    <br />

    > 🚧 *Important*
    >
    > *The webhook only works if it is in the**Active** state. Any changes made to the webhook configuration deactivates it. Therefore, make sure the toggle is set to **Active** whenever the configuration is updated.*
  </ToggleListItem>

  <br />

  <ToggleListItem title={<strong>5. Save configuration</strong>} icon="fa-rocket">
    <br />

    Select ![](https://files.readme.io/2f9b4304c20f01f6272a39bbdeef71a6abc9242aec6337ed7c3926401517f2f1-save_changes_button_2.png) to confirm the setup completion.
  </ToggleListItem>
</ToggleList>

***

### See also

<Cards columns="2">
  <Card title="Set Up Tracking Webhook Connection" href="https://docs.intersoftsapient.net/v4.04/docs/create-tracking-webhook" icon="fa-solid fa-code-pull-request">
    Automate the instantaneous flow of information regarding the status of shipments.
  </Card>

  <Card title="Add Tracking Account" href="https://docs.intersoftsapient.net/docs/create-tracking-account" icon="fa-solid fa-alarm-plus">
    Establish your tracking account for seamless integration.
  </Card>

  <Card title="Track Events and Milestones" href="https://docs.intersoftsapient.net/docs/tracking-events-and-milestones" icon="fa-solid fa-chart-line-up">
    Understand tracking events and milestone data.
  </Card>

  <Card title="Handle Webhook Suspension" href="https://docs.intersoftsapient.net/docs/webhook-suspension" icon="fa-solid fa-dial-max">
    Manage and resolve webhook suspension scenarios.
  </Card>
</Cards>

<br />