---
title: Swagger documentation updates
author: Syed Haroon Shah
hidden: true
published_at: '2024-12-20T14:51:57.208Z'
type: improved
---
The following information has been added to the swagger documentation:

* **New API endpoints**. A new **SAPIENT DX FREIGHT** block has been added to our carrier-specific APIs. This block includes the following API endpoints: 
  * **Shipping Account** 
    * **Get Accounts**: Retrieve a list of DX Freight shipping accounts.
    * **Add Account**: Add a new DX Freight shipping account.
    * **Update Account**: Update details of an existing DX Freight shipping account.
    * **Link Locations**: Link shipping locations to DX Freight shipping accounts.
    * **Get Associated Locations**: Retrieve locations linked to the DX Freight shipping account.
    * **Get Associated Location**: Fetch details for a specific associated location.
    * **Update Associated Location**: Update details for an associated location.
  * **Shipments** 
    * **Create Shipment**: Create a new DX Freight shipment request.
    * **Print Label**: Generate a label for a DX Freight shipment.

***

* **Additional information**. You can now call the following **SAPIENT CORE APIs** for relevant information while shipping with DX Freight: 
  * **Get Carrier Accounts**
  * **Get Carrier Services**
  * **Get Carrier Services Package Types**
  * **Get Carrier Service**

***

* **New Royal Mail API endpoints**. As part of the international arrival containers, the following new services API endpoints have been added under the **SAPIENT Royal Mail API** block in the Swagger documentation: 
  * **International Arrival Containers** 
    * **Add Container**
    * **Get Container**
    * **Update Container**
    * **Add/Remove Shipments**
    * **Delete Container**
    * **Get Container**