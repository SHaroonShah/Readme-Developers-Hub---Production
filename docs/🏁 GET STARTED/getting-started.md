---
title: Welcome to SAPIENT Developers Hub
excerpt: >-
  Welcome to Intersoft SAPIENT, a scalable carrier management platform designed
  to facilitate seamless integration with various shipping carriers, third-party
  logistics provider, and other eCommerce platforms. By leveraging APIs, SAPIENT
  enhances its adaptability and user friendliness, providing a simple, reliant
  shipping API to easily create and manage shipments, generate labels, and more.
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
<Image align="center" border={false} src="https://files.readme.io/0584ce0be71c220cb468d3c532a2c8ce10f81d4f6a9d8db111ca945bee9ac384-generated_image_222222222.gif" />

# Introduction

APIs play a crucial role in the SAPIENT system by facilitating seamless integration with various shipping carriers, third party logistics providers, and other eCommerce platforms. This connectivity allows businesses to automate data exchange, streamline workflows, and ensure real-time updates on shipping performance.

<Columns layout="auto">
  <Column>
    If you are looking to build an integration, then our API solution will help you incorporate the intelligence of Intersoft SAPIENT into your software with minimal integration effort.

    The Intersoft SAPIENT Developers Hub provides both new and current users with a step-by-step guide on how to set up a <Glossary>shipping account</Glossary>, <Glossary>shipments</Glossary>, and get started as a new user.
  </Column>

  <Column>
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

<Cards columns="2">
  <Card title="Create API Credentials" href="https://docs.intersoftsapient.net/docs/create-api-credentials" icon="fa-solid fa-key">
    Set up your API credentials to authenticate with the SAPIENT platform
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
       <td> County </td>
       
     </tr>
   </tbody>
