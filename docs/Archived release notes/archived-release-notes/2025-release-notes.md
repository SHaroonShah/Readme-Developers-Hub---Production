---
title: 2025 release notes
excerpt: This section includes the archived release notes published in the year 2025.
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
## Royal Mail combined label

A new Royal Mail label type has been added for shipments imported into GB, specifically aimed at those with a shipment value of £135 or under. These shipments will now require a combined label image of a domestic tracked label and a CN22 customs form. This update streamlines the process for lower-value shipments, which previously utilised CN23 forms exclusively for higher-value items. The new combined label will be produced in a standard 6x4 size, featuring two labels side by side for clarity and efficiency.

## Swagger documentation updates

As part of our **CORE API**, the descriptions of the following API endpoints have been updated for clarity and improved user experience:

* **Get Carrier**
* **Get Carriers**
* **Get Carrier Services**
* **Get Carrier Service Package Types**

## FedEx integration (coming soon)

A new FedEx integration is coming soon! This integration aims to enhance your shipping experience with improved functionality and efficiency. Stay tuned for more updates, as we will provide further details on features and availability shortly.

***

## Royal Mail HVD and ITO services description updates

The service descriptions for Royal Mail's HVD and ITO services have been updated to ensure alignment with the latest specifications. The service name for HVD has been changed from "INTL BUSINESS TRACKED EXPRESS NPC" to "INTL BUSINESS TRACKED PRIORITY," while the ITO service name has been updated from "DEImpNonUK TrkPCL Hvy (EMS)" to "DE Import Non-UK Tracked Parcel Cmp Heavy (DEImpNonUK TrkPCLCmp Hvy (EMS))." These updates reflect the current shipping services offered and enhance clarity for users.

## Royal Mail tracking integration updates

The tracking integration for Royal Mail  has been updated to enhance the accuracy of tracking information delivered through the SAPIENT tracking webhook. The Royal Mail tracking event "EVRTS" (Delivered back to sender) is now correctly mapped to the new INTERSOFT tracking event "UDTS" (Delivered to Sender) and assigned to the milestone category "Undeliverable." This change ensures that customers receive precise tracking updates, eliminating confusion regarding successful deliveries. The Royal Mail tracking translation file has been updated accordingly, allowing for seamless integration of this new mapping in the SAPIENT system.

## DX Freight integration

A new DX Freight integration has been added to SAPIENT to enhance your shipping experience with improved functionality and efficiency.

In the scope of the DX Freight integration, the following features have been integrated into SAPIENT:

* **Shipping Account screen**. Seamlessly manage your DX Freight shipping accounts.
* **Tracking Account screen**. Create tracking accounts and webhook to receive tracking updates from DX via the tracking webhook functionality.
* **Label Integration**. Configure the label integration with DX Freight and print your shipping labels using the **Print Label** API endpoint.

## International arrivals containers

INTERSOFT offers shipping services from different countries to the United Kingdom via Royal Mail; however, Royal Mail's inability to identify shipment contents before arrival has created unexpected traffic. To address this, a new **International Arrivals Containers** API service has been implemented by INTERSOFT. With this service, you can now link receptacle (bag) IDs with shipment tracking numbers by creating containers. Before constructing these containers, configuration of a **Customer Number** and **Barcode Range**is required, and to configure that, a new **International Arrivals Container Settings** screen has been added to SAPIENT.

## Additional Yodel services

The Yodel integration in Sapient has been updated with additional services, allowing Yodel customers to select and use these services for shipment creation. This integration ensures a consistent user experience by aligning with Yodel's latest specifications and maintaining compatibility with existing services. The new services are incorporated into the database, reflected in the **GetCarrierServices** API response, and displayed on generated shipment labels, facilitating effective onboarding of new clients and helping Yodel stay competitive.

## Swagger documentation updates

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