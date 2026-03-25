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
        ThThe integration supports shipping from locations in Great Britain (GB) only.
      </Card>

      <Card title="Shipping Destinations" icon="fa-solid fa-globe">
        Users can send shipments to Great Britain (GB), Europe, and the <Glossary>ROW</Glossary> (Rest of the World).
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
    * **Consignment services**: Consignment services are supported, and DPD UK allows a maximum of 99 packages per consignment.

    > 📘 *Note*
    >
    > *Please bear in mind that not all services offer consignment options.*

    * **Carrier-Specific Fields**: The **CarrierSpecifics** object in the **Create Shipment** request contains the following fields:

      * **DeliveryInstructions**: To provide any additional instructions to the carrier regarding the delivery of the shipment
  </Tab>

  <Tab title="Service Enhancements">
    <Cards columns={2}>
      <Card title="Proof of Identity" icon="fa-solid fa-ID">
        Requires the receiver to present valid identification at the point of delivery.
      </Card>

      <Card title="Proof of Age" icon="fa-solid fa-age">
        Ensures the recipient meets a minimum age requirement, like for age-restricted goods.
      </Card>

      <Card title="Pin Required" icon="fa-solid fa-location-pin-lock">
        A secure PIN is sent to the receiver, which must be provided upon delivery.
      </Card>

      <Card title="Pin Required & Proof of Age" icon="fa-solid fa-location-pin-lock">
        Requires PIN and age verification at the point of delivery for added security.
      </Card>
    </Cards>

    <Callout icon="💡" theme="default">
      ### *Tip*

      *For more information on the service enhancements and carrier services, refer to the following endpoints:*

      * [Create Shipment](https://docs.intersoftsapient.net/reference/post_v4-shipments-dpduk)
      * [Get Carrier Services](https://docs.intersoftsapient.net/reference/get_v4-carriers-carriercode-services)
    </Callout>
  </Tab>
</Tabs>

***

## API Services

<Tabs>
  <Tab title="Core Services">
    <Accordion title="Create Shipment" icon="plus-circle">
      The integration for creating shipments to reflect DPD UK as a primary carrier and allowing users to create shipments using the **Create Shipment** endpoint.
<Callout icon="💡" theme="default">
  ### _Tip_

  _For more information on the API endpoint, refer to the [Create Shipment](https://docs.intersoftsapient.net/reference/post_v4-shipments-dpduk)endpoint._

</Callout>

    </Accordion>

    <br />
  </Tab>

  <Tab title="Advanced Services">
    <Accordion title="Print Label" icon="print">
      Generate and return the label for an An Post shipment. This endpoint must be utilised when the label is not generated in the An Post Create Shipment request.

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

The following API services are provided by the DPD UK integration:

* **Label integration**: The system generates the label by populating a stored label template with the relevant shipment data.
* **Manifest integration**: A crucial API for DPD UK that generates an electronic manifest data file in the SAPIENT's default PDF format and send it to DPD UK via SFTP.
* **Tracking integration**: Enables data files to be sent via SFTP and received through the SAPIENT tracking webhook.

***

In this section, learn now to:

* <Anchor label="Add a DPD UK shipping account" target="_blank" href="https://docs.intersoftsapient.net/docs/add-dpd-uk-shipping-account">Add a DPD UK shipping account</Anchor>
* <Anchor label="Add a DPD UK tracking account" target="_blank" href="https://docs.intersoftsapient.net/docs/add-dpd-uk-tracking-account">Add a DPD UK tracking account</Anchor>

> 📘 _Note_
>
> _For more information on how to activate the DPD UK integration, refer to the [Activate integration](https://docs.intersoftsapient.net/docs/integration-activation#/) section._
