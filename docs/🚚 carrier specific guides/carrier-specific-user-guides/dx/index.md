---
title: DX Express
excerpt: >-
  _DX_ is a UK-based logistics and parcel delivery company that specialises in
  providing tailored delivery solutions for businesses and individuals. DX
  offers a wide range of delivery options, including time-sensitive and next-day
  services, focusing on delivering parcels, documents, and heavy items.
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
<Image align="center" width="130px" src="https://files.readme.io/160d38a06e94f72bb4eed1107cfb82c795f7bb915566bfa72eb3b8b3698bf38d-DX_express_logo.png" />

***

Express is one of DX's core solutions that provides a fast and secure next-day delivery service to businesses and home addresses for single and multiple items under 25 kg in weight and 2 metres in dimension.

The DX Express integration into the SAPIENT system provides the following key features:

* **Ship from destinations**: The integration supports shipping from locations in Great Britain (GB) only.
* **Ship To Destinations**: Users can send <Glossary>shipments</Glossary> to Great Britain (GB) and Northern Ireland (NI). Shipments to GB country code with a postcode beginning with BT).
* **Service Type**: The integration is focused on outbound shipping.

## Additional features

The DX Express integration provides the following additional features:

* **Single-piece shipments**: Supports only single-piece shipment (not consignment or multipiece)
* **Incoterms**: The integration supports <Glossary>DAP</Glossary> and <Glossary>DDP</Glossary>.
* **Label formats**: <Glossary>PDF</Glossary>, <Glossary>ZPL203DPI</Glossary>, and <Glossary>ZPL300DPI</Glossary>
* **Package types**: DX support <Glossary>package type</Glossary>s. You can look up for the packages types by calling the [Get Carrier Service Package Types](https://docs.intersoftsapient.net/reference/get_v4-carriers-carriercode-services-servicecode-packagetypes#/) endpoint.
  ## Carrier API services
  The following API services are provided by the DX Express integration:
  * **Session API**: The integration to authenticate and authorise users to use the carrier services via API.
  * **Consignment (Create Shipment) API**: The integration for creating individual shipments per request.
  * **Label API**: The integration for retrieving the package label in the PDF or ZPL format.
  * **Cancel API**: The integration for  directly calling the DX’s API to cancel shipments within DX’s system, to ensures that cancellations are fully registered with DX, helping prevent customers from being mistakenly charged for cancelled shipments.
  <br />
  > 🚧 _Important_
  >
  > _If you attempt to release a held shipment to a later date, please be aware that the shipment will no longer be eligible for cancellation._
  <br />
  * **Tracking**: The integration to track and monitor shipments in real time by receiving automatic updates on shipment status, delivery progress, and exceptions.

> 🚧 _Important_
>
> _If you attempt to release a held shipment to a later date, please be aware that the shipment will no longer be eligible for cancellation._

<br />

## Integration types

The following integration types are available for this integration:

* **Label**: Enables retrieving the package label in the PDF or ZPL format.
* **Tracking**: Enables the tracking data to be sent via the Tracking API.
* [Add DX shipping account](https://docs.intersoftsapient.net/docs/shipping-accounts-5)
* [Add DX tracking account](https://docs.intersoftsapient.net/docs/tracking-1)

***

## See also

* [DX rate limiting](https://docs.intersoftsapient.net/docs/dx-rate-limit)
* [Set up DX API credentials](https://docs.intersoftsapient.net/docs/setting-up-dx-api-credentials)
