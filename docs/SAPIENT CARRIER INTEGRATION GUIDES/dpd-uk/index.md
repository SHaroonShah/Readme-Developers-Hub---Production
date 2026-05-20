---
title: DPD UK
excerpt: "DPD is part of Geopost, one of the world leading parcel delivery networks operating in more than 50 countries.\_"
deprecated: false
hidden: false
icon: fad fa-truck-fast
metadata:
  robots: index
---
<Image align="center" width="900px" src="https://files.readme.io/ec7877a4210f964edd4030c4599be01a423d26d55a53f64019ff4604a52ef069-DPD_white_banner.png" />

***

DPD are one of the leading delivery carriers in the UK, shipping domestically and internationally, offering a range of next-day and timed delivery with our 1-hour delivery window sent to customers via text or email on the morning of delivery, DPD also offer worldwide deliveries.

## Overview

<Tabs>
  <Tab title="Key Features">
    <Cards columns={2}>
      <Card title="Shipping Origins" icon="fa-map-marker-alt">
        The integration supports shipping from locations in Great Britain (GB) only.
      </Card>

      <Card title="Shipping Destinations" icon="fa-solid fa-globe">
        Users can send shipments to Great Britain (GB), Europe, and the Rest of the World (<Glossary>ROW</Glossary>).
      </Card>

      <Card title="Service Type" icon="fa-solid fa-shipping-fast">
        The integration is focused on outbound shipping.
      </Card>

      <Card title="Incoterms Support" icon="fa-solid fa-file-contract">
        The integration supports <Glossary>DAP</Glossary> and <Glossary>DDP</Glossary> incoterms.
      </Card>

      <Card title="Label Formats" icon="fa-solid fa-tag">
        The integration supports labels in the <Glossary>PDF</Glossary> format.
      </Card>
    </Cards>

    <br />
  </Tab>

  <Tab title="Additional Features">
<Cards columns={2}>
<Card title="Consignment Services" icon="fa-cubes">
    The integration supports consignment services, and DPD UK allows a maximum of 99 packages per consignment.
Please bear in mind that not all services offer consignment options.
  </Card>
<Card title="Carrier-Specifics" icon="fa-map-marker-alt">
  The **CarrierSpecifics** object in the **Create Shipment** request contains the **DeliveryInstructions** field to provide any additional instructions to the carrier regarding the delivery of the shipment
  </Card>
</Cards>

  </Tab>

  <Tab title="Service Enhancements">
    <Cards columns={2}>
      <Card title="Proof of Identity" icon="fa-solid fa-id-card">
        Requires the receiver to present valid identification at the point of delivery.
      </Card>

      <Card title="Proof of Age" icon="fa-solid fa-calendar-circle-user">
        Ensures the recipient meets a minimum age requirement, like for age-restricted goods.
      </Card>

      <Card title="Pin Required" icon="fa-solid fa-location-pin-lock">
        A secure PIN is sent to the receiver, which must be provided upon delivery.
      </Card>

      <Card title="Pin Required & Proof of Age" icon="fa-solid fa-location-pin-lock">
        Requires PIN and age verification at the point of delivery for added security.
      </Card>
    </Cards>

    <br />

    <Callout icon="💡" theme="default">
      ### *Tip*

      *For more information on the service enhancements and carrier services, refer to the following endpoints:*

      * *[Create Shipment](https://docs.intersoftsapient.net/reference/post_v4-shipments-dpduk)*
      * *[Get Carrier Services](https://docs.intersoftsapient.net/reference/get_v4-carriers-carriercode-services)*
    </Callout>
  </Tab>
</Tabs>

***

## API Services

<Tabs>
  <Tab title="Core Services">
    <Accordion title="Create Shipment" icon="">
      The integration for creating shipments to reflect DPD UK as a primary carrier and allowing users to create shipments using the **Create Shipment** endpoint.
    </Accordion>

    <br />

    <Accordion title="Manifest" icon="">
      A crucial API for DPD UK that generates an electronic manifest data file in the SAPIENT's default PDF format and send it to DPD UK via SFTP.
    </Accordion>

    <br />
  </Tab>

  <Tab title="Other Services">
    <Accordion title="Print Label" icon="print">
      Generate and return the label for a DPD UK shipment. This endpoint must be utilised when the label is not generated in the DPD UK Create Shipment request.

      > 📘 *Note*
      >
      > *This endpoint changes the status of the shipment to label printed. This endpoint should be called at the time of actual printing or label creation, depending on how your business operates. Shipments must be updated to label printed status prior to manifesting.*
    </Accordion>

    <br />

    <Accordion title="Tracking" icon="print">
      This integration allows customers to monitor their shipments in real-time, providing transparency and peace of mind. Users can access detailed tracking information, including, real-time updates, tracking numbers, and delivery notifications.
    </Accordion>
  </Tab>
</Tabs>

***

## Getting Started

<Tabs>
  <Tab title="Account Setup">
    <Cards columns={2}>
      <Card title="Add DPD UK Shipping Account" icon="fa-solid fa-truck" href="https://docs.intersoftsapient.net/docs/add-dpd-uk-shipping-account">
        Set up your DPD UK shipping account to start creating shipments.
      </Card>

      <Card title="Add DPD UK Tracking Account" icon="fa-solid fa-search-location" href="https://docs.intersoftsapient.net/docs/add-dpd-uk-tracking-account">
        Configure tracking for your DPD UK shipments.
      </Card>
    </Cards>
  </Tab>

  <Tab title="API References">
    <Cards>
      <Card title="SAPIENT DPD UK API" icon="fa-solid fa-code" href="https://docs.intersoftsapient.net/reference/get_v4-shippingaccounts-dpduk">
        Explore the DPD UK API endpoints for a seamless shipping experience.
      </Card>
    </Cards>
  </Tab>
</Tabs>

<Banner isInline={true} message="Ready to integrate?" color="#ffb600" textColor="#ffffff" fontSize="20px" fontWeight="bold" width="120px" />

<Cards columns={0}>
  <Card title="Activate this integration" href="https://docs.intersoftsapient.net/docs/integration-activation#/" icon="fa-solid fa-circle-play fa-beat" target="_blank">
    Seamlessly connect with DPD UK and manage your shipping operations from a single platform.
  </Card>
</Cards>
