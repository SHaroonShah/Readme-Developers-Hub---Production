---
title: New integration - DHL Express
author: Syed Haroon Shah
hidden: true
published_at: '2026-06-04T15:42:39.559Z'
type: added
---
The DHL Express integration has been added to the SAPIENT system. This integration supports shipping domestically within UK, to EU and Rest of World destinations. With this addition, the following information has been added to the swagger documentation:

**New API endpoints**. A new **DHL EXPRESS** block has been added to our carrier-specific APIs. This block includes the following API endpoints:

* **Shipping Account**
  * **Get Accounts**: Retrieve a list of the DHL Express shipping accounts.
  * **Add Account**: Add a new DHL Express shipping account.
  * **Get Account**: Retrieve details of a specific DHL Express shipping account.
  * **Update Account**: Update details of an existing DHL Express shipping account.
  * **Link Locations**: Link shipping locations to a DHL Express shipping accounts.
  * **Get Associated Locations**: Retrieve locations linked to the DHL Express shipping account.
  * **Get Associated Location**: Retrieve details for a specific DHL Express associated location.
* **Shipments**
  * **Create Shipment**: Create a new DHL Express shipment request.
  * **Print Label**: Generate a label for the DHL Express shipment.
* **DHL Express shipping account screen**. As part of the new integration, customer users and Carrier Account Administrators can now configure the DHL Express shipping account via the SAPIENT UI for creating shipments.  The **Add Shipping Account** screen now includes DHL Express as a carrier for selection, with mandatory fields required for configuration, along with options to configure Archive Labels and Paperless Trade (PLT).
* **Tracking**: Enables customers to receive tracking updates through their integration with the SAPIENT tracking webhook.
* **Manifest shipment**: Enable customers to retrieve information about shipment manifests created by the system and track when shipments have been successfully manifested with DHL Express.

> 📘 _Note_
>
> _For more information on this integration, refer to the <Anchor label="DHL Express" target="_blank" href="https://docs.intersoftsapient.net/docs/dhl-express">DHL Express</Anchor> section._

<br />