</table>
`}</HTMLBlock>

<HTMLBlock>{`
<tbody><tr><th rowspan="1" colspan="3" colorname="" class="ak-renderer-tableHeader-sortable-column__wrapper" data-colwidth="193,212,84" aria-sort="none"><div class="ak-renderer-tableHeader-sortable-column"><p data-renderer-start-pos="2939"><strong data-renderer-mark="true">createIdCardRequest</strong></p><figure class="ak-renderer-tableHeader-sorting-icon__wrapper ak-renderer-tableHeader-sorting-icon__no-order"><div role="presentation"><div class="ak-renderer-tableHeader-sorting-icon ak-renderer-tableHeader-sorting-icon__not-allowed css-2i5j3y" role="button" tabindex="-1" aria-label="You can't sort a table with merged cells" aria-disabled="true" aria-hidden="true"><div class="sorting-icon-svg__not-allowed ak-renderer-tableHeader-sorting-icon-inactive css-1asrlx7"><div class="css-8nrin7"></div></div></div></div></figure></div></th><th rowspan="1" colspan="2" colorname="" class="ak-renderer-tableHeader-sortable-column__wrapper" data-colwidth="105,281" aria-sort="none"><div class="ak-renderer-tableHeader-sortable-column"><p data-renderer-start-pos="2962">&nbsp;</p><figure class="ak-renderer-tableHeader-sorting-icon__wrapper ak-renderer-tableHeader-sorting-icon__no-order"><div role="presentation"><div class="ak-renderer-tableHeader-sorting-icon ak-renderer-tableHeader-sorting-icon__not-allowed css-2i5j3y" role="button" tabindex="-1" aria-label="You can't sort a table with merged cells" aria-disabled="true" aria-hidden="true"><div class="sorting-icon-svg__not-allowed ak-renderer-tableHeader-sorting-icon-inactive css-1asrlx7"><div class="css-8nrin7"></div></div></div></div></figure></div></th></tr><tr><td rowspan="1" colspan="1" colorname="" data-colwidth="193"><p data-renderer-start-pos="2968"><strong data-renderer-mark="true">Field</strong></p></td><td rowspan="1" colspan="1" colorname="" data-colwidth="212"><p data-renderer-start-pos="2977"><strong data-renderer-mark="true">Element Name. Aggregate: </strong>&lt;createIdCardRequest&gt;&lt;integrationHeader&gt;</p></td><td rowspan="1" colspan="1" colorname="" data-colwidth="84"><p data-renderer-start-pos="3046"><strong data-renderer-mark="true">Data Type</strong></p></td><td rowspan="1" colspan="1" colorname="" data-colwidth="105"><p data-renderer-start-pos="3059"><strong data-renderer-mark="true">M/C/O</strong></p></td><td rowspan="1" colspan="1" colorname="" data-colwidth="281"><p data-renderer-start-pos="3068"><strong data-renderer-mark="true">Description</strong></p></td></tr><tr><td rowspan="1" colspan="1" colorname="" data-colwidth="193"><p data-renderer-start-pos="3085">Date and Time</p></td><td rowspan="1" colspan="1" colorname="" data-colwidth="212"><p data-renderer-start-pos="3102">&lt;dateTimeStamp&gt;</p></td><td rowspan="1" colspan="1" colorname="" data-colwidth="84"><p data-renderer-start-pos="3121">D-19</p></td><td rowspan="1" colspan="1" colorname="" data-colwidth="105"><p data-renderer-start-pos="3129"><span data-annotation-inline-node="true" data-annotation-mark="true" data-renderer-start-pos="3129" role="emphasis"><span class="status-lozenge-span" data-node-type="status" data-color="yellow"><span class="_2rkofajl _1reo15vq _18m915vq _1e0c116y _vchhusvi _kqswpfqs _1kz6184x _bozg1b66 _y4ti1b66 _bfhkxmjf" style="max-width: 100%;"><span class="_1reo15vq _18m915vq _ect41gqc _1wyb1skh _zg8l4jg8 _k48pmoej _vwz47vkz _1bto1l2s _1p1dangw _o5721q9c _1dyz9vsi _syazwwip" style="max-width: calc(200px - var(--ds-space-100, 8px));">O -optional</span></span></span></span> </p></td><td rowspan="1" colspan="1" colorname="" data-colwidth="281"><p data-renderer-start-pos="3135">The date and time when the create ID card request is made. It is formatted as yyyy-mm-dd hh:mm:ss to maintain consistency in timestamps across the system, facilitating tracking and auditing of requests.</p></td></tr><tr><td rowspan="1" colspan="1" colorname="" data-colwidth="193"><p data-renderer-start-pos="3343">Transaction ID</p></td><td rowspan="1" colspan="1" colorname="" data-colwidth="212"><p data-renderer-start-pos="3361">&lt;transactionI&gt;</p></td><td rowspan="1" colspan="1" colorname="" data-colwidth="84"><p data-renderer-start-pos="3379">C-32</p></td><td rowspan="1" colspan="1" colorname="" data-colwidth="105"><p data-renderer-start-pos="3387"><span data-annotation-inline-node="true" data-annotation-mark="true" data-renderer-start-pos="3387" role="emphasis"><span class="status-lozenge-span" data-node-type="status" data-color="red"><span class="_2rkofajl _1reo15vq _18m915vq _1e0c116y _vchhusvi _kqswpfqs _1kz6184x _bozg1b66 _y4ti1b66 _bfhk1366" style="max-width: 100%;"><span class="_1reo15vq _18m915vq _ect41gqc _1wyb1skh _zg8l4jg8 _k48pmoej _vwz47vkz _1bto1l2s _1p1dangw _o5721q9c _1dyz9vsi _syazwwip" style="max-width: calc(200px - var(--ds-space-100, 8px));">M - Mandatory</span></span></span></span> </p></td><td rowspan="1" colspan="1" colorname="" data-colwidth="281"><p data-renderer-start-pos="3393">A unique identifier preserved throughout the lifespan of the transaction. This ID is essential for tracking the specific request and is unique when combined with the <strong data-renderer-mark="true">applicationId</strong>. It helps maintain the integrity of the process and allows for troubleshooting or inquiry into specific transactions.</p></td></tr><tr><td rowspan="1" colspan="1" colorname="" data-colwidth="193"><p data-renderer-start-pos="3696">Application ID</p></td><td rowspan="1" colspan="1" colorname="" data-colwidth="212"><p data-renderer-start-pos="3714">&lt;applicationId&gt;</p></td><td rowspan="1" colspan="1" colorname="" data-colwidth="84"><p data-renderer-start-pos="3733">C-10</p></td><td rowspan="1" colspan="1" colorname="" data-colwidth="105"><p data-renderer-start-pos="3741"><span data-annotation-inline-node="true" data-annotation-mark="true" data-renderer-start-pos="3741" role="emphasis"><span class="status-lozenge-span" data-node-type="status" data-color="red"><span class="_2rkofajl _1reo15vq _18m915vq _1e0c116y _vchhusvi _kqswpfqs _1kz6184x _bozg1b66 _y4ti1b66 _bfhk1366" style="max-width: 100%;"><span class="_1reo15vq _18m915vq _ect41gqc _1wyb1skh _zg8l4jg8 _k48pmoej _vwz47vkz _1bto1l2s _1p1dangw _o5721q9c _1dyz9vsi _syazwwip" style="max-width: calc(200px - var(--ds-space-100, 8px));">M - Mandatory</span></span></span></span></p></td><td rowspan="1" colspan="1" colorname="" data-colwidth="281"><p data-renderer-start-pos="3746">For a request, this field represents the ID of the service requester calling the API, ensuring that the request is linked to a legitimate source.</p><p data-renderer-start-pos="3893">For the response, the applicationId indicates the ID of the service provider, which must also combine uniquely with the Transaction ID. This attribute enhances security and accountability by clearly identifying both the client and server involved in the transaction.</p></td></tr><tr><td rowspan="1" colspan="1" colorname="" data-colwidth="193"><p data-renderer-start-pos="4165">UserId</p></td><td rowspan="1" colspan="1" colorname="" data-colwidth="212"><p data-renderer-start-pos="4175">&lt;userId&gt;</p></td><td rowspan="1" colspan="1" colorname="" data-colwidth="84"><p data-renderer-start-pos="4187">C-10</p></td><td rowspan="1" colspan="1" colorname="" data-colwidth="105"><p data-renderer-start-pos="4195"><span data-annotation-inline-node="true" data-annotation-mark="true" data-renderer-start-pos="4195" role="emphasis"><span class="status-lozenge-span" data-node-type="status" data-color="red"><span class="_2rkofajl _1reo15vq _18m915vq _1e0c116y _vchhusvi _kqswpfqs _1kz6184x _bozg1b66 _y4ti1b66 _bfhk1366" style="max-width: 100%;"><span class="_1reo15vq _18m915vq _ect41gqc _1wyb1skh _zg8l4jg8 _k48pmoej _vwz47vkz _1bto1l2s _1p1dangw _o5721q9c _1dyz9vsi _syazwwip" style="max-width: calc(200px - var(--ds-space-100, 8px));">M - Mandatory</span></span></span></span></p></td><td rowspan="1" colspan="1" colorname="" data-colwidth="281"><p data-renderer-start-pos="4200">A unique identifier provided by the Intersoft platform for system access, provided by the Intersoft platform. It ensures that only authorised users can initiate <strong data-renderer-mark="true">createIdCardRequest</strong>, thus safeguarding the registration process.</p></td></tr><tr><td rowspan="1" colspan="1" colorname="" data-colwidth="193"><p data-renderer-start-pos="4431">Password</p></td><td rowspan="1" colspan="1" colorname="" data-colwidth="212"><p data-renderer-start-pos="4443">&lt;password&gt;</p></td><td rowspan="1" colspan="1" colorname="" data-colwidth="84"><p data-renderer-start-pos="4457">C-10</p></td><td rowspan="1" colspan="1" colorname="" data-colwidth="105"><p data-renderer-start-pos="4465"><span data-annotation-inline-node="true" data-annotation-mark="true" data-renderer-start-pos="4465" role="emphasis"><span class="status-lozenge-span" data-node-type="status" data-color="red"><span class="_2rkofajl _1reo15vq _18m915vq _1e0c116y _vchhusvi _kqswpfqs _1kz6184x _bozg1b66 _y4ti1b66 _bfhk1366" style="max-width: 100%;"><span class="_1reo15vq _18m915vq _ect41gqc _1wyb1skh _zg8l4jg8 _k48pmoej _vwz47vkz _1bto1l2s _1p1dangw _o5721q9c _1dyz9vsi _syazwwip" style="max-width: calc(200px - var(--ds-space-100, 8px));">M - Mandatory</span></span></span></span></p></td><td rowspan="1" colspan="1" colorname="" data-colwidth="281"><p data-renderer-start-pos="4470">The password to be used in conjunction with the <strong data-renderer-mark="true">UserId. </strong>It is required for authenticating the user making the request, providing an additional layer of security by verifying their identity before allowing changes to the system.</p></td></tr></tbody>
`}</HTMLBlock>

<br />
