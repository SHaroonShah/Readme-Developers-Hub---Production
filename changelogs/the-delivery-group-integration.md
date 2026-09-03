---
title: The Delivery Group integration
author: Syed Haroon Shah
hidden: true
published_at: '2025-05-28T10:15:17.499Z'
type: added
---
The Delivery Group integration has been added to the SAPIENT system. This integration expands our shipping options, allowing our customers to utilise The Delivery Group for their shipping needs, improving overall service flexibility and efficiency.

With this addition, the following information has been added to the swagger documentation:

* **New API endpoints**. A new **THE DELIVERY GROUP** block has been added to our carrier-specific APIs. This block includes the following API endpoints:
  * **Shipping Account**
    * **Get Accounts**: Retrieve a list of the delivery group shipping accounts.
    * **Add Account**: Add a new delivery group shipping account.
    * **Get Account**: Retrieve details of a specific delivery group shipping account.
    * **Update Account**: Update details of an existing delivery group shipping account.
    * **Link Locations**: Link shipping locations to the delivery group shipping accounts.
    * **Get Associated Locations**: Retrieve locations linked to the delivery group shipping account.
    * **Get Associated Location**: Fetch details for a specific associated location.
  * **Shipments**
    * **Create Shipment**: Create a new delivery group shipment request.
    * **Print Label**: Generate a label for the delivery group shipment.