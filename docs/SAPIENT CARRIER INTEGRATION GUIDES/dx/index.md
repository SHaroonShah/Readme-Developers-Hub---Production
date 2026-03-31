---
title: DX Express
excerpt: >-
  _DX_ is a UK-based logistics and parcel delivery company that specialises in
  providing tailored delivery solutions for businesses and individuals. DX
  offers a wide range of delivery options, including time-sensitive and next-day
  services, focusing on delivering parcels, documents, and heavy items.
deprecated: false
hidden: false
icon: fad fa-truck-fast
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
<Image align="center" width="900px" src="https://files.readme.io/18184b139f3c15f60566ae06ce4aacb8b6f3255b216fe298f6f8c971a8337e73-DX_Express_white_banner.png" />

***

Express is one of DX's core solutions that provides a fast and secure next-day delivery service to businesses and home addresses for single and multiple items under 25 kg in weight and 2 metres in dimension.

## Overview

<Tabs>
  <Tab title="Key Features">
    <Cards columns={3}>
      <Card title="Shipping Origins" icon="fa-map-marker-alt">
        The integration supports shipping from locations in Great Britain (GB) only.
      </Card>

      <Card title="Shipping Destinations" icon="fa-solid fa-globe">
        Users can send <Glossary>shipments</Glossary> to Great Britain (GB) and Northern Ireland (NI)——shipments to GB country code with a postcode beginning with BT).
      </Card>

      <Card title="Service Type" icon="fa-solid fa-shipping-fast">
        The integration is focused on outbound shipping.
      </Card>

      <Card title="Incoterms Support" icon="fa-solid fa-file-contract">
        The integration supports <Glossary>DAP</Glossary> and <Glossary>DDP</Glossary> incoterms.
      </Card>

      <Card title="Label Formats" icon="fa-solid fa-tag">
        The integration support labels in <Glossary>PDF</Glossary>, <Glossary>ZPL203DPI</Glossary>, and <Glossary>ZPL300DPI</Glossary> formats.
      </Card>
    </Cards>

    <br />

    > 📘 *Note*
    >
    > *Bear in mind that shipments to Channel Islands are treated as domestic destination for freight shipments.*

    <br />
  </Tab>

  <Tab title="Additional Features">
    <Accordion title="Single piece shipments" icon="">
      DX Freight supports a maximum of 999 packages in a shipment, but the SAPIENT maximum—99 is used instead.
    </Accordion>

    <br />

    <Accordion title="DX-1 service" icon="">
      A 1-man service type that is typically deigned for door to door standard next-day delivery of parcels weighing up to a specific limit (50 kg) to the capability of effectively handling pallets. This service is usually best for smaller and lighter <Glossary>package</Glossary>s. 1Man service type includes the following services:

      * **ON**: Overnight
      * **3D**: 3Day
      * 930: Overnight 9:30
      * AM: Overnight pre noon
      * SAT: Saturday
      * S93: Saturday 9:30
    </Accordion>

    <br />

    <Accordion title="DX-2 service" icon="">
      A 2-man service type that caters to larger and heavier <Glossary>shipments</Glossary>, typically allowing for items that require 2-person handling due to their size or weight. This service is useful particularly for businesses that deal with bulky items or items that cannot be managed by one person. 2Man service type includes the following services:

      * **H1**: 2Man Overnight
      * **H2**: 2Man Standard
      * **HS**: 2Man Saturday
      * **C1**: 2Man Collection Overnight
      * **C2**: 2Man Collection Standard
      * **CS**: 2Man Saturday Only
    </Accordion>
  </Tab>
</Tabs>

## Key features

The DX Express integration into the SAPIENT system provides the following key features:

* **Ship from destinations**: The integration supports shipping from locations in Great Britain (GB) only.
* **Ship To Destinations**: Users can send <Glossary>shipments</Glossary> to Great Britain (GB) and Northern Ireland (NI). Shipments to GB country code with a postcode beginning with BT).
* **Service Type**: The integration is focused on outbound shipping.
* **Label formats**: <Glossary>PDF</Glossary>, <Glossary>ZPL203DPI</Glossary>, and <Glossary>ZPL300DPI</Glossary>.
* **Incoterms**: The integration supports <Glossary>DAP</Glossary> and <Glossary>DDP</Glossary>.

## Additional features

The DX Express integration provides the following additional features:

* **Single-piece shipments**: Supports only single-piece shipment (not consignment or multipiece).
* **Package types**: DX support <Glossary>package type</Glossary>s. You can look up for the packages types by calling the [Get Carrier Service Package Types](https://docs.intersoftsapient.net/reference/get_v4-carriers-carriercode-services-servicecode-packagetypes#/) endpoint.
  ## Carrier API services
  The following API services are provided by the DX Express integration:
  * **Create Shipment**: The integration for creating individual shipments per request.
  * **Label**: The integration for retrieving the package label in the PDF or ZPL format.
  * **CanceI**: The integration for directly calling the DX’s API to cancel shipments within DX’s system, to ensures that cancellations are fully registered with DX, helping prevent customers from being mistakenly charged for cancelled shipments.

> 🚧 _Important_
>
> _If you attempt to release a held shipment to a later date, please be aware that the shipment will no longer be eligible for cancellation._

* **Tracking**: The integration to track and monitor shipments in real time by receiving automatic updates on shipment status, delivery progress, and exceptions.

## Integration types

The following integration types are available for this integration:

* **Label**: Enables retrieving the package label in the PDF or ZPL format.
* **Tracking**: Enables the tracking data to be sent via the Tracking API.

***

In this section, learn now to:

* [Add a DX shipping account](https://docs.intersoftsapient.net/docs/shipping-accounts-5)
* [Add a DX tracking account](https://docs.intersoftsapient.net/docs/tracking-1)
* [Handle DX rate limiting](https://docs.intersoftsapient.net/docs/dx-rate-limit)
* [Set up DX API credentials](https://docs.intersoftsapient.net/docs/setting-up-dx-api-credentials)

> 📘 _Note_
>
> _For more information on how to activate the DX Express integration, refer to the [Activate integration](https://docs.intersoftsapient.net/docs/integration-activation#/) section._
