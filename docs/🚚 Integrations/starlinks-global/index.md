---
title: Starlinks Global
excerpt: "Starlinks Global is a partner carrier providing international and domestic delivery solutions. They offer global delivery solutions for seamless cross-border trade, helping retailers deliver to nearly\_200 countries, even the regions which are typically complex to reach!"
deprecated: false
hidden: true
icon: fad fa-truck-fast
metadata:
  robots: index
---
The integration of Starlinks Global into the SAPIENT platform is a significant step in enhancing shipping capabilities. This section discusses the in-scope features of this integration and the services this carrier offers.

# <br />Key features

This integration provides the following key features:

- **Ship from destinations**: The integration supports shipping from locations in Great Britain (GB) only.
- **Ship To Destinations**: Users can send shipments to Great Britain (GB), Europe (EU), and <Glossary>ROW</Glossary> (Rest of the World).
- **Service Type**: The integration is focused on outbound shipping only.
- **Incoterms**: <Glossary>DDU</Glossary>and <Glossary>DDP</Glossary>.
- **Label formats**: <Glossary>PDF</Glossary>, <Glossary>PNG</Glossary>, and <Glossary>ZPL300DPI</Glossary>.

# <br />Service enhancements

<Callout icon="📘" theme="info">
  ### _Note_

  _There are no service enhancements for this integration_.
</Callout>

# <br />Additional features

The Starlinks Global integration provides the following additional features:

- **Single-package services**: Starlinks Global supports only single-package services. Consignment services are not supported in this integration.

# Carrier services

The following key services are provided by the Starlinks Global integration.

| Service Name                              | Description                                                                                                                  |
| ----------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------- |
| International Home Delivery               | This service provides international delivery of parcels directly to the recipient's home address.                            |
| International Express Service – Starlinks | This service provides expedited international delivery with end-to-end Starlinks handling.                                   |
| International Express Service – Last-Mile | This service provides expedited international delivery with delivery completed by a local last-mile carrier.                 |
| Final Mile                                | This service provides last-mile delivery from the destination hub to the recipient.                                          |
| Domestic                                  | This service provides domestic parcel delivery within supported countries such as the UK, USA, and Australia.                |
| Cross Border Direct – Starlinks Label     | This service provides cross-border parcel delivery using a Starlinks shipping label.                                         |
| Cross Border Direct – Last-Mile Label     | This service provides cross-border parcel delivery using a last-mile carrier label for final delivery.                       |
| Starlinks Domestic Premium                | This service provides premium domestic delivery within supported countries such as the UK, USA, and Australia.               |
| Cross Border Light                        | This service provides a cost-effective cross-border delivery solution for lightweight shipments.                             |
| Starlinks Border Flexi – Starlinks Label  | This service provides flexible cross-border delivery using a Starlinks shipping label.                                       |
| Starlinks Border Flexi – Last-Mile Label  | This service provides flexible cross-border delivery with final delivery performed by a local last-mile carrier.             |
| Starlinks Market Places – Starlinks Label | This service provides cross-border marketplace shipment delivery using a Starlinks shipping label.                           |
| Starlinks Market Places – Last-Mile Label | This service provides cross-border marketplace shipment delivery with final delivery completed by a local last-mile carrier. |

# Carrier API services

The following API services are provided by the Starlinks Global integration:

- **Create shipment**: The integration for creating shipments to reflect Starlinks Global as a primary carrier and allowing users to create shipments using the Create Shipment that returns the label in base64 encoded format.
- **Manifest Shipment**: Enables customers to retrieve information about shipment manifests created by the system and track when shipments have been successfully manifested with the carrier. For customers who need real‑time updates, we strongly recommend using the INTERSOFT Manifest Webhook to keep track of shipments and their statuses by receiving real-time updates or notifications whenever specific events occur in the system, such as shipping updates and status changes.
- **Tracking**: Enables customers to receive tracking updates through their integration with the SAPIENT tracking webhook.
- **Print Label:&#x20;**&#x47;enerate and return the label for a DX Freight shipment in the PDF, PNG, or ZPL format. This endpoint must be utilised when the label is not generated in the DXF Create Shipment request.
  <Callout icon="📘" theme="info">
    ### _Note_

    _This endpoint changes the status of the shipment to label printed. This endpoint should be called at the time of actual printing or label creation, depending on how your business operates. Shipments must be updated to label printed status prior to manifesting._
  </Callout>

<br />
