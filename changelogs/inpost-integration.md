---
title: InPost integration
author: Syed Haroon Shah
hidden: true
published_at: '2025-07-25T10:59:20.624Z'
type: added
---
The In Post integration has been added to the SAPIENT system, providing users with flexible shipping options, including lookup for convenient locker services for secure parcel pickups via the SAPIENT’s **PUDO Locations** endpoint. This enhancement streamlines shipment management and leverages new capabilities for a better shipping experience.

**New API endpoints**. A new **IN POST** block has been added to our carrier-specific APIs. This block includes the following API endpoints:

* **Shipping Account**
  * **Get Accounts**: Retrieve a list of the InPost shipping accounts.
  * **Add Account**: Add a new InPost shipping account.
  * **Get Account**: Retrieve details of a specific InPost shipping account.
  * **Update Account**: Update details of an existing InPost shipping account.
  * **Link Locations**: Link shipping locations to an InPost shipping accounts.
  * **Get Associated Locations**: Retrieve locations linked to the InPost shipping account.
  * **Get Associated Location**: Retrieve details for a specific InPost associated location.
  * **Shipments**
    * **Create Shipment**: Create a new InPost shipment request.
    * **Print Label**: Generate a label for the InPost shipment.

***

* **InPost shipping account screen**. As part of the InPost integration in Sapient, customer users and Carrier Account Administrators can now configure the InPost shipping account via the SAPIENT UI for creating shipments. This integration supports both outbound and return shipments using InPost’s eco-friendly parcel locker service across England, Wales, and Scotland. The **Add Shipping Account** screen will now include InPost as a carrier for selection, with mandatory fields required for configuration. Additionally, carrier-specific fields for the InPost integration include a mandatory **Client ID** and a **Bearer token** (to be provided by the carrier).