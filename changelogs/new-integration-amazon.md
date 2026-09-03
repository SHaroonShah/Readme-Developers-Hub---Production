---
title: New integration - Amazon
author: Laura Price
hidden: true
published_at: '2026-02-23T13:07:14.068Z'
type: added
---
The Amazon integration has been added to the SAPIENT system. This integration supports shipping via Amazon domestically within the UK for both orders created via Amazon and outside of Amazon.

With this addition, the following information has been added to the swagger documentation:

**New API endpoints**. A new **AMAZON** block has been added to our carrier-specific APIs. This block includes the following API endpoints:

* **Shipping Account**
  * **Get Accounts**: Retrieve a list of the Amazon shipping accounts.
  * **Add Account**: Add a new Amazon shipping account.
  * **Get Account**: Retrieve details of a specific Amazon shipping account.
  * **Update Account**: Update details of an existing Amazon shipping account.
  * **Link Locations**: Link shipping locations to an Amazon shipping account.
  * **Get Associated Locations**: Retrieve locations linked to the Amazon shipping account.
  * **Get Associated Location**: Retrieve details for a specific Amazon associated location.
* **Shipments**
  * **Create Shipment**: Create a new Amazon shipment request.
  * **Print Label**: Generate a label for the Amazon shipment.
* **Amazon shipping account screen**. As part of the new integration, customer users and Carrier Account Administrators can now configure the Amazon shipping account via the SAPIENT UI for creating shipments.  The **Add Shipping Account** screen will now include Amazon as a carrier for selection, with mandatory fields required for configuration.

> 📘 _Note_
>
> _For more information on how to set up an Amazon shipping account, refer to the  <Anchor label="Add Amazon Shipping Account" target="_blank" href="https://docs.intersoftsapient.net/docs/add-amazon-shipping-account">Add Amazon Shipping Account</Anchor> user guide._

<br />

<br />