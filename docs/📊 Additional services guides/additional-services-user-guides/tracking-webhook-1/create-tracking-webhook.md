---
title: Set up tracking webhook connection
excerpt: >-
  Learn how to set up tracking webhook connections in SAPIENT for real-time
  shipment status updates using Basic or OAuth2 authentication.
deprecated: false
hidden: false
icon: fad fa-code-pull-request-draft
link:
  new_tab: false
metadata:
  title: ''
  description: ''
  robots: index
---
## Overview

<Cards columns={2}>
  <Card title="What is a Tracking Webhook?" icon="webhook">
    A mechanism that enables real-time communication between shipping platforms and shipper systems via API, automating the flow of shipment status information.
  </Card>
  <Card title="Why Use Webhooks?" icon="bolt">
    Instead of periodic updates, webhooks provide instantaneous updates, enhancing logistics efficiency with immediate and accurate shipment information.
  </Card>
</Cards>

## Setup Process

Follow these steps to configure your tracking webhook connection in SAPIENT:

<Accordion title="Step 1: Access Webhook Configuration" icon="gear">

1. On the SAPIENT **Home** page, navigate to **API** > **Webhooks** in the left panel
2. The **Tracking Webhook** tab opens by default

<Image align="center" alt="Accessing tracking webhook" border={true} caption="Accessing tracking webhook" src="https://files.readme.io/7becde66bf84f680af845714283a1b1f8b8d4a236c27df0d5feea8e22b2fa051-Tracking_webhok_tab.png" />

</Accordion>

<Accordion title="Step 2: Configure Webhook Details" icon="edit">

In the **WEBHOOK DETAILS** block, enter the required information based on your authentication type:

<Image align="center" className="border" border={true} width="500px" src="https://files.readme.io/9ce50f6d2ac1bc058b72b5232cf2b81a2ed76a909088ca2512d01f617884f1c4-Adding_tracking_webhook.png" />

<AsteridkForMandatoryElements />

<Tabs>
  <Tab title="Basic Authentication">
    
**Authentication Type**: Simple HTTP protocol authentication using encoded credentials (Base64)

| Field | Description |
|-------|-------------|
| **Endpoint URL*** | Your endpoint URL for connection identification |
| **Username*** | Username to identify and authenticate INTERSOFT payload |
| **Password*** | Password for the specified username |

  </Tab>
  <Tab title="OAuth2 Authentication">
    
**Authentication Type**: Authorization protocol allowing third-party access without exposing credentials

| Field | Description |
|-------|-------------|
| **Endpoint URL*** | Your endpoint URL for connection identification |
| **Token URL*** | Endpoint to connect and retrieve security token |
| **Client ID*** | Client identifier for INTERSOFT payload authentication |
| **Secret*** | Secret key for INTERSOFT payload authentication |

  </Tab>
</Tabs>

</Accordion>

<Accordion title="Step 3: Test Your Configuration" icon="flask">

After entering all details:

1. Click ![Test button](https://files.readme.io/dcabcea774e82fdcf39f03bfcdcd2d95520a6aead65cb9bd47e7ccc32a8c085c-Test_button.png) to verify setup
2. **Success Response**: Webhook activates and test payload is sent

<Columns layout="auto">
  <Column>
    **Success Response**
    <Image align="center" alt="Success response" border={true} caption="Success response" src="https://files.readme.io/0994fa6-image.png" width="660px" />
  </Column>
  <Column>
    **Test Payload Example**
    <Image align="center" alt="tracking payload response example" border={true} caption="tracking payload response example" src="https://files.readme.io/6b06c9d-image.png" />
  </Column>
</Columns>

**Failure Response**: If connectivity test fails
<Image align="center" alt="Failed connection response" border={true} caption="Failed connection response" src="https://files.readme.io/65a4983-image.png" width="660px" />

> 🚧 **Important**
>
> Connectivity test fails when SAPIENT cannot call the configured endpoint. Check credentials and endpoint URL for correctness. If still failing with correct details, verify your endpoint is working properly.

</Accordion>

<Accordion title="Step 4: Select Tracking Event Type" icon="list">

Choose your preferred tracking event level from the dropdown:

<Cards columns={2}>
  <Card title="Milestones" icon="flag">
    Receive tracking milestones only - key status updates throughout the shipping journey.
  </Card>
  <Card title="Full Tracking Events" icon="stream">
    Receive all tracking events with optional **Received Expired Event** toggle for shipments without tracking numbers after set days.
  </Card>
</Cards>

> 💡 **Tip**
>
> Find detailed lists of milestones and tracking events in the [Tracking events and milestones](https://docs.intersoftsapient.net/docs/tracking-events-and-milestones) section.

</Accordion>

<Accordion title="Step 5: Activate and Save" icon="power-off">

1. **Activate Webhook**: Turn on the **Active** toggle to enable the webhook

<Image align="center" alt="Activating tracking webhook" border={true} caption="Activating tracking webhook" src="https://files.readme.io/a76feb6-image.png" width="660px" />

2. **Save Configuration**: Click ![Save changes](https://files.readme.io/2f9b4304c20f01f6272a39bbdeef71a6abc9242aec6337ed7c3926401517f2f1-save_changes_button_2.png) to complete setup

> 🚧 **Important**
>
> The webhook only works in **Active** state. Configuration changes deactivate it, so ensure the toggle is **Active** after any updates.

</Accordion>

## Next Steps

<Cards columns={3}>
  <Card title="Test Integration" href="#" icon="check-circle">
    Verify your webhook receives test payloads correctly
  </Card>
  <Card title="Monitor Events" href="#" icon="eye">
    Track incoming webhook notifications in your system
  </Card>
  <Card title="Troubleshoot" href="#" icon="wrench">
    Review common issues and solutions for webhook setup
  </Card>
</Cards>