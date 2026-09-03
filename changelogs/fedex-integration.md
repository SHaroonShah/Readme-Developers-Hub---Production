---
title: FedEx integration
author: Syed Haroon Shah
hidden: true
published_at: '2025-05-28T10:15:39.203Z'
type: added
---
The FedEx carrier integration has been added to the SAPIENT system. This enhancement provides our customers with expanded shipping options and improved logistics capabilities, allowing for more efficient management of their shipments.

With this addition, the following information has been added to the swagger documentation:

* **New API endpoints**. A new **FedEx** block has been added to our carrier-specific APIs. This block includes the following API endpoints:
* **Shipping Account**
  * **Get Accounts**: Retrieve a list of FedEx shipping accounts.
  * **Get Account**: Retrieve details of a specific FedEx shipping account.
  * **Link Locations**: Link shipping locations to FedEx shipping accounts.
  * **Get Associated Locations**: Retrieve locations linked to the FedEx shipping account.
  * **Get Associated Location**: Fetch details for a specific associated location.
* **Shipments**
  * **Create Shipment**: Create a new FedEx shipment request.
  * **Print Label**: Generate a label for a FedEx shipment.

> 📘 *Note*
>
> *For more information on how to set up a FedEx shipping account via the SAPIENT UI, refer to the [Add FedEx shipping account](https://docs.intersoftsapient.net/docs/add-fedex-shipping-account#/) section of our carrier-specific user guides.*