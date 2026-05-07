---
title: EVRi
excerpt: >-
  _EVRi_ is a logistics and parcel delivery service provider that operates
  primarily in the UK. EVRi offers a wide range of delivery options, including
  standard, next-day, and scheduled deliveries, catering to both business and
  residential customers.
deprecated: false
hidden: false
icon: fad fa-truck-fast
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
  pages:
    - type: basic
      slug: shipping-account-setup-3
      title: Evri shipping account setup
---
<Image align="center" width="900px" src="https://files.readme.io/01dc0d3b7707e7095a26e08e874ca4fb1b7f2f82ba588e5d1c119b8f20e5e9c9-EVRi_white_banner.png" />

***

The EVRi integration into the SAPIENT platform enhances our shipping capabilities by enabling users to seamlessly manage their shipments through Evri's robust delivery network. Customers can now access Evri's comprehensive suite of services, including real-time tracking, flexible delivery options, and efficient returns management, all within the familiar SAPIENT interface. This enhancement aims to streamline the shipping process, improve operational efficiency, and provide a better overall experience for our users.

## Overview

<Tabs>
  <Tab title="Key Features">
    <Cards columns={2}>
      <Card title="Shipping Origins" icon="fa-map-marker-alt">
        The integration supports shipping from locations in Great Britain (GB) only.
      </Card>

      <Card title="Shipping Destinations" icon="fa-solid fa-globe">
        Users can send shipments to Great Britain (GB), Europe, and <Glossary>ROW</Glossary> (Rest of the World).
      </Card>

      <Card title="Service Type" icon="fa-solid fa-shipping-fast">
        The integration is focused on outbound shipping and inbound shipping services.
      </Card>

      <Card title="Incoterms Support" icon="fa-solid fa-file-contract">
        The integration only supports <Glossary>DDU</Glossary>incoterm.
      </Card>

      <Card title="Label Formats" icon="fa-solid fa-tag">
        The intergration supports label in the <Glossary>PDF</Glossary> and <Glossary>PNG</Glossary> formats.<br />
      </Card>
    </Cards>

    > 📘 *Note*
    >
    > *QR code generation is supported for the returns shipments only.*

    <br />
  </Tab>

  <Tab title="Additional Features">
    <Cards columns={1}>
      <Card title="Single Piece Shipments" icon="fa-solid fa-box">
        All services in this integration support only single-package services. Which means, only one package can be sent per request. Consignment services are not supported in the this integration.
      </Card>

      <Card title="Carrier-specific Fields " icon="fa-solid fa-truck">
        The **CarrierSpecifics** object in the Create Shipment request contains the following fields:

        * **SpecialInstruction1**: To provide special instructions or requests to the carrier for handling the shipment, such as handling procedures or delivery preferences.
        * **SpecialInstruction2**: To provide additional specific instructions concerning the shipment handling that Evri should be aware of.
      </Card>
    </Cards>
  </Tab>

  <Tab title="Service Enhancements">
    <Cards columns={2}>
      <Card title="Signed" icon="fa-solid fa-signature">
        A signature is required upon delivery for verification of your shipment.
      </Card>

      <Card title="SMS" icon="fa-solid fa-phone">
        Requires a contact number to receive delivery updates via SMS.
      </Card>
    </Cards>

    <br />

    <Callout icon="💡" theme="default">
      ### *Tip*

      *For more information on the service enhancements and carrier services, refer to the following endpoints:*

      * *[Create Shipment](https://docs.intersoftsapient.net/v4.03/reference/post_v4-shipments-amazon)*
      * *[Get Carrier Services](https://docs.intersoftsapient.net/reference/get_v4-carriers-carriercode-services)*
    </Callout>
  </Tab>
</Tabs>

This integration provides the following key features:

**Ship from destinations**: The integration supports shipping from locations in Great Britain (GB) only.

* **Ship To Destinations**: Users can send <Glossary>shipments</Glossary> to Great Britain (GB), Europe, and the <Glossary>ROW</Glossary> (Rest of the World).
* **Label formats**: The EVRi's label integration support labels in the <Glossary>PDF</Glossary> and <Glossary>PNG</Glossary> formats.
* **Incoterms**: This integration only supports <Glossary>DDU</Glossary>.
* **Service Type**: The integration is focused on outbound and Returns shipping services.

> 📘 _Note_
>
> _QR code generation is supported for the returns shipments._

## Enhancements

The following are the key enhancements provided by the EVRi integration:

* Service enhancements: These services include the following:
  * **Signed**: Requires a signature upon delivery.
  * **SMS**: Requires a contact number to receive delivery updates via SMS.

## Additional features

The EVRi integration provides the following additional features:

* **Single package**: All services in this integration support only single-package services. Which means, only one package can be sent per request.

## Integration types

This integrations supports the following integration types on SAPIENT:

**Label**: Enables delivery routing request to be used for outbound services, and collection routing request for the returns services.

**Tracking**: Enables data files to be sent via SFTP.

***

In this section, learn how to:

* [Add an EVRi shipping account](https://docs.intersoftsapient.net/docs/shipping-account-setup-3)
* [Add an EVRi tracking account](https://docs.intersoftsapient.net/docs/tracking-account-setup)
* [Add a child client department to parent shipping account](https://docs.intersoftsapient.net/docs/client-id-and-child-clinet-id-management-1#/)

> 📘 _Note_
>
> _For more information on how to activate the EVRi integration, refer to the <Anchor label="Activate integration" target="_blank" href="https://docs.intersoftsapient.net/docs/integration-activation#/">Activate integration</Anchor> section._
