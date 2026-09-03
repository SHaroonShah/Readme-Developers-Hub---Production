---
title: New integration - DHL Germany (DE)
author: Syed Haroon Shah
hidden: true
published_at: '2026-04-21T14:22:37.223Z'
type: added
---
The DHL Germany (DE) integration has been added to the SAPIENT system. This integration supports shipping domestically within Germany, and to EU, GB, and Rest of World destinations. With this addition, the following information has been added to the swagger documentation:

**New API endpoints**. A new **DHL GERMANY** block has been added to our carrier-specific APIs. This block includes the following API endpoints:

* **Shipping Account**
  * **Get Accounts**: Retrieve a list of the DHL Germany shipping accounts.
  * **Add Account**: Add a new DHL Germany shipping account.
  * **Get Account**: Retrieve details of a specific DHL Germany shipping account.
  * **Update Account**: Update details of an existing DHL Germany shipping account.
  * **Link Locations**: Link shipping locations to a DHL Germany shipping accounts.
  * **Get Associated Locations**: Retrieve locations linked to the DHL Germany shipping account.
  * **Get Associated Location**: Retrieve details for a specific DHL Germany associated location.
* **Shipments**
  * **Create Shipment**: Create a new DHL Germany shipment request.
  * **Print Label**: Generate a label for the DHL Germany shipment.
* **DHL Germany shipping account screen**. As part of the new integration, customer users and Carrier Account Administrators can now configure the DHL Germany shipping account via the SAPIENT UI for creating shipments.  The **Add Shipping Account** screen now includes DHL Germany as a carrier for selection, with mandatory fields required for configuration.
* **Tracking**: Enables customers to receive tracking updates through their integration with the SAPIENT tracking webhook.
* **Manifest shipment**: Enable customers to retrieve information about shipment manifests created by the system and track when shipments have been successfully manifested with DHL Germany.

> 📘 _Note_
>
> _For more information on this integration, refer to the [DHL Germany](https://docs.intersoftsapient.net/docs/dhl-germany-de) user guides._

<br />

<br />