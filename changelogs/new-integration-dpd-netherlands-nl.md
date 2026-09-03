---
title: New integration - DPD Netherlands (NL)
author: Syed Haroon Shah
hidden: true
published_at: '2026-04-01T14:04:16.528Z'
type: added
---
The DPD Netherlands (NL) integration has been added to the SAPIENT system. This integration supports shipping domestically within the Netherlands, and to EU, GB, and Rest of World destinations. With this addition, the following information has been added to the swagger documentation:

**New API endpoints**. A new **DPD NETHERLANDS** block has been added to our carrier-specific APIs. This block includes the following API endpoints:

* **Shipping Account**
  * **Get Accounts**: Retrieve a list of the DPD Netherlands shipping accounts.
  * **Add Account**: Add a new DPD Netherlands shipping account.
  * **Get Account**: Retrieve details of a specific DPD Netherlands shipping account.
  * **Update Account**: Update details of an existing DPD Netherlands shipping account.
  * **Link Locations**: Link shipping locations to a DPD Netherlands shipping accounts.
  * **Get Associated Locations**: Retrieve locations linked to the DPD Netherlands shipping account.
  * **Get Associated Location**: Retrieve details for a specific DPD Netherlands associated location.
* **Shipments**
  * **Create Shipment**: Create a new DPD Netherlands shipment request.
  * **Print Label**: Generate a label for the DPD Netherlands shipment.
* **DPD Netherlands shipping account screen**. As part of the new integration, customer users and Carrier Account Administrators can now configure the DPD Netherlands shipping account via the SAPIENT UI for creating shipments.  The **Add Shipping Account** screen now includes DPD Netherlands as a carrier for selection, with mandatory fields required for configuration.