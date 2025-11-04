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
       <td> County 
         </td>
       
     </tr>
   </tbody>
</table>
`}</HTMLBlock>

<HTMLBlock>{`
<div class="_HorizontalGrid_19j2z_5" style="--ezui-c-horizontal-grid-grid-template-columns-xs: repeat(2, minmax(0, 1fr)); --ezui-c-horizontal-grid-grid-template-columns-md: repeat(5, minmax(0, 1fr)); --ezui-c-horizontal-grid-gap-xs: var(--ezui-space-3); --ezui-c-horizontal-grid-display: grid;"><a class="_container_1g8hs_5 _variantOutlined_1g8hs_65" href="/carriers/usps-guide"><div class="_area_1g8hs_23" style="--ezui-c-card-area-padding-xs: var(--ezui-space-0);"><div class="CarrierBox_CarrierBox__4v_GL"><div class="LogoBox_LogoBox__IzArO"><img alt="USPS Logo" loading="lazy" decoding="async" data-nimg="fill" sizes="(max-width: 640px) 50vw, (max-width: 1200px) 20vw" srcset="/carriers/usps-logo.png?w=128&amp;q=80 128w, /carriers/usps-logo.png?w=256&amp;q=80 256w, /carriers/usps-logo.png?w=384&amp;q=80 384w, /carriers/usps-logo.png?w=640&amp;q=80 640w, /carriers/usps-logo.png?w=750&amp;q=80 750w, /carriers/usps-logo.png?w=828&amp;q=80 828w, /carriers/usps-logo.png?w=1080&amp;q=80 1080w, /carriers/usps-logo.png?w=1200&amp;q=80 1200w, /carriers/usps-logo.png?w=1920&amp;q=80 1920w, /carriers/usps-logo.png?w=2048&amp;q=80 2048w, /carriers/usps-logo.png?w=3840&amp;q=80 3840w" src="/carriers/usps-logo.png?w=3840&amp;q=80" style="position: absolute; height: 100%; width: 100%; inset: 0px; color: transparent;"></div></div></div></a><a class="_container_1g8hs_5 _variantOutlined_1g8hs_65" href="/carriers/ups-guide"><div class="_area_1g8hs_23" style="--ezui-c-card-area-padding-xs: var(--ezui-space-0);"><div class="CarrierBox_CarrierBox__4v_GL"><div class="LogoBox_LogoBox__IzArO"><img alt="UPS Logo" loading="lazy" decoding="async" data-nimg="fill" sizes="(max-width: 640px) 50vw, (max-width: 1200px) 20vw" srcset="/carriers/ups-logo.svg?w=128&amp;q=80 128w, /carriers/ups-logo.svg?w=256&amp;q=80 256w, /carriers/ups-logo.svg?w=384&amp;q=80 384w, /carriers/ups-logo.svg?w=640&amp;q=80 640w, /carriers/ups-logo.svg?w=750&amp;q=80 750w, /carriers/ups-logo.svg?w=828&amp;q=80 828w, /carriers/ups-logo.svg?w=1080&amp;q=80 1080w, /carriers/ups-logo.svg?w=1200&amp;q=80 1200w, /carriers/ups-logo.svg?w=1920&amp;q=80 1920w, /carriers/ups-logo.svg?w=2048&amp;q=80 2048w, /carriers/ups-logo.svg?w=3840&amp;q=80 3840w" src="/carriers/ups-logo.svg?w=3840&amp;q=80" style="position: absolute; height: 100%; width: 100%; inset: 0px; color: transparent;"></div></div></div></a><a class="_container_1g8hs_5 _variantOutlined_1g8hs_65" href="/carriers/fedex-guide"><div class="_area_1g8hs_23" style="--ezui-c-card-area-padding-xs: var(--ezui-space-0);"><div class="CarrierBox_CarrierBox__4v_GL"><div class="LogoBox_LogoBox__IzArO"><img alt="FedEx Logo" loading="lazy" decoding="async" data-nimg="fill" sizes="(max-width: 640px) 50vw, (max-width: 1200px) 20vw" srcset="/carriers/fedex-logo.svg?w=128&amp;q=80 128w, /carriers/fedex-logo.svg?w=256&amp;q=80 256w, /carriers/fedex-logo.svg?w=384&amp;q=80 384w, /carriers/fedex-logo.svg?w=640&amp;q=80 640w, /carriers/fedex-logo.svg?w=750&amp;q=80 750w, /carriers/fedex-logo.svg?w=828&amp;q=80 828w, /carriers/fedex-logo.svg?w=1080&amp;q=80 1080w, /carriers/fedex-logo.svg?w=1200&amp;q=80 1200w, /carriers/fedex-logo.svg?w=1920&amp;q=80 1920w, /carriers/fedex-logo.svg?w=2048&amp;q=80 2048w, /carriers/fedex-logo.svg?w=3840&amp;q=80 3840w" src="/carriers/fedex-logo.svg?w=3840&amp;q=80" style="position: absolute; height: 100%; width: 100%; inset: 0px; color: transparent;"></div></div></div></a><a class="_container_1g8hs_5 _variantOutlined_1g8hs_65" href="/carriers/dhl-ecommerce-guide"><div class="_area_1g8hs_23" style="--ezui-c-card-area-padding-xs: var(--ezui-space-0);"><div class="CarrierBox_CarrierBox__4v_GL"><div class="LogoBox_LogoBox__IzArO"><img alt="DHL Logo" loading="lazy" decoding="async" data-nimg="fill" sizes="(max-width: 640px) 50vw, (max-width: 1200px) 20vw" srcset="/carriers/dhl-logo.svg?w=128&amp;q=80 128w, /carriers/dhl-logo.svg?w=256&amp;q=80 256w, /carriers/dhl-logo.svg?w=384&amp;q=80 384w, /carriers/dhl-logo.svg?w=640&amp;q=80 640w, /carriers/dhl-logo.svg?w=750&amp;q=80 750w, /carriers/dhl-logo.svg?w=828&amp;q=80 828w, /carriers/dhl-logo.svg?w=1080&amp;q=80 1080w, /carriers/dhl-logo.svg?w=1200&amp;q=80 1200w, /carriers/dhl-logo.svg?w=1920&amp;q=80 1920w, /carriers/dhl-logo.svg?w=2048&amp;q=80 2048w, /carriers/dhl-logo.svg?w=3840&amp;q=80 3840w" src="/carriers/dhl-logo.svg?w=3840&amp;q=80" style="position: absolute; height: 100%; width: 100%; inset: 0px; color: transparent;"></div></div></div></a><a class="_container_1g8hs_5 _variantOutlined_1g8hs_65" href="/carriers/canada-post-wallet-guide"><div class="_area_1g8hs_23" style="--ezui-c-card-area-padding-xs: var(--ezui-space-0);"><div class="CarrierBox_CarrierBox__4v_GL"><div class="LogoBox_LogoBox__IzArO"><img alt="Canada Post Logo" loading="lazy" decoding="async" data-nimg="fill" sizes="(max-width: 640px) 50vw, (max-width: 1200px) 20vw" srcset="/carriers/canada-post-logo.svg?w=128&amp;q=80 128w, /carriers/canada-post-logo.svg?w=256&amp;q=80 256w, /carriers/canada-post-logo.svg?w=384&amp;q=80 384w, /carriers/canada-post-logo.svg?w=640&amp;q=80 640w, /carriers/canada-post-logo.svg?w=750&amp;q=80 750w, /carriers/canada-post-logo.svg?w=828&amp;q=80 828w, /carriers/canada-post-logo.svg?w=1080&amp;q=80 1080w, /carriers/canada-post-logo.svg?w=1200&amp;q=80 1200w, /carriers/canada-post-logo.svg?w=1920&amp;q=80 1920w, /carriers/canada-post-logo.svg?w=2048&amp;q=80 2048w, /carriers/canada-post-logo.svg?w=3840&amp;q=80 3840w" src="/carriers/canada-post-logo.svg?w=3840&amp;q=80" style="position: absolute; height: 100%; width: 100%; inset: 0px; color: transparent;"></div></div></div></a><a class="_container_1g8hs_5 _variantOutlined_1g8hs_65" href="/carriers/royal-mail-guide"><div class="_area_1g8hs_23" style="--ezui-c-card-area-padding-xs: var(--ezui-space-0);"><div class="CarrierBox_CarrierBox__4v_GL"><div class="LogoBox_LogoBox__IzArO"><img alt="Royal Mail Logo" loading="lazy" decoding="async" data-nimg="fill" sizes="(max-width: 640px) 50vw, (max-width: 1200px) 20vw" srcset="/carriers/royal-mail-logo-ca.png?w=128&amp;q=80 128w, /carriers/royal-mail-logo-ca.png?w=256&amp;q=80 256w, /carriers/royal-mail-logo-ca.png?w=384&amp;q=80 384w, /carriers/royal-mail-logo-ca.png?w=640&amp;q=80 640w, /carriers/royal-mail-logo-ca.png?w=750&amp;q=80 750w, /carriers/royal-mail-logo-ca.png?w=828&amp;q=80 828w, /carriers/royal-mail-logo-ca.png?w=1080&amp;q=80 1080w, /carriers/royal-mail-logo-ca.png?w=1200&amp;q=80 1200w, /carriers/royal-mail-logo-ca.png?w=1920&amp;q=80 1920w, /carriers/royal-mail-logo-ca.png?w=2048&amp;q=80 2048w, /carriers/royal-mail-logo-ca.png?w=3840&amp;q=80 3840w" src="/carriers/royal-mail-logo-ca.png?w=3840&amp;q=80" style="position: absolute; height: 100%; width: 100%; inset: 0px; color: transparent;"></div></div></div></a><a class="_container_1g8hs_5 _variantOutlined_1g8hs_65" href="/carriers/lso-guide"><div class="_area_1g8hs_23" style="--ezui-c-card-area-padding-xs: var(--ezui-space-0);"><div class="CarrierBox_CarrierBox__4v_GL"><div class="LogoBox_LogoBox__IzArO"><img alt="LSO Logo" loading="lazy" decoding="async" data-nimg="fill" sizes="(max-width: 640px) 50vw, (max-width: 1200px) 20vw" srcset="/carriers/lso-logo.jpg?w=128&amp;q=80 128w, /carriers/lso-logo.jpg?w=256&amp;q=80 256w, /carriers/lso-logo.jpg?w=384&amp;q=80 384w, /carriers/lso-logo.jpg?w=640&amp;q=80 640w, /carriers/lso-logo.jpg?w=750&amp;q=80 750w, /carriers/lso-logo.jpg?w=828&amp;q=80 828w, /carriers/lso-logo.jpg?w=1080&amp;q=80 1080w, /carriers/lso-logo.jpg?w=1200&amp;q=80 1200w, /carriers/lso-logo.jpg?w=1920&amp;q=80 1920w, /carriers/lso-logo.jpg?w=2048&amp;q=80 2048w, /carriers/lso-logo.jpg?w=3840&amp;q=80 3840w" src="/carriers/lso-logo.jpg?w=3840&amp;q=80" style="position: absolute; height: 100%; width: 100%; inset: 0px; color: transparent;"></div></div></div></a><a class="_container_1g8hs_5 _variantOutlined_1g8hs_65" href="/carriers/canpar-guide"><div class="_area_1g8hs_23" style="--ezui-c-card-area-padding-xs: var(--ezui-space-0);"><div class="CarrierBox_CarrierBox__4v_GL"><div class="LogoBox_LogoBox__IzArO"><img alt="Canpar Logo" loading="lazy" decoding="async" data-nimg="fill" sizes="(max-width: 640px) 50vw, (max-width: 1200px) 20vw" srcset="/carriers/canpar-logo.png?w=128&amp;q=80 128w, /carriers/canpar-logo.png?w=256&amp;q=80 256w, /carriers/canpar-logo.png?w=384&amp;q=80 384w, /carriers/canpar-logo.png?w=640&amp;q=80 640w, /carriers/canpar-logo.png?w=750&amp;q=80 750w, /carriers/canpar-logo.png?w=828&amp;q=80 828w, /carriers/canpar-logo.png?w=1080&amp;q=80 1080w, /carriers/canpar-logo.png?w=1200&amp;q=80 1200w, /carriers/canpar-logo.png?w=1920&amp;q=80 1920w, /carriers/canpar-logo.png?w=2048&amp;q=80 2048w, /carriers/canpar-logo.png?w=3840&amp;q=80 3840w" src="/carriers/canpar-logo.png?w=3840&amp;q=80" style="position: absolute; height: 100%; width: 100%; inset: 0px; color: transparent;"></div></div></div></a><a class="_container_1g8hs_5 _variantOutlined_1g8hs_65" href="/carriers/cirro-e-commerce-guide"><div class="_area_1g8hs_23" style="--ezui-c-card-area-padding-xs: var(--ezui-space-0);"><div class="CarrierBox_CarrierBox__4v_GL"><div class="LogoBox_LogoBox__IzArO"><img alt="Cirro E-Commerce Logo" loading="lazy" decoding="async" data-nimg="fill" sizes="(max-width: 640px) 50vw, (max-width: 1200px) 20vw" srcset="/carriers/cirro-e-commerce-logo.svg?w=128&amp;q=80 128w, /carriers/cirro-e-commerce-logo.svg?w=256&amp;q=80 256w, /carriers/cirro-e-commerce-logo.svg?w=384&amp;q=80 384w, /carriers/cirro-e-commerce-logo.svg?w=640&amp;q=80 640w, /carriers/cirro-e-commerce-logo.svg?w=750&amp;q=80 750w, /carriers/cirro-e-commerce-logo.svg?w=828&amp;q=80 828w, /carriers/cirro-e-commerce-logo.svg?w=1080&amp;q=80 1080w, /carriers/cirro-e-commerce-logo.svg?w=1200&amp;q=80 1200w, /carriers/cirro-e-commerce-logo.svg?w=1920&amp;q=80 1920w, /carriers/cirro-e-commerce-logo.svg?w=2048&amp;q=80 2048w, /carriers/cirro-e-commerce-logo.svg?w=3840&amp;q=80 3840w" src="/carriers/cirro-e-commerce-logo.svg?w=3840&amp;q=80" style="position: absolute; height: 100%; width: 100%; inset: 0px; color: transparent;"></div></div></div></a><a class="_container_1g8hs_5 _variantOutlined_1g8hs_65" href="/carriers/firstmile-guide"><div class="_area_1g8hs_23" style="--ezui-c-card-area-padding-xs: var(--ezui-space-0);"><div class="CarrierBox_CarrierBox__4v_GL"><div class="LogoBox_LogoBox__IzArO"><img alt="FirstMile Logo" loading="lazy" decoding="async" data-nimg="fill" sizes="(max-width: 640px) 50vw, (max-width: 1200px) 20vw" srcset="/carriers/firstmile-logo.png?w=128&amp;q=80 128w, /carriers/firstmile-logo.png?w=256&amp;q=80 256w, /carriers/firstmile-logo.png?w=384&amp;q=80 384w, /carriers/firstmile-logo.png?w=640&amp;q=80 640w, /carriers/firstmile-logo.png?w=750&amp;q=80 750w, /carriers/firstmile-logo.png?w=828&amp;q=80 828w, /carriers/firstmile-logo.png?w=1080&amp;q=80 1080w, /carriers/firstmile-logo.png?w=1200&amp;q=80 1200w, /carriers/firstmile-logo.png?w=1920&amp;q=80 1920w, /carriers/firstmile-logo.png?w=2048&amp;q=80 2048w, /carriers/firstmile-logo.png?w=3840&amp;q=80 3840w" src="/carriers/firstmile-logo.png?w=3840&amp;q=80" style="position: absolute; height: 100%; width: 100%; inset: 0px; color: transparent;"></div></div></div></a></div>
`}</HTMLBlock>

<br />
