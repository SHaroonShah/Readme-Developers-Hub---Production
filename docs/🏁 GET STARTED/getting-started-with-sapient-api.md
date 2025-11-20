---
title: Getting started with SAPIENT API
excerpt: >-
  Welcome to Intersoft SAPIENT, a scalable carrier management platform designed
  to facilitate seamless integration with various shipping carriers, third-party
  logistics provider, and other eCommerce platforms. By leveraging APIs, SAPIENT
  enhances its adaptability and user friendliness, providing a simple, reliant
  shipping API to easily create and manage shipments, generate labels, and more.
deprecated: false
hidden: true
icon: fad fa-diagram-lean-canvas
link:
  new_tab: false
metadata:
  robots: index
---
# Introduction

APIs play a crucial role in the SAPIENT system by facilitating seamless integration with various shipping carriers, third-party logistics providers, and other eCommerce platforms. This connectivity allows businesses to automate data exchange, streamline workflows, and ensure real-time updates on shipping performance.

<Image align="center" border={true} src="https://files.readme.io/82fb0cbe41a890f07d419cd0f39a19ec47336cd51e97fe6969efdb6b26a4d82d-Sapient.png" className="border" />

If you are looking to build an integration, then our API solution will help you incorporate the intelligence of Intersoft SAPIENT into your software with minimal integration effort.

## What is SAPIENT API?

<Accordion title="API Overview" icon="code">

**Intersoft SAPIENT API** enables you to create and manage shipments, produce labels and customs documentation, generate and print collection manifests. The API also allows you to retrieve reference data such as carriers supported by the platform and the countries where shipments can be sent, maintain your own data required for these, such as adding and managing shipping accounts and <Glossary>shipping location</Glossary> details.

**Intersoft API** is a fully RESTful service implemented using JSON messaging. You, as the customer, are responsible for sending JSON messages and for maintaining the capability of receiving JSON messages in the format described in this documentation.

<Image align="center" border={false} width="500px" src="https://files.readme.io/c388f57ddfed471dccc9c49befdedf8da79a14260f9ffbbc5e7f5996226f2022-Intersoft_api_art.png" />

</Accordion>

## Getting Started Checklist

<Columns layout="auto">
<Column>

### Seamless integration awaits: Get started with SAPIENT

Get ready to integrate our powerful API into your existing systems. Whether you are looking to streamline shipping management, monitor performance metrics, or customise your logistics workflows, our APIs provide the flexibility and scalability you need to succeed.

</Column>
</Columns>

<Cards columns={2}>
  <Card title="Create API Credentials" href="https://docs.intersoftsapient.net/docs/create-api-credentials" icon="key">
    Set up your authentication credentials to access the SAPIENT API securely.
  </Card>
  <Card title="Activate Integration" href="https://docs.intersoftsapient.net/docs/integration-activation" icon="plug">
    Enable your integration to start using SAPIENT's powerful features.
  </Card>
  <Card title="Add Users" href="https://docs.intersoftsapient.net/docs/add-users-to-your-organisation-to-begin-collaborating-with-your-team" icon="users">
    Invite team members to collaborate on your SAPIENT organization.
  </Card>
  <Card title="Add Shipping Locations" href="https://docs.intersoftsapient.net/docs/add-a-shipping-location" icon="map-marker-alt">
    Configure your shipping locations for accurate shipment processing.
  </Card>
  <Card title="Add Shipping Accounts" href="https://docs.intersoftsapient.net/docs/add-a-shipping-account" icon="truck">
    Set up carrier accounts to enable shipment creation and management.
  </Card>
</Cards>

> 🚧 _Important_
>
> _The API requires the user to provide a [Bearer token](https://docs.intersoftsapient.net/docs/bearer-token-generation-1). To learn more about the bearer token and its generation, refer to the [Authentication](https://docs.intersoftsapient.net/docs/authentication) section._

---

## Resources & Documentation

<Tabs>
  <Tab title="User Guides">
    <Cards columns={2}>
      <Card title="Maintenance Guides" href="https://docs.intersoftsapient.net/docs/maintenance-guides" icon="tools">
        Learn how to maintain and configure your SAPIENT setup.
      </Card>
      <Card title="Shipment Creation & Manifesting" href="https://docs.intersoftsapient.net/docs/shipment-creation-and-manifesting" icon="shipping-fast">
        Complete guide on creating shipments and generating manifests.
      </Card>
    </Cards>
  </Tab>
  <Tab title="Advanced Features">
    <Cards columns={2}>
      <Card title="Additional Services" href="https://docs.intersoftsapient.net/docs/additional-services-user-guides" icon="plus-circle">
        Explore advanced features and additional service options.
      </Card>
      <Card title="Carrier Specific Guides" href="https://docs.intersoftsapient.net/docs/carrier-specific-user-guides" icon="truck-loading">
        Detailed guides for integrating with specific shipping carriers.
      </Card>
    </Cards>
  </Tab>
  <Tab title="Reference">
    <Cards columns={2}>
      <Card title="Glossary" href="https://docs.intersoftsapient.net/docs/glossary-1" icon="book">
        Definitions of key terms and concepts used in SAPIENT.
      </Card>
      <Card title="Archived Release Notes" href="https://docs.intersoftsapient.net/docs/archived-release-notes" icon="archive">
        Historical release notes and version information.
      </Card>
    </Cards>
  </Tab>
</Tabs>

The Intersoft SAPIENT Developers Hub provides both new and current users with a step-by-step guide on how to set up a <Glossary>shipping account</Glossary>, <Glossary>shipments</Glossary>, and get started as a new user. Furthermore, this section covers the vital processes on how the business clients can utilise the API to carry out shipping activities with available carriers, as well as the technical details required to build this integration.