---
title: Royal Mail
excerpt: >-
  Royal Mail is a leading British postal service and courier company. It
  provides a wide range of services, including standard and express mail
  delivery, parcel distribution, logistics, and international shipping.
deprecated: false
hidden: false
link:
  new_tab: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  pages:
    - slug: shipping-account-requirements
      title: Royal Mail shipping account setup
      type: basic
---
<Image align="center" border={false} width="120px" src="https://files.readme.io/a9ee760d85555af384cfd0575c7bc99d51a1aada6dec34c8bfb588907ccd9422-RM_favicon.png" />

<Banner isInline={true} message="Ready to integrate?" color="#ffb600" textColor="#ffffff" fontSize="20px" fontWeight="bold" width="120px" Imagesrc="https://files.readme.io/a9ee760d85555af384cfd0575c7bc99d51a1aada6dec34c8bfb588907ccd9422-RM_favicon.png" />

***

The Royal Mail-SAPIENT integration aims to enhance operational efficiency and provide users with tailored shipping options. By leveraging Royal Mail's extensive capabilities, businesses can ensure a streamlined shipping process that meets diverse logistical needs.

This integration represents a significant step towards optimising shipping functions within SAPIENT, offering comprehensive coverage from Great Britain to Europe and the Rest of the World.

## Overview

