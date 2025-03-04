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
\<details>
&#x20; \<summary>Jan 2025\</summary>

&#x20; \<br />

&#x20; \## Royal Mail HVD and ITO services description updates

&#x20; The service descriptions for Royal Mail's HVD and ITO services have been updated to ensure alignment with the latest specifications. The service name for HVD has been changed from "INTL BUSINESS TRACKED EXPRESS NPC" to "INTL BUSINESS TRACKED PRIORITY," while the ITO service name has been updated from "DEImpNonUK TrkPCL Hvy (EMS)" to "DE Import Non-UK Tracked Parcel Cmp Heavy (DEImpNonUK TrkPCLCmp Hvy (EMS))." These updates reflect the current shipping services offered and enhance clarity for users.

&#x20; \## Royal Mail tracking integration updates

&#x20; The tracking integration for Royal Mail  has been updated to enhance the accuracy of tracking information delivered through the SAPIENT tracking webhook. The Royal Mail tracking event "EVRTS" (Delivered back to sender) is now correctly mapped to the new INTERSOFT tracking event "UDTS" (Delivered to Sender) and assigned to the milestone category "Undeliverable." This change ensures that customers receive precise tracking updates, eliminating confusion regarding successful deliveries. The Royal Mail tracking translation file has been updated accordingly, allowing for seamless integration of this new mapping in the SAPIENT system.

&#x20; \*\*\*

&#x20; \## DX Freight integration

&#x20; A new DX Freight integration has been added to SAPIENT to enhance your shipping experience with improved functionality and efficiency.

&#x20; In the scope of the DX Freight integration, the following features have been integrated into SAPIENT:

&#x20; \* \*\*Shipping Account screen\*\*. Seamlessly manage your DX Freight shipping accounts.
&#x20; \* \*\*Tracking Account screen\*\*. Create tracking accounts and webhook to receive tracking updates from DX via the tracking webhook functionality.
&#x20; \* \*\*Label Integration\*\*. Configure the label integration with DX Freight and print your shipping labels using the \*\*Print Label\*\* API endpoint.

&#x20; \## International arrivals containers

&#x20; INTERSOFT offers shipping services from different countries to the United Kingdom via Royal Mail; however, Royal Mail's inability to identify shipment contents before arrival has created unexpected traffic. To address this, a new \*\*International Arrivals Containers\*\* API service has been implemented by INTERSOFT. With this service, you can now link receptacle (bag) IDs with shipment tracking numbers by creating containers. Before constructing these containers, configuration of a \*\*Customer Number\*\* and \*\*Barcode Range\*\* is required, and to configure that, a new \*\*International Arrivals Container Settings\*\* screen has been added to SAPIENT.

&#x20; \## Additional Yodel services

&#x20; The Yodel integration in Sapient has been updated with additional services, allowing Yodel customers to select and use these services for shipment creation. This integration ensures a consistent user experience by aligning with Yodel's latest specifications and maintaining compatibility with existing services. The new services are incorporated into the database, reflected in the \*\*GetCarrierServices\*\* API response, and displayed on generated shipment labels, facilitating effective onboarding of new clients and helping Yodel stay competitive.

&#x20; \## Swagger documentation updates

&#x20; The following information has been added to the swagger documentation:

&#x20; \* \*\*New API endpoints\*\*. A new \*\*SAPIENT DX FREIGHT\*\* block has been added to our carrier-specific APIs. This block includes the following API endpoints:
&#x20;   \* \*\*Shipping Account\*\*
&#x20;     \* \*\*Get Accounts\*\*: Retrieve a list of DX Freight shipping accounts.
&#x20;     \* \*\*Add Account\*\*: Add a new DX Freight shipping account.
&#x20;     \* \*\*Update Account\*\*: Update details of an existing DX Freight shipping account.
&#x20;     \* \*\*Link Locations\*\*: Link shipping locations to DX Freight shipping accounts.
&#x20;     \* \*\*Get Associated Locations\*\*: Retrieve locations linked to the DX Freight shipping account.
&#x20;     \* \*\*Get Associated Location\*\*: Fetch details for a specific associated location.
&#x20;     \* \*\*Update Associated Location\*\*: Update details for an associated location.
&#x20;   \* \*\*Shipments\*\*
&#x20;     \* \*\*Create Shipment\*\*: Create a new DX Freight shipment request.
&#x20;     \* \*\*Print Label\*\*: Generate a label for a DX Freight shipment.
&#x20; \* \*\*Additional information\*\*. You can now call the following \*\*SAPIENT CORE APIs\*\* for relevant information while shipping with DX Freight:
&#x20;   \* \*\*Get Carrier Accounts\*\*
&#x20;   \* \*\*Get Carrier Services\*\*
&#x20;   \* \*\*Get Carrier Services Package Types\*\*
&#x20;   \* \*\*Get Carrier Service\*\*
&#x20; \* \*\*New Royal Mail API endpoints\*\*. As part of the international arrival containers, the following new services API endpoints have been added under the \*\*SAPIENT Royal Mail API\*\* block in the Swagger documentation:
&#x20;   \* \*\*International Arrival Containers\*\*
&#x20;     \* \*\*Add Container\*\*
&#x20;     \* \*\*Get Container\*\*
&#x20;     \* \*\*Update Container\*\*
&#x20;     \* \*\*Add/Remove Shipments\*\*
&#x20;     \* \*\*Delete Container\*\*
&#x20;     \* \*\*Get Container\*\*
\</details>

\<details>
\<summary>Feb\</summary>
\<br>
\## FedEx integration (coming soon)
&#x20;&#x20;
\</details>