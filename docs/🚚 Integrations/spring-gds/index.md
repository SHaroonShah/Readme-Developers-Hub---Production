---
title: Spring GDS
excerpt: >-
  Spring Global Delivery Solutions (GDS) is a carrier aggregator providing
  international mail and parcel services through a network of final mile
  delivery partners.
deprecated: false
hidden: false
icon: fad fa-truck-fast
link:
  new_tab: false
metadata:
  robots: index
---
The integration of Spring GDS into the SAPIENT platform is a significant step in enhancing shipping capabilities. This section discusses the in-scope features of this integration and the services this carrier offers.

Key features

This integration provides the following key features:

Shipping origins: The integration supports shipping from Great Britain (GB) and European Union (EU).

Shipping destinations: Users can send shipments to Great Britain (GB), Europe (EU), and ROW (Rest of the World).

Note

Shipping destinations will be determined based on the services enabled on the shipping account and service matrix provided by the carrier.

Service Type: The integration is focused on outbound shipping only.

Incoterms: DDU and DDP.

Label formats: PDF, PNG, and ZPL (200 and 300 dpi).

Service enhancements

Note

There are no service enhancements for this integration.

Additional features

The Spring GDS integration provides the following additional features:

Single-package services: Spring GDS supports only single-package services. Consignment services are not supported in this integration.

Carrier-specific fields: The following fields are optional and are specified in the Carrier Specifics block of the create shipment request.

Important

Before using the carrier-specific fields, please bear in mind the following:

Carrier-specific fields are only applicable to Spring Clear and default to false if not supplied and do not cause shipment validation failures when omitted.

Spring Clear cannot be configured at the shipping account level or via any UI setting in SAPIENT. It is not a configurable feature on our side and depends on the customer’s agreement and setup with Spring GDS.

If configured, you can trigger it by setting the incoterm to DDP in the create shipment request.

PreferentialOriginTag: An optional field for reduced or zero duty rates under specific international trade agreements. Customers are expected to determine which of their products qualify for this treatment based on their own research and compliance obligations.

BondedGoods: An optional field used to indicate goods where customs duties have not yet been paid, and the goods remain under customs supervision until duty payment.

Carrier API services

The following API services are provided by the Spring GDS integration:

Create shipment: The integration for creating shipments to reflect Spring GDS as a primary carrier and allowing users to create shipments using the Create Shipment that returns the label in base64 encoded format.

Tracking: Enables customers to receive tracking updates through their integration with the SAPIENT tracking webhook.

Manifest shipment: Enable customers to retrieve information about shipment manifests created by the system and track when shipments have been successfully manifested with the carrier. For customers who need real‑time updates, we strongly recommend using the INTERSOFT Manifest Webhook, which provides updates on manifest requests, allowing you to track the progress and status of shipments prepared for carrier collection and delivery.
