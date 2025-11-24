---
title: Getting Started with SAPIENT API
excerpt: >-
  Get started with SAPIENT API integration. Learn how to set up credentials,
  activate integrations, and configure shipping accounts for seamless logistics
  automation.
deprecated: false
hidden: false
icon: fad fa-diagram-lean-canvas
link:
  new_tab: false
metadata:
  robots: index
---
If you are looking to build an integration, then our API solution will help you incorporate the intelligence of Intersoft SAPIENT into your software with minimal integration effort.

<Image align="center" border={false} width="100px" src="https://files.readme.io/b39ab1a7142550c3018a81fedda67069e7e5a83c72b48e62e0d58010f4ef19f5-Add_location_icon.png" />

<Accordion title="What is SAPIENT API?" icon="code">
  **Intersoft SAPIENT API** is a fullt RESTful service that enables you to create and manage shipments, produce labels and customs documentation, generate and print collection manifests. The API also allows you to retrieve reference data such as carriers supported by the platform and the countries where shipments can be sent, maintain your own data required for these, such as adding and managing shipping accounts and <Glossary>shipping location</Glossary> details.

  This API service implemented using JSON messaging. You, as the customer, are responsible for sending JSON messages and for maintaining the capability of receiving JSON messages in the format described in this documentation.

  <Image align="center" src="https://files.readme.io/c388f57ddfed471dccc9c49befdedf8da79a14260f9ffbbc5e7f5996226f2022-Intersoft_api_art.png" width="300px" />
</Accordion>

The Intersoft SAPIENT Developers Hub provides both new and current users with a step-by-step guide on how to set up a <Glossary>shipping account</Glossary>, <Glossary>shipments</Glossary>, and get started as a new user. Furthermore, this section covers the vital processes on how the business clients can utilise the API to carry out shipping activities with available carriers, as well as the technical details required to build this integration.

***

<Banner isInline={true} message="Seamless integration awaits: Get started with SAPIENT" color="#ffb600" textColor="#ffffff" fontSize="20px" fontWeight="bold" />

Get ready to integrate our powerful API into your existing systems. Whether you are looking to streamline shipping management, monitor performance metrics, or customise your logistics workflows, our APIs provide the flexibility and scalability you need to succeed.

<SimpleStepper>
  <SimpleStep header="1. Create API Credentials">
    <Image align="center" src="https://files.readme.io/631288afff2a17353aead1452f46b1c8477702d40886341d0ee7b672de51bba0-API_icon.png" width="100px" />

    [Set up your authentication credentials](https://docs.intersoftsapient.net/v4.02_4.03_Testing/docs/create-api-credentials#/) to start accessing the SAPIENT API securely
  </SimpleStep>

  <SimpleStep header="2. Activate Integration">
    <Image align="center" src="https://files.readme.io/0d834350d524acfd7c9056a10823a436f98427aab0d97a5f88193414b311d680-Activate_icon.png" width="100px" />

    [Enable your integration](https://docs.intersoftsapient.net/v4.02_4.03_Testing/docs/integration-activation#/) to begin using SAPIENT's shipping capabilities
  </SimpleStep>

  <SimpleStep header="3. Add Users">
    <Image align="center" src="https://files.readme.io/9182449761017b81f93b51f03c22f6653be9ce6379dd4c0f97d71f3b6b9eaadc-Add_user_icon.png" width="100px" />

    [Add users](https://docs.intersoftsapient.net/v4.02_4.03_Testing/docs/add-users-to-your-organisation-to-begin-collaborating-with-your-team#/) and invite them to collaborate and manage your shipping operations
  </SimpleStep>

  <SimpleStep header="4. Add Shipping Location">
    <Image align="center" border={false} width="100px" src="https://files.readme.io/b39ab1a7142550c3018a81fedda67069e7e5a83c72b48e62e0d58010f4ef19f5-Add_location_icon.png" />

    [Configure your shipping locations](https://docs.intersoftsapient.net/v4.02_4.03_Testing/docs/add-a-shipping-location#/) to define from where the shipments will originate.
  </SimpleStep>

  <SimpleStep header="5. Add Shipping Account">
    <Image align="center" src="https://files.readme.io/4552bab17f8918d2c3798a73045513e467d7b498a0ff5302a7b29ce08e239965-Add_shipping_account_icon.png" width="60px" />

    [Set up carrier shipping accounts](https://docs.intersoftsapient.net/v4.02_4.03_Testing/docs/add-a-shipping-account#/) to enable shipping services through SAPIENT
  </SimpleStep>
</SimpleStepper>

> 🚧 _Important_
>
> _The API requires the user to provide a <Anchor label="Bearer token" target="_blank" href="https://docs.intersoftsapient.net/docs/bearer-token-generation-1">Bearer token</Anchor>. To learn more about the bearer token and its generation, refer to the <Anchor label="Authentication" target="_blank" href="https://docs.intersoftsapient.net/docs/authentication">Authentication</Anchor> section._

***

## Further Reading

Explore additional resources to deepen your understanding of the SAPIENT system and its capabilities.

<Tabs>
  <Tab title="User Guides">
    <Cards columns={3}>
      <Card title="Maintenance Guides" href="https://docs.intersoftsapient.net/docs/maintenance-guides" icon="fa-book-open" iconColor="">
        Learn how to maintain and configure your SAPIENT system effectively
      </Card>

      <Card title="Additional Services" href="https://docs.intersoftsapient.net/docs/additional-services-user-guides" icon="fa-solid fa-layer-plus" iconColor="">
        Discover additional services and features available through SAPIENT
      </Card>

      <Card title="Carrier-Specific Guides" href="https://docs.intersoftsapient.net/v4.02_4.03_Testing/docs/carrrier-specific-user-guides#/" icon="fa-book-open" iconColor="">
        Explore the carrier integrations available on SAPIENT
      </Card>
    </Cards>
  </Tab>

  <Tab title="Operations">
    <Cards columns={2}>
      <Card title="Shipment Creation & Manifesting" href="https://docs.intersoftsapient.net/docs/shipment-creation-and-manifesting" icon="fa-solid fa-arrow-progress" iconColor="">
        Full flows on creating shipments and generating manifests
      </Card>

      <Card title="Intersoft Tracking Webhook" href="https://docs.intersoftsapient.net/v4.02_4.03_Testing/docs/tracking-webhook-1#/versions" icon="fa-solid fa-webhook" iconColor="">
        Use our tracking webhook solution to receive real-time updates and data from various services and applications.
      </Card>
    </Cards>
  </Tab>

  <Tab title="Reference">
    <Cards columns={2}>
      <Card title="Glossary" href="https://docs.intersoftsapient.net/docs/glossary-1" icon="fa-solid fa-arrow-down-a-z">
        Definitions and explanations of key terms used in SAPIENT.
      </Card>

      <Card title="Archived Release Notes" href="https://docs.intersoftsapient.net/docs/archived-release-notes" icon="fa-solid fa-box-archive">
        Historical information about previous system updates and changes.
      </Card>
    </Cards>
  </Tab>
</Tabs>
