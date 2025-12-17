---
title: Webhooks
excerpt: >-
  Webhooks are valuable tools for receiving real-time updates and data from
  various services and applications. They allow you to automate workflows,
  integrate systems, and stay up to date on important events.
deprecated: false
hidden: false
icon: fad fa-webhook
link:
  new_tab: false
metadata:
  title: ''
  description: >-
    _Webhooks_ are valuable tools for receiving real-time updates and data from
    various services and applications. They allow you to automate workflows,
    integrate systems, and stay up to date on important events.
  robots: index
---
The application sending the data sends a **POST** API call containing the data to the receiving application​. The endpoint is hosted by the application receiving the data, not the application sending the data as with a request and response-based API​.

INTERSOFT offers a comprehensive <Glossary>tracking webhook</Glossary> solution for receiving tracking events from carriers. The tracking data is sent to the customer's endpoint configured in the tracking webhook setup.

## What You Can Track

<Cards columns={3}>
  <Card title="SAPIENT Shipments" icon="shipping-fast">
    Track all <Glossary>shipments</Glossary> created on the SAPIENT platform in real-time.
  </Card>
  <Card title="Intelligent Shipper" icon="brain">
    Monitor specific shipments created on Intelligent Shipper with targeted tracking.
  </Card>
  <Card title="Royal Mail Integration" icon="mail-bulk">
    Track Royal Mail shipments created on any external shipping platform or by individuals.
  </Card>
</Cards>

---

## Getting Started

<Accordion title="Quick Setup Guide" icon="rocket">
Follow these essential steps to get your webhook tracking up and running:

1. **Create your tracking webhook** - Set up the endpoint to receive tracking data
2. **Configure your tracking account** - Establish the connection between your system and our tracking service  
3. **Set up manifest webhook** - Enable manifest-level tracking for bulk operations
4. **Understanding events** - Learn about the different tracking events and milestones
5. **Handle suspensions** - Know how to manage webhook suspension scenarios
</Accordion>

## Documentation & Resources

<Cards columns={2}>
  <Card title="Create Tracking Webhook" href="https://docs.intersoftsapient.net/docs/create-tracking-webhook" icon="plus-circle">
    Set up your webhook endpoint to start receiving tracking events from carriers.
  </Card>
  <Card title="Set Up Tracking Account" href="https://docs.intersoftsapient.net/docs/create-tracking-account" icon="user-cog">
    Configure your tracking account to connect with the webhook system.
  </Card>
  <Card title="Manifest Webhook Setup" href="https://docs.intersoftsapient.net/docs/manifest-webhook" icon="list-alt">
    Enable webhook notifications for manifest-level tracking operations.
  </Card>
  <Card title="Track Events & Milestones" href="https://docs.intersoftsapient.net/docs/tracking-events-and-milestones" icon="flag-checkered">
    Understand the different tracking events and milestone notifications you'll receive.
  </Card>
  <Card title="Handle Webhook Suspension" href="https://docs.intersoftsapient.net/docs/webhook-suspension" icon="pause-circle">
    Learn how to manage and resolve webhook suspension scenarios.
  </Card>
</Cards>