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
<tbody><tr data-prosemirror-content-type="node" data-prosemirror-node-name="tableRow" data-prosemirror-node-block="true" data-vc-nvs="true" data-header-row="true" data-is-observed="true" style="grid-template-columns: 373.641px 371.359px; width: 746px;"><th data-colwidth="326" class="pm-table-header-content-wrap" data-prosemirror-content-type="node" data-prosemirror-node-name="tableHeader" data-prosemirror-node-block="true"><div class="fabric-editor-block-mark fabric-editor-alignment fabric-editor-align-center" data-align="center" data-prosemirror-content-type="mark" data-prosemirror-mark-name="alignment"><p data-prosemirror-content-type="node" data-prosemirror-node-name="paragraph" data-prosemirror-node-block="true" style="anchor-name: --node-anchor-paragraph-8ca369d3-9fd7-4e63-be78-c60f05a01719;" data-drag-handler-anchor-name="--node-anchor-paragraph-8ca369d3-9fd7-4e63-be78-c60f05a01719" data-drag-handler-node-type="paragraph" data-drag-handler-anchor-depth="4"><strong data-prosemirror-content-type="mark" data-prosemirror-mark-name="strong">API object</strong></p></div></th><th data-colwidth="324" class="pm-table-header-content-wrap" data-prosemirror-content-type="node" data-prosemirror-node-name="tableHeader" data-prosemirror-node-block="true"><p data-prosemirror-content-type="node" data-prosemirror-node-name="paragraph" data-prosemirror-node-block="true" style="anchor-name: --node-anchor-paragraph-af7bd1b2-5ad8-4da5-b742-28d6bf0386ad;" data-drag-handler-anchor-name="--node-anchor-paragraph-af7bd1b2-5ad8-4da5-b742-28d6bf0386ad" data-drag-handler-node-type="paragraph" data-drag-handler-anchor-depth="4"><strong data-prosemirror-content-type="mark" data-prosemirror-mark-name="strong">Mandatory fields</strong></p></th></tr><tr data-prosemirror-content-type="node" data-prosemirror-node-name="tableRow" data-prosemirror-node-block="true"><td rowspan="5" data-colwidth="326" class="pm-table-cell-content-wrap" data-prosemirror-content-type="node" data-prosemirror-node-name="tableCell" data-prosemirror-node-block="true"><p data-prosemirror-content-type="node" data-prosemirror-node-name="paragraph" data-prosemirror-node-block="true" style="anchor-name: --node-anchor-paragraph-89de0678-c0be-4f5a-b58e-e9f7d04d289c;" data-drag-handler-anchor-name="--node-anchor-paragraph-89de0678-c0be-4f5a-b58e-e9f7d04d289c" data-drag-handler-node-type="paragraph" data-drag-handler-anchor-depth="4"><br class="ProseMirror-trailingBreak"></p><p data-prosemirror-content-type="node" data-prosemirror-node-name="paragraph" data-prosemirror-node-block="true" style="anchor-name: --node-anchor-paragraph-d1141f0d-df84-4a33-9f19-87aee3b95c45;" data-drag-handler-anchor-name="--node-anchor-paragraph-d1141f0d-df84-4a33-9f19-87aee3b95c45" data-drag-handler-node-type="paragraph" data-drag-handler-anchor-depth="4"><br class="ProseMirror-trailingBreak"></p><p data-prosemirror-content-type="node" data-prosemirror-node-name="paragraph" data-prosemirror-node-block="true" style="anchor-name: --node-anchor-paragraph-206ca6a4-2984-493e-9973-16fe62deac78;" data-drag-handler-anchor-name="--node-anchor-paragraph-206ca6a4-2984-493e-9973-16fe62deac78" data-drag-handler-node-type="paragraph" data-drag-handler-anchor-depth="4"><strong data-prosemirror-content-type="mark" data-prosemirror-mark-name="strong">Shipper &gt; Address</strong></p></td><td data-colwidth="324" class="pm-table-cell-content-wrap" data-prosemirror-content-type="node" data-prosemirror-node-name="tableCell" data-prosemirror-node-block="true"><p data-prosemirror-content-type="node" data-prosemirror-node-name="paragraph" data-prosemirror-node-block="true" style="anchor-name: --node-anchor-paragraph-551e0c46-fa4b-47ab-8147-bfcc30622f7d;" data-drag-handler-anchor-name="--node-anchor-paragraph-551e0c46-fa4b-47ab-8147-bfcc30622f7d" data-drag-handler-node-type="paragraph" data-drag-handler-anchor-depth="4">ContactName</p></td></tr><tr data-prosemirror-content-type="node" data-prosemirror-node-name="tableRow" data-prosemirror-node-block="true"><td data-colwidth="324" class="pm-table-cell-content-wrap" data-prosemirror-content-type="node" data-prosemirror-node-name="tableCell" data-prosemirror-node-block="true"><p data-prosemirror-content-type="node" data-prosemirror-node-name="paragraph" data-prosemirror-node-block="true" style="anchor-name: --node-anchor-paragraph-b9d1f565-b02c-4ef8-beb4-a5d7d7a90741;" data-drag-handler-anchor-name="--node-anchor-paragraph-b9d1f565-b02c-4ef8-beb4-a5d7d7a90741" data-drag-handler-node-type="paragraph" data-drag-handler-anchor-depth="4">Line 1</p></td></tr><tr data-prosemirror-content-type="node" data-prosemirror-node-name="tableRow" data-prosemirror-node-block="true"><td data-colwidth="324" class="pm-table-cell-content-wrap" data-prosemirror-content-type="node" data-prosemirror-node-name="tableCell" data-prosemirror-node-block="true"><p data-prosemirror-content-type="node" data-prosemirror-node-name="paragraph" data-prosemirror-node-block="true" style="anchor-name: --node-anchor-paragraph-38634f57-9a81-4251-960b-991accd41904;" data-drag-handler-anchor-name="--node-anchor-paragraph-38634f57-9a81-4251-960b-991accd41904" data-drag-handler-node-type="paragraph" data-drag-handler-anchor-depth="4">Town</p></td></tr><tr data-prosemirror-content-type="node" data-prosemirror-node-name="tableRow" data-prosemirror-node-block="true"><td data-colwidth="324" class="pm-table-cell-content-wrap" data-prosemirror-content-type="node" data-prosemirror-node-name="tableCell" data-prosemirror-node-block="true"><p data-prosemirror-content-type="node" data-prosemirror-node-name="paragraph" data-prosemirror-node-block="true" style="anchor-name: --node-anchor-paragraph-6eb0664a-64e7-4ad3-a728-4edcc8d89f46;" data-drag-handler-anchor-name="--node-anchor-paragraph-6eb0664a-64e7-4ad3-a728-4edcc8d89f46" data-drag-handler-node-type="paragraph" data-drag-handler-anchor-depth="4">PostCode</p></td></tr><tr data-prosemirror-content-type="node" data-prosemirror-node-name="tableRow" data-prosemirror-node-block="true"><td data-colwidth="324" class="pm-table-cell-content-wrap" data-prosemirror-content-type="node" data-prosemirror-node-name="tableCell" data-prosemirror-node-block="true"><p data-prosemirror-content-type="node" data-prosemirror-node-name="paragraph" data-prosemirror-node-block="true" style="anchor-name: --node-anchor-paragraph-c09e7883-4d81-4deb-aa13-edcbbf5ae738;" data-drag-handler-anchor-name="--node-anchor-paragraph-c09e7883-4d81-4deb-aa13-edcbbf5ae738" data-drag-handler-node-type="paragraph" data-drag-handler-anchor-depth="4">CountryCode</p></td></tr><tr data-prosemirror-content-type="node" data-prosemirror-node-name="tableRow" data-prosemirror-node-block="true"><td rowspan="4" data-colwidth="326" class="pm-table-cell-content-wrap" data-prosemirror-content-type="node" data-prosemirror-node-name="tableCell" data-prosemirror-node-block="true"><p data-prosemirror-content-type="node" data-prosemirror-node-name="paragraph" data-prosemirror-node-block="true" style="anchor-name: --node-anchor-paragraph-62be00d8-b405-4a25-b643-f5854dd86d9f;" data-drag-handler-anchor-name="--node-anchor-paragraph-62be00d8-b405-4a25-b643-f5854dd86d9f" data-drag-handler-node-type="paragraph" data-drag-handler-anchor-depth="4"><br class="ProseMirror-trailingBreak"></p><p data-prosemirror-content-type="node" data-prosemirror-node-name="paragraph" data-prosemirror-node-block="true" style="anchor-name: --node-anchor-paragraph-00f38063-5222-4e43-a510-df33fdbb0e85;" data-drag-handler-anchor-name="--node-anchor-paragraph-00f38063-5222-4e43-a510-df33fdbb0e85" data-drag-handler-node-type="paragraph" data-drag-handler-anchor-depth="4"><br class="ProseMirror-trailingBreak"></p><p data-prosemirror-content-type="node" data-prosemirror-node-name="paragraph" data-prosemirror-node-block="true" style="anchor-name: --node-anchor-paragraph-f822ed86-28a2-4205-81f9-39aac4847e40;" data-drag-handler-anchor-name="--node-anchor-paragraph-f822ed86-28a2-4205-81f9-39aac4847e40" data-drag-handler-node-type="paragraph" data-drag-handler-anchor-depth="4"><strong data-prosemirror-content-type="mark" data-prosemirror-mark-name="strong">Destination &gt; Address</strong></p></td><td data-colwidth="324" class="pm-table-cell-content-wrap" data-prosemirror-content-type="node" data-prosemirror-node-name="tableCell" data-prosemirror-node-block="true"><p data-prosemirror-content-type="node" data-prosemirror-node-name="paragraph" data-prosemirror-node-block="true" style="anchor-name: --node-anchor-paragraph-f036b4fe-cb15-4830-a08b-8aefcea11afe;" data-drag-handler-anchor-name="--node-anchor-paragraph-f036b4fe-cb15-4830-a08b-8aefcea11afe" data-drag-handler-node-type="paragraph" data-drag-handler-anchor-depth="4">ContactName</p></td></tr><tr data-prosemirror-content-type="node" data-prosemirror-node-name="tableRow" data-prosemirror-node-block="true"><td data-colwidth="324" class="pm-table-cell-content-wrap" data-prosemirror-content-type="node" data-prosemirror-node-name="tableCell" data-prosemirror-node-block="true"><p data-prosemirror-content-type="node" data-prosemirror-node-name="paragraph" data-prosemirror-node-block="true" style="anchor-name: --node-anchor-paragraph-03cd1e88-c688-4be2-8965-9c662471603f;" data-drag-handler-anchor-name="--node-anchor-paragraph-03cd1e88-c688-4be2-8965-9c662471603f" data-drag-handler-node-type="paragraph" data-drag-handler-anchor-depth="4">Line 1</p></td></tr><tr data-prosemirror-content-type="node" data-prosemirror-node-name="tableRow" data-prosemirror-node-block="true"><td data-colwidth="324" class="pm-table-cell-content-wrap" data-prosemirror-content-type="node" data-prosemirror-node-name="tableCell" data-prosemirror-node-block="true"><p data-prosemirror-content-type="node" data-prosemirror-node-name="paragraph" data-prosemirror-node-block="true" style="anchor-name: --node-anchor-paragraph-05d3ba15-cc4b-4a5d-b561-7f3c48939acc;" data-drag-handler-anchor-name="--node-anchor-paragraph-05d3ba15-cc4b-4a5d-b561-7f3c48939acc" data-drag-handler-node-type="paragraph" data-drag-handler-anchor-depth="4">Town</p></td></tr><tr data-prosemirror-content-type="node" data-prosemirror-node-name="tableRow" data-prosemirror-node-block="true"><td data-colwidth="324" class="pm-table-cell-content-wrap" data-prosemirror-content-type="node" data-prosemirror-node-name="tableCell" data-prosemirror-node-block="true"><p data-prosemirror-content-type="node" data-prosemirror-node-name="paragraph" data-prosemirror-node-block="true" style="anchor-name: --node-anchor-paragraph-42450c30-070f-4216-af61-2344dbeff57f;" data-drag-handler-anchor-name="--node-anchor-paragraph-42450c30-070f-4216-af61-2344dbeff57f" data-drag-handler-node-type="paragraph" data-drag-handler-anchor-depth="4">CountryCode</p></td></tr><tr data-prosemirror-content-type="node" data-prosemirror-node-name="tableRow" data-prosemirror-node-block="true"><td rowspan="4" data-colwidth="326" class="pm-table-cell-content-wrap" data-prosemirror-content-type="node" data-prosemirror-node-name="tableCell" data-prosemirror-node-block="true"><p data-prosemirror-content-type="node" data-prosemirror-node-name="paragraph" data-prosemirror-node-block="true" style="anchor-name: --node-anchor-paragraph-8e46b677-7627-4d0b-8802-cacbdac5b989;" data-drag-handler-anchor-name="--node-anchor-paragraph-8e46b677-7627-4d0b-8802-cacbdac5b989" data-drag-handler-node-type="paragraph" data-drag-handler-anchor-depth="4"><br class="ProseMirror-trailingBreak"></p><p data-prosemirror-content-type="node" data-prosemirror-node-name="paragraph" data-prosemirror-node-block="true" style="anchor-name: --node-anchor-paragraph-7bdf5ec3-3799-446f-82e0-92a1f1ea9356;" data-drag-handler-anchor-name="--node-anchor-paragraph-7bdf5ec3-3799-446f-82e0-92a1f1ea9356" data-drag-handler-node-type="paragraph" data-drag-handler-anchor-depth="4"><br class="ProseMirror-trailingBreak"></p><p data-prosemirror-content-type="node" data-prosemirror-node-name="paragraph" data-prosemirror-node-block="true" style="anchor-name: --node-anchor-paragraph-032a3599-190e-49c6-b51e-58b01ab268e6;" data-drag-handler-anchor-name="--node-anchor-paragraph-032a3599-190e-49c6-b51e-58b01ab268e6" data-drag-handler-node-type="paragraph" data-drag-handler-anchor-depth="4"><strong data-prosemirror-content-type="mark" data-prosemirror-mark-name="strong">Items</strong></p><p data-prosemirror-content-type="node" data-prosemirror-node-name="paragraph" data-prosemirror-node-block="true" style="anchor-name: --node-anchor-paragraph-63aabbe1-a5c4-4aa1-8809-13ebc99d2b2e;" data-drag-handler-anchor-name="--node-anchor-paragraph-63aabbe1-a5c4-4aa1-8809-13ebc99d2b2e" data-drag-handler-node-type="paragraph" data-drag-handler-anchor-depth="4"><br class="ProseMirror-trailingBreak"></p></td><td data-colwidth="324" class="pm-table-cell-content-wrap" data-prosemirror-content-type="node" data-prosemirror-node-name="tableCell" data-prosemirror-node-block="true"><p data-prosemirror-content-type="node" data-prosemirror-node-name="paragraph" data-prosemirror-node-block="true" style="anchor-name: --node-anchor-paragraph-8ac3fd38-1113-48d0-9ad9-50beea85405f;" data-drag-handler-anchor-name="--node-anchor-paragraph-8ac3fd38-1113-48d0-9ad9-50beea85405f" data-drag-handler-node-type="paragraph" data-drag-handler-anchor-depth="4">Quantity</p></td></tr><tr data-prosemirror-content-type="node" data-prosemirror-node-name="tableRow" data-prosemirror-node-block="true"><td data-colwidth="324" class="pm-table-cell-content-wrap" data-prosemirror-content-type="node" data-prosemirror-node-name="tableCell" data-prosemirror-node-block="true"><p data-prosemirror-content-type="node" data-prosemirror-node-name="paragraph" data-prosemirror-node-block="true" style="anchor-name: --node-anchor-paragraph-24c28f04-fd4d-4e54-bac1-7bee0e4b06fa;" data-drag-handler-anchor-name="--node-anchor-paragraph-24c28f04-fd4d-4e54-bac1-7bee0e4b06fa" data-drag-handler-node-type="paragraph" data-drag-handler-anchor-depth="4">Description</p></td></tr><tr data-prosemirror-content-type="node" data-prosemirror-node-name="tableRow" data-prosemirror-node-block="true"><td data-colwidth="324" class="pm-table-cell-content-wrap" data-prosemirror-content-type="node" data-prosemirror-node-name="tableCell" data-prosemirror-node-block="true"><p data-prosemirror-content-type="node" data-prosemirror-node-name="paragraph" data-prosemirror-node-block="true" style="anchor-name: --node-anchor-paragraph-53be43bb-70b5-4e86-96e9-4e25ca72d286;" data-drag-handler-anchor-name="--node-anchor-paragraph-53be43bb-70b5-4e86-96e9-4e25ca72d286" data-drag-handler-node-type="paragraph" data-drag-handler-anchor-depth="4">Value</p></td></tr><tr data-prosemirror-content-type="node" data-prosemirror-node-name="tableRow" data-prosemirror-node-block="true"><td data-colwidth="324" class="pm-table-cell-content-wrap" data-prosemirror-content-type="node" data-prosemirror-node-name="tableCell" data-prosemirror-node-block="true"><p data-prosemirror-content-type="node" data-prosemirror-node-name="paragraph" data-prosemirror-node-block="true" style="anchor-name: --node-anchor-paragraph-13ac50ec-5749-478e-aba4-522f1f5eb6e3;" data-drag-handler-anchor-name="--node-anchor-paragraph-13ac50ec-5749-478e-aba4-522f1f5eb6e3" data-drag-handler-node-type="paragraph" data-drag-handler-anchor-depth="4">Weight</p></td></tr></tbody>
`}</HTMLBlock>

<br />
