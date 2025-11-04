---
title: Welcome to SAPIENT Developers Hub
deprecated: false
hidden: false
icon: fad fa-diagram-lean-canvas
link:
  new_tab: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  pages:
    - slug: integration-activation
      title: Integration Activation
      type: basic
---
# Introduction

APIs play a crucial role in the SAPIENT system by facilitating seamless integration with various shipping carriers, third party logistics providers, and other eCommerce platforms. This connectivity allows businesses to automate data exchange, streamline workflows, and ensure real-time updates on shipping performance.

<Columns layout="auto">
  <Column>
    If you are looking to build an integration, then our API solution will help you incorporate the intelligence of Intersoft SAPIENT into your software with minimal integration effort.

    
The Intersoft SAPIENT Developers Hub provides both new and current users with a step-by-step guide on how to set up a <Glossary>shipping account</Glossary>, <Glossary>shipments</Glossary>, and get started as a new user.
    

  Furthermore, this section covers the vital processes on how the business clients can utilise the API to carry out shipping activities with available carriers, as well as the technical details required to build this integration.
 </Column>
</Columns>

## Getting started

This section outlines the essential information on our APIs and steps to begin utilising the SAPIENT APIs, including setup instructions, authentication processes, and key functionalities that can be accessed through the API and SAPIENT's UI.

<Tabs>
  <Tab title="API Overview">
    **Intersoft SAPIENT API** enables you to create and manage shipments, produce labels and customs documentation, generate and print collection manifests. The API also allows you to retrieve reference data such as carriers supported by the platform and the countries where shipments can be sent, maintain your own data required for these, such as adding and managing shipping accounts and <Glossary>shipping location</Glossary> details.

    **Intersoft API** is a fully RESTful service implemented using JSON messaging. You, as the customer, are responsible for sending JSON messages and for maintaining the capability of receiving JSON messages in the format described in this documentation.

    <Image align="center" src="https://files.readme.io/c388f57ddfed471dccc9c49befdedf8da79a14260f9ffbbc5e7f5996226f2022-Intersoft_api_art.png" width="500px" />
  </Tab>

  <Tab title="Integration Steps">
    ### Seamless integration awaits: Get started with SAPIENT

    Get ready to integrate our powerful API into your existing systems. Whether you are looking to streamline shipping management, monitor performance metrics, or customise your logistics workflows, our APIs provide the flexibility and scalability you need to succeed.

    > 🚧 *Important*
    >
    > *The API requires the user to provide a[Bearer token](https://docs.intersoftsapient.net/docs/bearer-token-generation-1). To learn more about the bearer token and its generation, refer to the [Authentication](https://docs.intersoftsapient.net/docs/authentication) section.*
  </Tab>
</Tabs>

### Setup Checklist

<Cards columns="3">
  <Card title="" href="https://docs.intersoftsapient.net/docs/create-api-credentials" icon="">
    <Image align="center" src="https://files.readme.io/c388f57ddfed471dccc9c49befdedf8da79a14260f9ffbbc5e7f5996226f2022-Intersoft_api_art.png" width="200px" alt="thumbnail" />
  </Card>

  <Card title="Activate Integration" href="doc:integration-activation" icon="fa-solid fa-power-off">
    Activate your integration to start using SAPIENT services
  </Card>

  <Card title="Add Users" href="doc:add-users-to-your-organisation-to-begin-collaborating-with-your-team" icon="users">
    Add team members to your organisation for collaboration
  </Card>

  <Card title="Add Shipping Locations" href="https://docs.intersoftsapient.net/docs/add-a-shipping-location" icon="map-marker-alt">
    Configure your shipping locations for dispatch
  </Card>

  <Card title="Add Shipping Accounts" href="https://docs.intersoftsapient.net/docs/add-a-shipping-account" icon="credit-card">
    Set up carrier accounts for shipping services
  </Card>
</Cards>

***

## Further Reading

<Cards columns="3">
  <Card title="User Guides" href="https://docs.intersoftsapient.net/docs/maintenance-guides" icon="book">
    Comprehensive guides for using SAPIENT features
  </Card>

  <Card title="Shipment Creation" href="https://docs.intersoftsapient.net/docs/shipment-creation-and-manifesting" icon="box">
    Learn about creating shipments and manifesting
  </Card>

  <Card title="Additional Services" href="https://docs.intersoftsapient.net/docs/additional-services-user-guides" icon="plus-circle">
    Explore additional SAPIENT services
  </Card>

  <Card title="Carrier Guides" href="https://docs.intersoftsapient.net/docs/carrier-specific-user-guides" icon="truck">
    Carrier-specific implementation guides
  </Card>

  <Card title="Glossary" href="https://docs.intersoftsapient.net/docs/glossary-1" icon="list">
    Terms and definitions used in SAPIENT
  </Card>

  <Card title="Release Notes" href="https://docs.intersoftsapient.net/docs/archived-release-notes" icon="clipboard-list">
    Archived release notes and updates
  </Card>
</Cards>

<HTMLBlock>{`
 <table>
   <thead>
     <tr>
       <th> API Object </th>
       <th> API Field Name </th>
     </tr>
   </thead>
   <tbody>
     <tr>
       <td rowspan="4"> <b>Address</b> </td>
     </tr>
     <tr>
       <td> Town </td>
     </tr>
     <tr>
       <td> PostCode </td>
     </tr>
     <tr>
       <td> County </td>
     </tr>
     <tr>
       <td rowspan="4"> <b>Packages</b> </td>
     </tr>
     <tr>
       <td> Town </td>
     </tr>
     <tr>
       <td> PostCode </td> 
     </tr>
     <tr>
       <td> County 
         </td>
       
     </tr>
   </tbody>
</table>
`}</HTMLBlock>

[![Go to Documentation](https://example.com/Intersoft_api_art.png)](https://-page)

<br />