<Tabs>
  <Tab title="Key Features">
    <Cards columns={2}>
      <Card title="Shipping Origins" icon="fa-solid fa-map-marker-alt">
        The integration supports shipping from locations in Great Britain (GB) only.
      </Card>

      <Card title="Global Destinations" icon="fa-solid fa-globe">
        Users can send <Glossary>shipments</Glossary> to Europe and the <Glossary>ROW</Glossary> (Rest of the World).
      </Card>

      <Card title="Service Type" icon="fa-solid fa-shipping-fast">
        The integration is focused on inbound and outbound shipping.
      </Card>

      <Card title="Incoterms Support" icon="fa-solid fa-file-contract">
        The integration supports <Glossary>DDU</Glossary>, <Glossary>DDP</Glossary>, <Glossary>DAP</Glossary>, and <Glossary>DAT</Glossary>.
      </Card>
    </Cards>
  </Tab>

  <Tab title="Additional Features">
    <Cards columns={2}>
      <Card title="Single Piece shipments" icon="fa-solid fa-box">
        Support for single shipments is included in the integration, allowing users to send single shipment. However, users can create multiple single shipments via a single API call.
      </Card>

      <Card title="Package Types" icon="fa-solid fa-boxes">
        Royal Mail offers its own distinct <Glossary>package type</Glossary>s, such as Letter, Large letter, Parcel, and Printed papers. You can look up package types by calling the [Get Carrier Service Package Types](https://docs.intersoftsapient.net/reference/get_v4-carriers-carriercode-services-servicecode-packagetypes#/) endpoint.
      </Card>
    </Cards>
  </Tab>

  <Tab title="Service Enhancements">
    <Accordion title="Consequential Loss Coverage" icon="shield-alt">
      Royal Mail offers multiple tiers of consequential loss coverage to protect your shipments:

      * **CL1** - Consequential Loss £1000: Coverage for losses up to £1000.
      * **CL2** - Consequential Loss £2500: Coverage for losses up to £2500.
      * **CL3** - Consequential Loss £5000: Coverage for losses up to £5000.
      * **CL4** - Consequential Loss £7500: Coverage for losses up to £7500.
      * **CL5** - Consequential Loss £10000: Coverage for losses up to £10000
    </Accordion>

    <br />

    <Accordion title="Delivery Options & Notifications" icon="bell">
      Enhanced delivery and notification services:

      * **Signed**: A signature is required upon delivery, applicable to 24, 48, 1st Class, and 2nd Class services.
      * **SMS**: Provides delivery updates via SMS for Special Delivery Guaranteed, Tracked, and Tracked High Volume services.
      * **Email**: Sends delivery updates via email for eligible services, such as Special Delivery Guaranteed, Tracked and Tracked High Volume, International Tracked and International Tracked and Signed services.
      * **Safeplace**: The shipment will be left in a specified safe place location; details must be provided in the SafeplaceLocation field. Can be used with Tracked, Tracked High Volume and 24/48 services.
      * **LocalCollect**: The shipment will be delivered to a Post Office for collection by the receiver. Can be used with Special Delivery Guaranteed, Tracked and Tracked High Volume services.
    </Accordion>

    <br />

    <Accordion title="International Services" icon="plane">
      Additional enhancements for international shipments:

      * **CustomsEmail**: The receiver's email address will be included in eCustoms data. This enhancement code can be used with international services.
      * **CustomsPhone**: The receiver's phone number will be included in eCustoms data. This enhancement code can be used with international services.
    </Accordion>
  </Tab>
</Tabs>

***

## API Services

<Tabs>
  <Tab title="Core Services">
    <Accordion title="Create Shipment" icon="plus-circle">
      The integration for creating shipments to reflect Royal Mail as a primary carrier and allowing users to create shipments using the **Create Shipment** endpoint.
    </Accordion>

    <br />

    <Accordion title="Print Label" icon="print">
      Generate and return the label for the Royal Mail shipment. This endpoint is utilised after a Royal Mail shipment has been created and is meant to facilitate the printing of the label required for that shipment.

      > 📘 *Note*
      >
      > *This endpoint changes the status of the shipment to label printed. This endpoint should be called at the time of actual printing or label creation, depending on how your business operates. Shipments must be updated to label printed status prior to manifesting.*
    </Accordion>

    <br />

    <Accordion title="Print My Label QR Code" icon="qrcode">
      Generate an easy-to-scan QR code for the associated label specified in the **PrintLabel** API endpoint. This endpoint can only be used for Royal Mail Tracked Return services.
    </Accordion>

    <br />

    <Accordion title="Pre Allocate Tracking Number" icon="hashtag">
      Receive a Royal Mail Tracking Number that will be pre-allocated to the service and destination supplied in the request. No shipment or label will be produced using this endpoint. This endpoint can only be used for services that are assigned a tracking number.
    </Accordion>
  </Tab>

  <Tab title="Advanced Services">
    <Accordion title="Offline Barcoding" icon="barcode">
      Request a specific range of barcodes for use in your shipping processes. Offline Barcoding is only available if it has been activated on your customer account in the GUI.
    </Accordion>

    <br />

    <Accordion title="PUDO Locations" icon="map-marked-alt">
      Retrieves a list of Pick-Up and Drop-Off (PUDO) locations associated with a specified carriers that are within a set radius of the postcode provided in the request. That radius is set to 10 Miles / 16.09 Kilometres.

      > 🚧 *Important*
      >
      > *This endpoint must be called before the**Create Shipment** endpoint so that the desired PUDO location is selected in the Create Shipment request.*
    </Accordion>

    <br />

    <Accordion title="International Arrivals Containers" icon="container-storage">
      Create and name (with and ID or alias) a new international arrivals container to be used for manifesting a specific group of shipments. Define which carrier and shipping location the container should be linked to.

      Unlike the common [Containers](https://docs.intersoftsapient.net/reference/get_v4-containers#/) API, the **International Arrivals Containers** endpoint is used for Royal Mail shipments that are being imported into GB only. For shipments in these containers, a <Glossary>data solution</Glossary> file is generated and sent to Royal Mail, which allows them to associate the shipments in the container with its associated ID, for better tracking and visibility purposes.
    </Accordion>
  </Tab>
</Tabs>

***

## Getting Started

<Tabs>
  <Tab title="Account Setup">
    <Cards columns={3}>
      <Card title="Account Setup" href="https://docs.intersoftsapient.net/docs/oba-email-validation" icon="fa-solid fa-user-plus">
        Access the step-by-step guide on how to set up Royal Mail Online Business Account (OBA).
      </Card>

      <Card title="Shipping Account" href="https://docs.intersoftsapient.net/docs/shipping-account-requirements" icon="fa-solid fa-truck">
        Access the step-by-step guide on how to set up Royal Mail shipping account on SAPIENT.
      </Card>

      <Card title="Tracking Account" href="https://docs.intersoftsapient.net/docs/royal-mail-tracking-account-setup" icon="fa-solid fa-search-location">
        Access the step-by-step guide on how to set up Royal Mail tracking account on SAPIENT.
      </Card>
    </Cards>
  </Tab>

  <Tab title="Shipment Services">
    <Cards columns={3}>
      <Card title="BFPO Shipments" href="https://docs.intersoftsapient.net/docs/bfpo-shipments" icon="fa-solid fa-person-military-rifle">
        Create BFPO shipments and send them to British military personnel, their families, and official organisations stationed abroad or in remote locations.
      </Card>

      <Card title="Return Shipments" href="https://docs.intersoftsapient.net/docs/royal-mail-returns" icon="fa-solid fa-undo">
        Send your items back with the Royal Mail hassle-free returns service.
      </Card>

      <Card title="Pre-allocated Tracking" href="https://docs.intersoftsapient.net/docs/use-the-royal-mail-pre-allocated-tracking-number" icon="fa-solid fa-input-numeric">
        Get the pre-allocated tracking number in advance for a shipment or order before despaching.
      </Card>
    </Cards>
  </Tab>

  <Tab title="Advanced Features">
    <Cards columns={3}>
      <Card title="Collection Service" href="https://docs.intersoftsapient.net/docs/royal-mail-parcel-collect" icon="fa-solid fa-hand-holding-box">
        Use the collection service to have your returns collected from your homes.
      </Card>

      <Card title="PUDO Service" href="https://docs.intersoftsapient.net/docs/use-local-collect-shipment-service#/" icon="fa-solid fa-store">
        Use the Royal Mail pick up and drop-off services for a conveninent out-of-home collection or return of your items.
      </Card>

      <Card title="International Containers" href="https://docs.intersoftsapient.net/docs/add-barcode-range-for-international-arrival-containers" icon="fa-solid fa-globe-americas">
        Generate a barcode range for your international arrivals containers to track the containers arriving in the UK.
      </Card>
    </Cards>
  </Tab>
</Tabs>

<Banner isInline={true} message="Ready to integrate?" color="#ffb600" textColor="#ffffff" fontSize="20px" fontWeight="bold" width="120px" />

<Cards>
  <Card title="Activate this integration" href="https://docs.intersoftsapient.net/docs/integration-activation#/" icon="fa-solid fa-circle-play" target="_blank">
    Seamlessly connect with Royal Mail and manage your shipping operations from a single platform.
  </Card>
</Cards>

<br />
