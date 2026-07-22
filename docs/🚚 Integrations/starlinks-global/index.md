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

- Ship from destinations: The integration supports shipping from locations in Great Britain (GB) only.
- Ship To Destinations: Users can send shipments to Great Britain (GB), Europe (EU), and ROW (Rest of the World).
- Service Type: The integration is focused on outbound shipping only.
- Incoterms: DDU and DDP.
- Label formats: PDF, PNG, and ZPL300DPI.

# <br />Service enhancements

<Callout icon="📘" theme="info">
  ### _Note_

  _There are no service enhancements for this integration_.
</Callout>

# <br />Additional features

The Starlinks Global integration provides the following additional features:

- Single-package services: Starlinks Global supports only single-package services. Consignment services are not supported in this integration.

# Carrier services

<br />

# Carrier API services

The following API services are provided by the Starlinks Global integration:

- **Create shipment**: The integration for creating shipments to reflect Starlinks Global as a primary carrier and allowing users to create shipments using the Create Shipment that returns the label in base64 encoded format.
- **Tracking**: Enables customers to receive tracking updates through their integration with the SAPIENT tracking webhook.
- **Manifest shipment**: Enable customers to retrieve information about shipment manifests created by the system and track when shipments have been successfully manifested with the carrier. For customers who need real‑time updates, we strongly recommend using the INTERSOFT Manifest Webhook to keep track of shipments and their statuses by to receiving real-time updates or notifications whenever specific events occur in the system (such as shipping updates, status changes, and so on).

<br />
