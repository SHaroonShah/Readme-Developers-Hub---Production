---
title: New integration - DPD Ireland
author: Syed Haroon Shah
hidden: true
published_at: '2026-08-05T13:49:06.867Z'
type: added
---
The DPD Ireland integration has been added to the SAPIENT system. This integration supports shipping domestically within Ireland and Northern Ireland, and to EU, GB, and Rest of World destinations. With this addition, the following information has been added to the swagger documentation:

**New API endpoints**. A new **DPD Ireland** block has been added to our carrier-specific APIs. This block includes the following API endpoints:

- **Shipping Account**
  - **Get Accounts**: Retrieve a list of the DPD Ireland shipping accounts.
  - **Add Account**: Add a new DPD Ireland shipping account.
  - **Get Account**: Retrieve details of a specific DPD Ireland shipping account.
  - **Update Account**: Update details of an existing DPD Ireland shipping account.
  - **Link Locations**: Link shipping locations to a DPD Ireland shipping accounts.
  - **Get Associated Locations**: Retrieve locations linked to the DPD Ireland shipping account.
  - **Get Associated Location**: Retrieve details for a specific DPD Ireland associated location.
- **Shipments**
  - **Create Shipment**: Create a new DPD Ireland shipment request.
  - **Print Label**: Generate a label for the DPD Ireland shipment.
- **DPD Ireland shipping account screen**. As part of the new integration, customer users and Carrier Account Administrators can now configure the DPD Ireland shipping account via the SAPIENT UI for creating shipments.  The **Add Shipping Account** screen now includes DPD Ireland as a carrier for selection, with mandatory fields required for configuration.
- **Tracking**: Enables customers to receive tracking updates through their integration with the SAPIENT tracking webhook.
- **Manifest shipment**: Enable customers to retrieve information about shipment manifests created by the system and track when shipments have been successfully manifested with DPD Ireland.

<Callout icon="📘" theme="info">
  ### _Note_

  _For more information on this integration, refer to the DPD Ireland user guides._
</Callout>

<br />

<br />