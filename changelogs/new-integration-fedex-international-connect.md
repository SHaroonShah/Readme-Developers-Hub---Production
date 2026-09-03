---
title: New integration - FedEx International Connect
author: Laura Price
hidden: true
published_at: '2026-02-23T12:55:51.144Z'
type: added
---
The FedEx International Connect integration has been added to the SAPIENT system. This integration supports shipping domestically within the UK, and to EU and Rest of World destinations. With this addition, the following information has been added to the swagger documentation:

**New API endpoints**. A new **FEDEX INTERNATIONAL CONNECT** block has been added to our carrier-specific APIs. This block includes the following API endpoints:

* **Shipping Account**
  * **Get Accounts**: Retrieve a list of the FedEx International Connect shipping accounts.
  * **Add Account**: Add a new FedEx International Connect shipping account.
  * **Get Account**: Retrieve details of a specific FedEx International Connect shipping account.
  * **Update Account**: Update details of an existing FedEx International Connect shipping account.
  * **Link Locations**: Link shipping locations to an FedEx International Connect shipping accounts.
  * **Get Associated Locations**: Retrieve locations linked to the FedEx International Connect shipping account.
  * **Get Associated Location**: Retrieve details for a specific FedEx International Connect associated location.
* **Shipments**
  * **Create Shipment**: Create a new FedEx International Connect shipment request.
  * **Print Label**: Generate a label for the FedEx International Connect shipment.
* **FedEx International Connect shipping account screen**. As part of the new integration, customer users and Carrier Account Administrators can now configure the FedEx International Connect shipping account via the SAPIENT UI for creating shipments.  The **Add Shipping Account** screen will now include FedEx International Connect as a carrier for selection, with mandatory fields required for configuration. Additionally, carrier-specific fields for the FedEx International Connect integration include a mandatory **Shipper Website URL** and  an **API Key** (to be provided by the carrier).

> 📘 _Note_
>
> _For more information on how to set up a FedEx International Connect shipping account, refer to the <Anchor label="Add FedEx International Connect Shipping Account" target="_blank" href="https://docs.intersoftsapient.net/docs/add-fedex-international-shipping-account">Add FedEx International Connect Shipping Account</Anchor> user guide._

<br />