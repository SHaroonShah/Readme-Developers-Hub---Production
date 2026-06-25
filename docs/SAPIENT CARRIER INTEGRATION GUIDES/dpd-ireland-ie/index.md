---
title: DPD Ireland (IE)
excerpt: >-
  DPD Ireland is the branch of DPD operating in Ireland, and is part of the
  GeoPost group.
deprecated: false
hidden: false
icon: fad fa-truck-fast
metadata:
  robots: index
---
<Image align="center" width="900px" src="https://files.readme.io/5f844af2d7884698a45f3d8af806874028f7a16f36a6ce86bb9e28ee4e83363c-DPD_IE_banner_white.png" />

***

DPD Ireland ship domestically within Ireland and internationally to other EU and <Glossary>ROW</Glossary> countries.

The integration of DPD IE into the SAPIENT platform is a significant step in enhancing shipping capabilities. This section provides more information on how DPD IE services can help you to deliver more for you and your customers.

## Key features

This integration provides the following key features:

* **Ship from destinations**: The integration supports shipping from locations in Ireland (IE) and Northern Ireland (country code GB and postcodes beginning with BT).
* **Ship To Destinations**: Users can send shipments domestically within Ireland, to Great Britain (GB), Europe (EU), and Rest of the World (<Glossary>ROW</Glossary>).
* **Service Type**: The integration is focused on outbound shipping only.
* **Incoterms**: <Glossary>DAP</Glossary> and <Glossary>DDP</Glossary>.
* **Label formats**: <Glossary>PDF</Glossary> and <Glossary>PNG</Glossary>.

## Service enhancements

The following are the key services are provided by the DPD IE integration:

* **Email Notification**: Delivery updates are sent via email. To use this enhancement code, the destination **ContactEmail** must be provided with a valid email address.   
* **SMS Notification**: Delivery updates are sent via SMS. To use this enhancement code, the destination **ContactPhone** field must be specified with a valid phone number.
* **Delivery options**: DPD IE provides the following delivery options:
  * **DelivertoNeighbour**: Allows the delivery to be left with a nearby neighbour if the recipient is not available.
  * **DelivertoSafeplace**: Allows the delivery to be left in a specified secure location at the delivery address when the recipient is not available. If this enhancement is used, the details of the location must be specfied in the **SafeplaceLocation** field captured in the **CarrierSpecifics** block of the Create Shipment request.
  * **DeliverytoLetterbox**: Indicates that the item is small enough to be delivered through the recipient’s letterbox.
* **ExtraInsurance**: Provides additional coverage for the shipment beyond the standard liability, protecting against loss or damage up to a specified value.
* **PinOnDelivery**: Requires a secure PIN to be provided at the time of delivery to confirm receipt by the recipient. To use this enhancement code, the destination **ContactPhone** or **ContactEmail** fields must be specified with a valid phone number or email address.

<Callout icon="💡" theme="default">
  ### _Tip_

  _For more information on the service enhancements and carrier services, refer to the [Get Carrier Services](https://docs.intersoftsapient.net/reference/get_v4-carriers-carriercode-services) API endpoint_
</Callout>

## Additional features

The DPD IE integration provides the following additional features:

* **Consignment services**:  Multi-piece shipments are are supported for all services except DPD Air Express.

> 📘 _Note_
>
> _For Domestic and DPD Classic services, the maximum number of packages allowed is 10, and for DPD Air Express,  it is 1._

* **Delivery Instructions**: To provide special instructions related to the delivery of the shipment. This may involve guidance on how the package should be handled or specific requests regarding the delivery location (for example, leave at the back door or deliver to a neighbour to sign).
* Safe Place Location: To provide details of the safe place location for the shipment. This field is mandatory if  the **DeliverToSafeplace** service enhancement is used.

## Carrier Services

The following key services are provided by the DPD Ireland integration.

| Service Name                  | Description                                                                                                                                                                                                           |
| :---------------------------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **DPD Saturday Delivery**     | This service provides weekend delivery of parcels on Saturdays, enabling businesses and recipients to receive shipments outside standard weekday delivery schedules.                                                  |
| **DPD Next Day**              | This service provides fast, next-working-day delivery within Ireland and selected regions, ensuring parcels arrive quickly with reliable transit times and full tracking visibility.                                  |
| **DPD Air Express**           | This service provides urgent international delivery via an established air network, offering next-day delivery to many destinations and worldwide coverage to over 200 countries with full tracking.                  |
| **DPD Classic**               | This service provides reliable, cost-effective road-based parcel delivery across Ireland and Europe, offering fast standard transit times, full tracking, and high-volume shipping capabilities.                      |
| **DPD Classic International** | This service provides international parcel delivery through DPD’s road and air network, combining competitive pricing with reliable transit times, full tracking, and coverage across Europe and global destinations. |

<Callout icon="💡" theme="default">
  ### _Tip_

  _For the most up-to-date carrier services, use the [Get Carrier Services](https://docs.intersoftsapient.net/reference/get_v4-carriers-carriercode-services) endpoint._
</Callout>

## API Services

The following API services are provided by the DPD IE integration:

* **Create shipment**: The integration for creating shipments to reflect DPD IE as a primary carrier and allowing users to create shipments using the Create Shipment that returns the label in base64 encoded format.
* **Manifest webhook**: Keep track of shipments and their statuses by to receiving real-time updates or notifications whenever specific events occur in the system (such as shipping updates, status changes, and so on) via the SAPIENT Manifest Webhook feature.
* **Tracking**: Enables customers to receive tracking updates through their integration with the SAPIENT tracking webhook.
