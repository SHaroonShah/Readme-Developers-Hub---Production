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
## Royal Mail Local Collect enhancements

The Royal Mail's Local Collect enhancement now provides the following two new location types:

* **Collect+**: Now receiving data from Royal Mail for collect+ location, enabling customers to choose from a wide range of collection points.
* **Lockers**: This location will be available soon as part of the Local Collect enhancement.

This update allows customers to access a broader range of collection points. To utilise these new location types, the customers need to request the **enhancedLocationDetails** object to be returned in the [GET PUDO Locations](https://docs.intersoftsapient.net/reference/get_v4-pudolocations-carriercode-countrycode-postcode#/) response, and save the **locationId** of the chosen location to be sent in the `pudoId` field of the destination address object when preparing the shipment. The existing Local Collect functionality will remain effective if the `pudoId` is not provided.

> 📘 *Note*
>
> *For more information on the new local collect enhancements, refer to the<Anchor label="Use local collect shipment service" target="_blank" href="https://docs.intersoftsapient.net/update/docs/use-local-collect-shipment-service#/">Use local collect shipment service</Anchor> section.*

## Swagger documentation updates

The following updates have been made to the swagger documentation:

* **Get PUDO Locations**. The **GET PUDO Locations** API has been updated to improve its functionality and user experience. Key enhancements include allowing for additional data to be returned from the new Local Collect file and introducing new query parameters for better filtering of pickup and drop-off points. The updates include the following:
  * The **Get PUDO Locations** endpoint has been updated to modify the default value for the **MaximumResults** field from 30 to 10 when a maximum number of locations is not specified by the customer.
  * The existing **locationId** field has been modified to return Royal Mail's unique ID for locations, replacing the previous postcode response.
  * A new **enhancedLocationDetails** object is included in the **GET PUDO Locations** API response when the **includeEnhancedLocationDetails** query parameter is set to true, providing more detailed information about the PUDO locations.

> 📘 *Note*
>
> *For more information on the new local collect enhancements, refer to the<Anchor label="Use local collect shipment service" target="_blank" href="https://docs.intersoftsapient.net/update/docs/use-local-collect-shipment-service#/">Use local collect shipment service</Anchor> section.*

* **Royal Mail Create Shipment API endpoint**. A new **pudoId** field has been added to the **Address** object in the Royal Mail Create Shipment request, allowing the capture of the Location ID returned by the **Get PUDO Locations** endpoint. This optional field is only valid for the destination address in Royal Mail shipments and is essential for collection shipments.

## Offline barcoding shipments

Royal Mail customers can now create Offline Barcoding shipments without requiring a fully matching postcode in the Gazetteer. This enhancement allows customers using offline barcoding to generate pre-advice and OBA data for existing shipments that have "non-matching" postcodes, enabling accurate billing. This change aims to reduce the number of uncharged shipments and streamline the billing process for Royal Mail's Offline Barcoding customers.

## Royal Mail domestic and international label templates

All Royal Mail’s international and domestic label templates have been updated to include the King’s crown in the Royal Mail cruciform logo. This enhancement ensures that customers can generate labels that meet the latest Royal Mail standards, keeping the SAPIENT system compliant with ongoing updates to the bespoke shipping solution.

<Image align="center" border={true} caption="Royal Mail new logo example" src="https://files.readme.io/22779b14c0d377c9cdf45cdb2845b229d69c87b26709b8535d3921c658e7df86-Delivered_By-min.jpg" width="500px" />

## InPost integration (coming soon)

A new InPost integration is coming soon! This integration aims to enhance your shipping experience with improved functionality and efficiency. Stay tuned for more updates, as we will provide further details on features and availability shortly.

***

## Royal Mail SFTP and PUDO API updates

The Royal Mail Collect + locations are now integrated into the **SFTP** and **PUDO** API, allowing you to easily access and create shipments for collection from Collect + points. This addition provides greater flexibility and convenience for users, streamlining the collection process for their shipments.

## The Delivery Group integration

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

## FedEx integration

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
> *For more information on how to set up a FedEx shipping account via the SAPIENT UI, refer to the[Add FedEx shipping account](https://docs.intersoftsapient.net/docs/add-fedex-shipping-account#/) section of our carrier-specific user guides.*

## New SupplementaryUnits field

A new field **supplementaryUnits** has been added to the **Items** object in the **Create Shipment** request. This field can be used to provide the measure of supplementary units for HS codes that support this, for example, the number of pieces, litres or square metres of the item. The unit of measure for the supplementary units does not need to be provided, as this is determined by the HS Code itself (litres, square metres, and so on).

For more information on this field, see the field description in the Create Shipment request under the [API References](https://docs.intersoftsapient.net/reference/get_v4-carriers#/) page.

***

## Royal Mail heavy weight services

The maximum combined dimension validation for Royal Mail heavy weight services has been updated. This is done for accurate validation based solely on individual parcel dimensions, in line with our parcel specifications. This change facilitates a smoother shipment creation process, improving the overall user experience for customers utilising Royal Mail heavy weight services.

## Tracking event enhancements

INTERSOFT's **PRID** tracking event code has now been mapped to the **In Transit** milestone, replacing its previous association with the **It’s on its way** milestone. This change aims to provide customers opting for tracking milestones with clearer visibility of their shipment's journey through the Royal Mail network, accurately reflecting its status and enhancing overall transparency in the tracking process.

## Royal Mail collection booking

The Royal Mail collection logic for shipments has been updated that allows the system to default the dimensions and format based on the weight of the shipment, applying the maximum dimensions specified on our website for each format:

* Shipments weighing 750g or under will be classified as Large Letters.
* Shipments weighing between 751g and 2kg will be classified as Small Parcels.
* Shipments weighing over 2kg up to 20kg will be classified as Medium Parcels.

This change aims to ensure that collections are accepted based on the actual weight and format of the parcels, enhancing the overall shipping experience for our customers.

***

## Maintenance

Routine back-end work and minor UI improvements were addressed and deployed.

***

## Maintenance

Routine back-end work and minor UI improvements were addressed and deployed.

***

## Maintenance

Routine back-end work and minor UI improvements were addressed and deployed.

***

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
    * **Get Account**: Retrieve details of a specific DX Freight shipping account.
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