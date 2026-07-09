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

## Key features

This integration provides the following key features:

* **Ship from destinations**: The integration supports shipping from locations in Great Britain (GB) only.
* **Ship To Destinations**: Users can send shipments to Great Britain (GB), Europe (EU), and the Rest of the World (<Glossary>ROW</Glossary>).
* **Service Type**: The integration is focused on outbound shipping.
* **Incoterms**: <Glossary>DAP</Glossary> and <Glossary>DDP</Glossary>.
* **Label formats**: <Glossary>PDF</Glossary>

## Service enhancements

The following are the key services are provided by the DPD UK integration:

* **Proof of Identity**: Requires the receiver to present valid identification at the point of delivery.
* **Proof of Age**: Ensures the recipient meets a minimum age requirement, like for age-restricted goods.
* **Pin Required**: A secure PIN is sent to the receiver, which must be provided upon delivery.
* **Pin Required & Proof of Age**: Requires PIN and age verification at the point of delivery for added security.

<Callout icon="💡" theme="default">
  ### _Tip_

  _For more information on the service enhancements and carrier services, refer to the following endpoints:_

  * [_Create Shipment_](https://docs.intersoftsapient.net/reference/post_v4-shipments-dpduk)
  * [_Get Carrier Services_](https://docs.intersoftsapient.net/reference/get_v4-carriers-carriercode-services)
</Callout>

## Additional features

The DPD UK integration provides the following additional features:

* **Consignment services**:  Consignment services are supported, and DPD UK allows a maximum of 99 packages per consignment.

> 📘 _Note_
>
> _Please bear in mind that not all services offer consignment options._

* **Carrier specific fields**: The **CarrierSpecifics** object in the **Create Shipment** endpoint contains the following field:
  * **DeliveryInstructions**: To provide any additional instructions to the carrier regarding the delivery of the shipment.

## Integration types

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
