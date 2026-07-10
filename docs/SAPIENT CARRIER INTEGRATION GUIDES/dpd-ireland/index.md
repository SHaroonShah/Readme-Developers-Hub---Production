---
title: DPD Ireland (IE)
excerpt: >-
  DPD Ireland is the branch of DPD operating in Ireland, and is part of the
  GeoPost group.
deprecated: false
hidden: true
icon: fad fa-truck-fast
metadata:
  robots: index
---

<Image src="https://files.readme.io/5f844af2d7884698a45f3d8af806874028f7a16f36a6ce86bb9e28ee4e83363c-DPD_IE_banner_white.png" align="center" width="900px" />


***

The integration of DPD Ireland (IE) into the SAPIENT platform is a significant step in enhancing shipping capabilities. This section discusses the in-scope features of this integration and the services this carrier offers.

<Tabs>
  <Tab title="Key Features">
    <Cards columns={2}>
      <Card title="Shipping Origins" icon="fa-map-marker-alt">
        The integration supports shipping from locations in Ireland (IE) and Northern Ireland (country code GB and postcodes beginning with BT).
      </Card>

      <Card title="Shipping Destinations" icon="fa-solid fa-globe">
        The integration supports domestic shipments within Ireland and international shipments to Great Britain (GB), Europe (EU), and Rest of the World (<Glossary>ROW</Glossary>) destinations.
      </Card>

      <Card title="Service Type" icon="fa-solid fa-shipping-fast">
        The integration is focused on outbound shipping.
      </Card>

      <Card title="Incoterms Support" icon="fa-solid fa-file-contract">
        The integration supports <Glossary>DAP</Glossary> and <Glossary>DDP</Glossary> incoterms.
      </Card>

      <Card title="Label Formats" icon="fa-solid fa-tag">
        The integration supports labels in the <Glossary>PDF</Glossary> and <Glossary>PNG</Glossary> formats.
      </Card>
    </Cards>

    <br />
  </Tab>

  <Tab title="Additional Features">
    <Cards columns={2}>
      <Card title="Consignment services" icon="fa-solid fa-boxes-stacked">
        Multi-piece shipments are supported for all services except DPD Air Express.

        > _For Domestic and DPD Classic services, the maximum number of packages allowed is 10, and for DPD Air Express, it is 1._
      </Card>

      <Card title="Delivery instructions" icon="fa-solid fa-clipboard-list">
        Provide special instructions related to the delivery of the shipment. This may involve guidance on how the package should be handled or specific requests regarding the delivery location, such as leaving the shipment at the back door or delivering it to a neighbour to sign.
      </Card>

      <Card title="Safe place location" icon="fa-solid fa-location-dot">
        Provide details of the safe place location for the shipment. This field is mandatory if the **DeliverToSafeplace** service enhancement is used.
      </Card>
    </Cards>
  </Tab>

  <Tab title="Service Enhancements">
    The following are the key service enhancements provided by the DPD Ireland integration:

    * **Email Notification**: Delivery updates are sent via email. To use this enhancement code, the destination **ContactEmail** must be provided with a valid email address.
    * **SMS Notification**: Delivery updates are sent via SMS. To use this enhancement code, the destination **ContactPhone** field must be specified with a valid phone number.
    * **Delivery options**: DPD IE provides the following delivery options:
      * **DelivertoNeighbour**: Allows the delivery to be left with a nearby neighbour if the recipient is not available.
      * **DelivertoSafeplace**: Allows the delivery to be left in a specified secure location at the delivery address when the recipient is not available. If this enhancement is used, the details of the location must be specified in the **SafeplaceLocation** field captured in the **CarrierSpecifics** block of the Create Shipment request.
      * **DeliverytoLetterbox**: Indicates that the item is small enough to be delivered through the recipient’s letterbox.
    * **ExtraInsurance**: Provides additional coverage for the shipment beyond the standard liability, protecting against loss or damage up to a specified value.
    * **PinOnDelivery**: Requires a secure PIN to be provided at the time of delivery to confirm receipt by the recipient. To use this enhancement code, the destination **ContactPhone** or **ContactEmail** fields must be specified with a valid phone number or email address.

    <Callout icon="💡" theme="default">
      ### *Tip*

      *For more information on the service enhancements and carrier services, refer to the [Get Carrier Services](https://docs.intersoftsapient.net/reference/get_v4-carriers-carriercode-services) API endpoint.*
    </Callout>
  </Tab>

  <Tab title="Carrier Services">
The following key services are provided by the DPD Ireland integration.

| Service Name                  | Description                                                                                                                                                                                                           |
| :---------------------------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **DPD Saturday Delivery**     | This service provides weekend delivery of parcels on Saturdays, enabling businesses and recipients to receive shipments outside standard weekday delivery schedules.                                                  |
| **DPD Next Day**              | This service provides fast, next-working-day delivery within Ireland and selected regions, ensuring parcels arrive quickly with reliable transit times and full tracking visibility.                                  |
| **DPD Air Express**           | This service provides urgent international delivery via an established air network, offering next-day delivery to many destinations and worldwide coverage to over 200 countries with full tracking.                  |
| **DPD Classic**               | This service provides reliable, cost-effective road-based parcel delivery across Ireland and Europe, offering fast standard transit times, full tracking, and high-volume shipping capabilities.                      |
| **DPD Classic International** | This service provides international parcel delivery through DPD’s road and air network, combining competitive pricing with reliable transit times, full tracking, and coverage across Europe and global destinations. |
<br />

<Callout icon="💡" theme="default">
  ### _Tip_

  _For the most up-to-date carrier services, use the [Get Carrier Services](https://docs.intersoftsapient.net/reference/get_v4-carriers-carriercode-services) endpoint._
</Callout>
</Tab>
</Tabs>

***

## API Services

<Tabs>
  <Tab title="Core Services">
    <Accordion title="Create Shipment">
      The integration for creating shipments to reflect DPD Ireland as a primary carrier and allowing users to create shipments using the **Create Shipment** endpoint, which returns the label in base64-encoded format.
    </Accordion>

    <br />

    <Accordion title="Manifest Shipment">
      Keep track of shipments and their statuses by receiving real-time updates or notifications whenever specific events occur in the system, such as shipping updates and status changes, via the SAPIENT Manifest Webhook feature.
    </Accordion>
  </Tab>

  <Tab title="Other Services">
    <Accordion title="Tracking">
      Enables customers to receive tracking updates through their integration with the SAPIENT tracking webhook.
    </Accordion>

  <br />

 <Accordion title="Print Label">
      Generate and return the label for a DHL Germany shipment in the supported label formats. This endpoint must be utilised when the label is not generated in the DHL Germany Create Shipment request.

      > 📘 *Note*
      >
      > *This endpoint changes the status of the shipment to label printed. This endpoint should be called at the time of actual printing or label creation, depending on how your business operates. Shipments must be updated to label printed status prior to manifesting.*
    </Accordion>

  </Tab>
</Tabs>

***

## Getting Started

<Tabs>
  <Tab title="Account Setup">
    <Cards columns={3}>
      <Card title="Add DPD Ireland Shipping Account" icon="fa-solid fa-truck" href="https://docs.intersoftsapient.net/docs/add-dpd-ireland-shipping-account">
        Set up your DPD Ireland shipping account to start creating shipments.
      </Card>

      <Card title="Add DPD Ireland Tracking Account" icon="fa-solid fa-search-location" href="https://docs.intersoftsapient.net/docs/add-dpd-ireland-tracking-account">
        Configure tracking for your DPD Ireland shipments.
      </Card>
    </Cards>
  </Tab>

  <Tab title="API References">
    <Cards columns={2}>
      <Card title="Get Carrier Services" icon="fa-solid fa-code" href="https://docs.intersoftsapient.net/reference/get_v4-carriers-carriercode-services">
        Explore the available DPD Ireland carrier services and service enhancements.
      </Card>
    </Cards>
  </Tab>
</Tabs>

<Banner isInline={true} message="Ready to integrate?" color="#ffb600" textColor="#ffffff" fontSize="20px" fontWeight="bold" width="120px" />

<Cards columns={0}>
  <Card title="Activate this integration" href="https://docs.intersoftsapient.net/docs/integration-activation#/" icon="fa-solid fa-circle-play fa-beat" target="_blank">
    Connect with DPD Ireland and manage your shipping operations from a single platform.
  </Card>
</Cards>

<br />
