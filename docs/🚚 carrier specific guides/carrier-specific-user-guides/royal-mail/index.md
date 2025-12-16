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

***

<Columns layout="auto">
  <Column>
    The Royal Mail-SAPIENT integration aims to enhance operational efficiency and provide users with tailored shipping options. By leveraging Royal Mail's extensive capabilities, businesses can ensure a streamlined shipping process that meets diverse logistical needs.
  </Column>
  <Column>
    This integration represents a significant step towards optimising shipping functions within SAPIENT, offering comprehensive coverage from Great Britain to Europe and the Rest of the World.
  </Column>
</Columns>

## Overview

<Tabs>
  <Tab title="Core Features">
    <Cards columns={2}>
      <Card title="Shipping Origins" icon="map-marker-alt">
        **Ship from destinations**: The integration supports shipping from locations in Great Britain (GB) only.
      </Card>
      <Card title="Global Destinations" icon="globe">
        **Ship To Destinations**: Users can send <Glossary>shipments</Glossary> to Europe and the <Glossary>ROW</Glossary> (Rest of the World).
      </Card>
      <Card title="Service Type" icon="shipping-fast">
        **Service Type**: The integration is focused on inbound and outbound shipping.
      </Card>
      <Card title="Incoterms Support" icon="file-contract">
        **Incoterms**: The integration supports <Glossary>DDU</Glossary>, <Glossary>DDP</Glossary>, <Glossary>DAP</Glossary>, and <Glossary>DAT</Glossary>.
      </Card>
    </Cards>
  </Tab>
  <Tab title="Advanced Capabilities">
    <Cards columns={2}>
      <Card title="Multipiece Shipments" icon="boxes">
        Support for multipiece shipments is included in the integration, allowing you to send multiple packages as a single shipment.
      </Card>
      <Card title="Package Types" icon="package">
        Royal Mail offers its own distinct <Glossary>package type</Glossary>s, such as Letter, Large letter, Parcel, and Printed papers. You can look up package types by calling the [Get Carrier Service Package Types](https://docs.intersoftsapient.net/reference/get_v4-carriers-carriercode-services-servicecode-packagetypes#/) endpoint.
      </Card>
      <Card title="Return Services" icon="undo">
        Comprehensive return shipment capabilities with QR code generation for easy scanning and processing.
      </Card>
      <Card title="International Support" icon="plane">
        Full support for international shipping with customs data integration and compliance features.
      </Card>
    </Cards>
  </Tab>
</Tabs>

## Service Enhancements

<Accordion title="Protection & Insurance" icon="shield-alt">
  <Cards columns={3}>
    <Card title="CL1 Coverage" icon="shield">
      **Consequential Loss £1000**: Coverage for losses up to £1000.
    </Card>
    <Card title="CL2 Coverage" icon="shield">
      **Consequential Loss £2500**: Coverage for losses up to £2500.
    </Card>
    <Card title="CL3 Coverage" icon="shield">
      **Consequential Loss £5000**: Coverage for losses up to £5000.
    </Card>
    <Card title="CL4 Coverage" icon="shield">
      **Consequential Loss £7500**: Coverage for losses up to £7500.
    </Card>
    <Card title="CL5 Coverage" icon="shield">
      **Consequential Loss £10000**: Coverage for losses up to £10000.
    </Card>
  </Cards>
</Accordion>

<Accordion title="Delivery & Notification Services" icon="bell">
  <Tabs>
    <Tab title="Delivery Options">
      <Cards columns={2}>
        <Card title="Signed Delivery" icon="signature">
          **Signed**: A signature is required upon delivery, applicable to 24, 48, 1st Class, and 2nd Class services.
        </Card>
        <Card title="Safeplace Delivery" icon="home">
          **Safeplace**: The shipment will be left in a specified safe place location; details must be provided in the SafeplaceLocation field. Can be used with Tracked, Tracked High Volume and 24/48 services.
        </Card>
        <Card title="Local Collection" icon="store">
          **LocalCollect**: The shipment will be delivered to a Post Office for collection by the receiver. Can be used with Special Delivery Guaranteed, Tracked and Tracked High Volume services.
        </Card>
      </Cards>
    </Tab>
    <Tab title="Notifications">
      <Cards columns={2}>
        <Card title="SMS Updates" icon="mobile-alt">
          **SMS**: Provides delivery updates via SMS for Special Delivery Guaranteed, Tracked, and Tracked High Volume services.
        </Card>
        <Card title="Email Updates" icon="envelope">
          **Email**: Sends delivery updates via email for eligible services, such as Special Delivery Guaranteed, Tracked and Tracked High Volume, International Tracked and International Tracked and Signed services.
        </Card>
      </Cards>
    </Tab>
  </Tabs>
</Accordion>

<Accordion title="International Services" icon="globe">
  <Cards columns={2}>
    <Card title="Customs Email Integration" icon="envelope-open-text">
      **CustomsEmail**: The receiver's email address will be included in eCustoms data. This enhancement code can be used with international services.
    </Card>
    <Card title="Customs Phone Integration" icon="phone">
      **CustomsPhone**: The receiver's phone number will be included in eCustoms data. This enhancement code can be used with international services.
    </Card>
  </Cards>
</Accordion>

## API Services & Endpoints

<Tabs>
  <Tab title="Essential Services">
    <Cards columns={2}>
      <Card title="Create Shipment" icon="plus-circle">
        The integration for creating shipments to reflect Royal Mail as a primary carrier and allowing users to create shipments using the **Create Shipment** endpoint.
      </Card>
      <Card title="Print Label" icon="print">
        Generate and return the label for the Royal Mail shipment. This endpoint is utilised after a Royal Mail shipment has been created and is meant to facilitate the printing of the label required for that shipment.
        
        > 📘 _Note_: This endpoint changes the status of the shipment to label printed. This endpoint should be called at the time of actual printing or label creation, depending on how your business operates. Shipments must be updated to label printed status prior to manifesting.
      </Card>
    </Cards>
  </Tab>
  <Tab title="Tracking & Labels">
    <Cards columns={2}>
      <Card title="QR Code Generation" icon="qrcode">
        **Print My Label QR Code**: Generate an easy-to-scan QR code for the associated label specified in the **PrintLabel** API endpoint. This endpoint can only be used for Royal Mail Tracked Return services.
      </Card>
      <Card title="Pre-allocated Tracking" icon="hashtag">
        **Pre Allocate Tracking Number**: Receive a Royal Mail Tracking Number that will be pre-allocated to the service and destination supplied in the request. No shipment or label will be produced using this endpoint. This endpoint can only be used for services that are assigned a tracking number.
      </Card>
    </Cards>
  </Tab>
  <Tab title="Advanced Features">
    <Cards columns={2}>
      <Card title="Offline Barcoding" icon="barcode">
        **Offline Barcoding**: Request a specific range of barcodes for use in your shipping processes. Offline Barcoding is only available if it has been activated on your customer account in the GUI.
      </Card>
      <Card title="PUDO Locations" icon="map-marked-alt">
        **PUDO Locations**: Retrieves a list of Pick-Up and Drop-Off (PUDO) locations associated with a specified carriers that are within a set radius of the postcode provided in the request. That radius is set to 10 Miles / 16.09 Kilometres.
        
        > 🚧 _Important_: This endpoint must be called before the **Create Shipment** endpoint so that the desired PUDO location is selected in the Create Shipment request.
      </Card>
    </Cards>

    <Accordion title="International Arrivals Containers" icon="container-storage">
      <Cards columns={1}>
        <Card title="Container Management" icon="boxes">
          Create and name (with and ID or alias) a new international arrivals container to be used for manifesting a specific group of shipments. Define which carrier and shipping location the container should be linked to.

          Unlike the common [Containers](https://docs.intersoftsapient.net/reference/get_v4-containers#/) API, the **International Arrivals Containers** endpoint is used for Royal Mail shipments that are being imported into GB only. For shipments in these containers, a <Glossary>data solution</Glossary> file is generated and sent to Royal Mail, which allows them to associate the shipments in the container with its associated ID, for better tracking and visibility purposes.
        </Card>
      </Cards>
    </Accordion>
  </Tab>
</Tabs>

## Getting Started

<Accordion title="Account Configuration" icon="user-cog">
  <Tabs>
    <Tab title="Basic Setup">
      <Cards columns={3}>
        <Card title="OBA Setup" href="https://docs.intersoftsapient.net/docs/oba-email-validation" icon="user-plus">
          **Online Business Account**: Set up Royal Mail Online Business Account (OBA) for account management and validation.
        </Card>
        <Card title="Shipping Account" href="https://docs.intersoftsapient.net/docs/shipping-account-requirements" icon="truck">
          **Shipping Configuration**: Configure your Royal Mail shipping account with proper credentials and settings.
        </Card>
        <Card title="Tracking Setup" href="https://docs.intersoftsapient.net/docs/royal-mail-tracking-account-setup" icon="search-location">
          **Tracking Integration**: Set up Royal Mail tracking account for shipment visibility and monitoring.
        </Card>
      </Cards>
    </Tab>
    <Tab title="Integration Activation">
      <Cards columns={1}>
        <Card title="Activate Integration" href="https://docs.intersoftsapient.net/docs/integration-activation#/" icon="power-off">
          **Enable Royal Mail Services**: For detailed information on how to activate the Royal Mail integration within your SAPIENT environment, refer to the comprehensive integration activation guide.
        </Card>
      </Cards>
    </Tab>
  </Tabs>
</Accordion>

<Accordion title="Shipment Services" icon="shipping-fast">
  <Tabs>
    <Tab title="Standard Services">
      <Cards columns={3}>
        <Card title="BFPO Shipments" href="https://docs.intersoftsapient.net/docs/bfpo-shipments" icon="flag">
          **Military Shipments**: Create and manage British Forces Post Office (BFPO) shipments for military personnel and operations.
        </Card>
        <Card title="Return Shipments" href="https://docs.intersoftsapient.net/docs/royal-mail-returns" icon="undo">
          **Returns Management**: Configure and process return shipments with automated label generation and tracking.
        </Card>
        <Card title="Pre-allocated Tracking" href="https://docs.intersoftsapient.net/docs/use-the-royal-mail-pre-allocated-tracking-number" icon="number">
          **Tracking Numbers**: Utilize pre-allocated tracking numbers for improved shipment planning and inventory management.
        </Card>
      </Cards>
    </Tab>
    <Tab title="Premium Services">
      <Cards columns={3}>
        <Card title="Collection Service" href="https://docs.intersoftsapient.net/docs/royal-mail-parcel-collect" icon="hand-holding-box">
          **Parcel Collection**: Schedule and manage Royal Mail collection services for outbound shipments from your location.
        </Card>
        <Card title="PUDO Service" href="https://docs.intersoftsapient.net/docs/use-local-collect-shipment-service#/" icon="store">
          **Pick-Up Drop-Off**: Utilize Royal Mail's network of PUDO locations for flexible delivery and collection options.
        </Card>
        <Card title="International Containers" href="https://docs.intersoftsapient.net/docs/add-barcode-range-for-international-arrival-containers" icon="globe-americas">
          **Container Management**: Set up and manage international arrival containers for bulk shipment processing and tracking.
        </Card>
      </Cards>
    </Tab>
  </Tabs>
</Accordion>

<Accordion title="Quick Start Checklist" icon="tasks">
  <Cards columns={2}>
    <Card title="Pre-Integration Steps" icon="clipboard-list">
      1. **Account Setup**: Complete Royal Mail OBA registration
      2. **Credentials**: Obtain API credentials and access tokens
      3. **Testing Environment**: Set up sandbox/testing environment
      4. **Documentation Review**: Familiarize yourself with API endpoints
    </Card>
    <Card title="Post-Integration Steps" icon="check-circle">
      1. **Service Configuration**: Configure desired shipping services
      2. **Enhancement Setup**: Enable required enhancements (SMS, Email, etc.)
      3. **Testing**: Create test shipments to validate integration
      4. **Production Deployment**: Move to live environment after testing
    </Card>
  </Cards>
</Accordion>