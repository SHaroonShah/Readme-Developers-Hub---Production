---
title: New integration - Spring GDS
author: Syed Haroon Shah
hidden: true
published_at: '2026-10-05T14:33:49.594Z'
---
The Starlinks Global integration has been added to the SAPIENT system. This integration supports outbound international shipments from Great Britain (GB) and European Union (EU) and to GB domestically ,EU, and ROW (Rest of the World) destinations. With this addition, the following information has been added to the swagger documentation:

**New API endpoints**. A new **Starlinks Global** block has been added to our carrier-specific APIs. This block includes the following API endpoints:

- **Shipping Account**
  - **Get Accounts**: Retrieve a list of the Starlinks Global shipping accounts.
  - **Add Account**: Add a new Starlinks Global shipping account.
  - **Get Account**: Retrieve details of a specific Starlinks Global shipping account.
  - **Update Account**: Update details of an existing Starlinks Global shipping account.
  - **Link Locations**: Link shipping locations to a Starlinks Global shipping accounts.
  - **Get Associated Locations**: Retrieve locations linked to the Starlinks Global shipping account.
  - **Get Associated Location**: Retrieve details for a specific Starlinks Global associated location.
- **Shipments**
  - **Create Shipment**: Create a new Starlinks Global shipment request.
  - **Print Label**: Generate a label for the Starlinks Global shipment.
- **DPD Ireland shipping account screen**. As part of the new integration, customer users and Carrier Account Administrators can now configure the Starlinks Global shipping account via the SAPIENT UI for creating shipments.  The **Add Shipping Account** screen now includes Starlinks Global as a carrier for selection, with mandatory fields required for configuration.
- **Tracking**: Enables customers to receive tracking updates through their integration with the SAPIENT tracking webhook.
- **Manifest shipment**: Enable customers to retrieve information about shipment manifests created by the system and track when shipments have been successfully manifested with Starlinks Global.

<Callout icon="📘" theme="info">
  ### _Note_

  _For more information on this integration, refer to the Starlinks Global user guides._
</Callout>