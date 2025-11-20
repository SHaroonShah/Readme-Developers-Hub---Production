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

<Image align="center" border={false} width="500px" src="https://files.readme.io/c388f57ddfed471dccc9c49befdedf8da79a14260f9ffbbc5e7f5996226f2022-Intersoft_api_art.png" />

The Intersoft SAPIENT Developers Hub provides both new and current users with a step-by-step guide on how to set up a <Glossary>shipping account</Glossary>, <Glossary>shipments</Glossary>, and get started as a new user. Furthermore, this section covers the vital processes on how the business clients can utilise the API to carry out shipping activities with available carriers, as well as the technical details required to build this integration.

## Overview

<Accordion title="What is SAPIENT API?" icon="rocket">
  This section outlines the essential information on our APIs and steps to begin utilising the SAPIENT APIs, including setup instructions, authentication processes, and key functionalities that can be accessed through the API and SAPIENT's UI. Whether you are a developer or a business user, this section offers the necessary resources to seamlessly connect and optimise your processes within the SAPIENT platform.

  **Intersoft SAPIENT API** enables you to create and manage shipments, produce labels and customs documentation, generate and print collection manifests. The API also allows you to retrieve reference data such as carriers supported by the platform and the countries where shipments can be sent, maintain your own data required for these, such as adding and managing shipping accounts and <Glossary>shipping location</Glossary> details.

  **Intersoft API** is a fully RESTful service implemented using JSON messaging. You, as the customer, are responsible for sending JSON messages and for maintaining the capability of receiving JSON messages in the format described in this documentation.
</Accordion>

## Seamless integration awaits: Get started with SAPIENT

Get ready to integrate our powerful API into your existing systems. Whether you are looking to streamline shipping management, monitor performance metrics, or customise your logistics workflows, our APIs provide the flexibility and scalability you need to succeed.

<SimpleStepper>
  <SimpleStep header="Step 1: Create API Credentials">
    Plan your documentation and gather resources.
  </SimpleStep>

  <SimpleStep header="Step 2: Write">
    Write effective and clear documentation.
  </SimpleStep>

  <SimpleStep header="Step 3: Review">
    Review and refine your content.
  </SimpleStep>

  <SimpleStep header="Step 4: Review">
    Review and refine your content.
  </SimpleStep>

  <SimpleStep header="Step 5: Review">
    Review and refine your content.
  </SimpleStep>
</SimpleStepper>

<Cards columns={2}>
  <Card title="Create API Credentials" href="https://docs.intersoftsapient.net/docs/create-api-credentials" icon="key">
    Set up your authentication credentials to start accessing the SAPIENT API securely.
  </Card>

  <Card title="Activate Integration" href="doc:integration-activation" icon="power-off">
    Enable your integration to begin using SAPIENT's shipping capabilities.
  </Card>

  <Card title="Add Users" href="doc:add-users-to-your-organisation-to-begin-collaborating-with-your-team" icon="users">
    Invite team members to collaborate and manage your shipping operations together.
  </Card>

  <Card title="Add Shipping Locations" href="https://docs.intersoftsapient.net/docs/add-a-shipping-location" icon="map-marker-alt">
    Configure your shipping locations to define where packages will be sent from.
  </Card>

  <Card title="Add Shipping Accounts" href="https://docs.intersoftsapient.net/docs/add-a-shipping-account" icon="credit-card">
    Set up carrier accounts to enable shipping services through various providers.
  </Card>
</Cards>

> 🚧 _Important_
>
> _The API requires the user to provide a [Bearer token](https://docs.intersoftsapient.net/docs/bearer-token-generation-1). To learn more about the bearer token and its generation, refer to the [Authentication](https://docs.intersoftsapient.net/docs/authentication) section._

***

## Further Reading

Explore additional resources to deepen your understanding of the SAPIENT system and its capabilities.

<Tabs>
  <Tab title="User Guides">
    <Cards columns={2}>
      <Card title="Maintenance Guides" href="https://docs.intersoftsapient.net/docs/maintenance-guides" icon="tools">
        Learn how to maintain and configure your SAPIENT system effectively.
      </Card>

      <Card title="Additional Services" href="https://docs.intersoftsapient.net/docs/additional-services-user-guides" icon="plus-circle">
        Discover additional services and features available through SAPIENT.
      </Card>
    </Cards>
  </Tab>

  <Tab title="Operations">
    <Cards columns={2}>
      <Card title="Shipment Creation & Manifesting" href="https://docs.intersoftsapient.net/docs/shipment-creation-and-manifesting" icon="shipping-fast">
        Complete guide on creating shipments and generating manifests.
      </Card>

      <Card title="Carrier Specific Guides" href="https://docs.intersoftsapient.net/docs/carrier-specific-user-guides" icon="truck">
        Detailed instructions for working with specific shipping carriers.
      </Card>
    </Cards>
  </Tab>

  <Tab title="Reference">
    <Cards columns={2}>
      <Card title="Glossary" href="https://docs.intersoftsapient.net/docs/glossary-1" icon="book">
        Definitions and explanations of key terms used in SAPIENT.
      </Card>

      <Card title="Archived Release Notes" href="https://docs.intersoftsapient.net/docs/archived-release-notes" icon="archive">
        Historical information about previous system updates and changes.
      </Card>
    </Cards>
  </Tab>
</Tabs>
