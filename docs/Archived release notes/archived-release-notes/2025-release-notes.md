---
title: 2025 release notes
excerpt: This section includes the archived release notes published in the year 2025.
deprecated: false
hidden: false
icon: fad fa-page
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
## Mandatory Registered Billing Postcode for Royal Mail production shipping accounts

The **Registered Billing Postcode** field in both the **Add Shipping Account** UI and API is now required in the following scenarios:

* Creating a new **Production** shipping account.
* Switching an existing account from **Sandbox** to **Production**, if the account does not already have a Registered Billing Postcode.

This change ensures compliance with Royal Mail’s account validation and sign-off process requirements and improves data accuracy during onboarding.

## Automated OBA Access Code retrieval for Royal Mail

The SAPIENT system now supports automatic retrieval of OBA Access Codes when adding a new Royal Mail shipping account, updating the Royal Mail shipping accounts from **Sandbox** to **Production**, or linking a new shipping location to an existing shipping account via UI and API. This enhancement leverages Royal Mail’s new **Get Access Code** API to validate account details in real time and eliminate the current 2–5-day approval delay. With it, customers can now experience a faster, more efficient onboarding process without needing manual intervention from the Royal Mail OBA team.

> 📘 _Note_
>
> _For more information on the **OBA Access Code** API and Royal Mail's sign-off process, refer to the [Royal Mail OBA account validation and sign-off](https://docs.intersoftsapient.net/docs/royal-mail-sign-off#/) section._

## Asynchronous shipment manifesting (coming soon)

Soon, a fully asynchronous shipment manifesting process will be introduced across the SAPIENT API and UI, allowing customers to submit manifest requests without waiting for completion.

* **API endpoints**: The following two new endpoints will be added to our existing **Manifests** API endpoint.
  * **Manifest Shipments Async**. To submit the manifest requests to be processed asynchronously. This endpoint accepts the same parameters as the existing [Manifests](https://docs.intersoftsapient.net/reference/post_v4-manifests-carriercode#/) endpoint, excluding the **async** parameter.
  * **Get Manifest Request Status**: To check the status of the submitted manifest request with optional detailed responses, including manifest images when complete.
* **Manifest webhook**: To configure a manifest webhook via the UI to receive automatic updates when a manifest request completes or fails, with retry logic and suspension handling.
* **Manifest via UI**: To get real-time progress on async manifest in a separate pop-up dialog and access to completed manifests through the **Manifest History** page.

## Royal Mail label template updates

The Royal Mail label templates for express weekend services have been updated to include the following:

* **Safeplace**: For parcels that can be left in a designated safeplace location upon delivery, enhancing customer satisfaction by providing flexibility while maintaining security.

<Image align="center" border={true} caption="Safeplace label template example" src="https://files.readme.io/6d6098e15d4c247ea06f60f96df9f0114e93d954391907a5580182c8afcf6232-Safeplace_only.png" width="300px" />

* **DO NOT FLY (LQDG)**: For parcels containing Limited Quantity Dangerous Goods (LQDG) that cannot be transported via air, land, or sea. This label prominently displays the **DO NOT FLY** instruction to prevent mishandling and ensure compliance with the safety regulations.

<Image align="center" border={true} caption="LQDG label template example" src="https://files.readme.io/24456f0cae721db1b9d271895a0dc789e6ccf0a4b62c54be1a0a576166e3a718-LQDG_only.png" width="300px" />

* **Combined Safeplace + DO NOT FLY**: For parcels that are subjected to both safeplace and LQDG. This label includes instructions for leaving the parcel in a safeplace location while also highlighting that the contents are subject to the DO NOT FLY requirement due to hazardous materials.

<Image align="center" border={true} caption="Safeplace and LQDG label template example" src="https://files.readme.io/3f987ccb3d34ed2611cd6c617201043aaba21360a6834d448852a8f21e02c606-Safeplace_and_LQDG.png" width="300px" />

***

## DX Cancel API

The SAPIENT system now directly calls DX’s API to cancel shipments within DX’s system. This enhancement ensures that cancellations are fully registered with DX, helping prevent customers from being mistakenly charged for cancelled shipments.

## Recall cancelled DX shipment

The SAPIENT system now prevents any recall actions for a cancelled DX shipment and ensures the shipment remains in its cancelled state.

## INTERSOFT's new tracking events

The following new tracking events have been added in addition to our existing ones:

| Tracking event code | Event description                               |
| :------------------ | :---------------------------------------------- |
| **IARR**            | Shipment Arrived at Facility                    |
| **ICLR**            | Shipment Customs Cleared                        |
| **IRCO**            | Shipment Ready for Collection from the Facility |

## Royal Mail logo update

The Royal Mail carrier logo has been updated on our ReadMe platform and the **Get Carrier** endpoint response to reflect the new King’s Cruciform emblem. This change honours the latest royal insignia and ensures our visuals stay current and consistent across all touchpoints.

<Image align="center" border={true} width="300px" src="https://files.readme.io/d7a05aaef8593abbeec4d05402e47fb6bf6dccabae93be7f1a6bd58f91b98d85-RM_favicon.png" className="border" />

## Swagger documentation updates

The following enhancements have been made to the swagger documentation:

* **Get PUDO Locations**. The following enhancements have been made to the **Get PUDO Locations** endpoint:
  * The **Get PUDO Locations** endpoint has been enhanced to integrate with the InPost **Locations Points** service, unlocking access to both Automated Parcel Machines (APMs or Lockers) and PUDO shop locations. This enhancement provides greater flexibility and convenience for customers choosing out-of-home delivery and return options.
  * The response example for the **Get PUDO Locations** endpoint in our Swagger documentation has been refined to reflect accurate, up-to-date data, ensuring greater clarity and reliability for customers integrating with our API.
  * The description of the **Labels** field in the Royal Mail Create Shipment response has been updated to reflect the generation of the ID8000 label—provided that the **PrintId8000Label** field in the request parameters is set to true.
  * The query and response field descriptions of all the DX API endpoints have been updated to improve clarity and support correct usage of the API.

***

## Royal Mail ID8000 Label Generation for Class 9 Hazardous Goods

Royal Mail customers can now generate ID8000 label alongside the shipping label for Class 9 hazardous goods in SAPIENT. When creating a hazardous shipment, the **Id8000Category** field must be populated to specify the category, such as Medicines or Perfume. If the **PrintId8000Label** field is set to "yes," both the shipping label and ID8000 label will be included in the API response. For multiple Class 9 items, a single ID8000 label will be produced with all relevant categories checked.

> 📘 _Note_
>
> _The ID8000 labels are valid only within the UK; shipments destined for outside UK will not generate an ID8000 label_.

## Automated OBA Access Code retrieval for Royal Mail (Coming Soon)

Soon, SAPIENT will support automatic retrieval of OBA Access Codes when adding a new Royal Mail shipping account, updating the Roya Mail shipping accounts from **Sandbox** to **Production**, or linking a new shipping location to an existing shipping account via UI and API. This enhancement leverages Royal Mail’s new **Get Access Code** API to validate account details in real time and eliminate the current 2–5-day approval delay. Once live, customers will experience a faster, more efficient onboarding process without needing manual intervention from the Royal Mail OBA team.

## Swagger documentation updates

The following enhancements have been made to the swagger documentation:

* **Get PUDO Locations**. A new **LC5** code has been added to the **SupplementCode** field in the **Get PUDO Locations** API response. The field description has been updated to include this new code and clarify the suppliers associated with each location type.
* **DX endpoint updates**. The query and response field descriptions for the following DX API endpoints have been updated to improve clarity and support correct usage of the API:
  * **Get Accounts**
  * **Add Account**
  * **Get Account**
  * **Update Account**
  * **Link Locations**
  * **Get Associated Locations**
  * **Get Associated Location**
  * **Create Shipment**
  * **Print Label**

***

## HS Code validation enhancement in SAPIENT's core API

The **Hurricane Services** API endpoint of the Sapient Core API is now enhanced to support HS codes longer than 10 digits, enabling accurate code validation for countries like Qatar and Kuwait. The **Commodity Codes Validation** endpoint will send requests to Hurricane’s Quick Check API. In response, two new fields—**originalImportCode** and **originalExportCode**—will be included under the **Items** object, providing the correct codes directly from the Hurricane service. The originalImportCode and originalExportCode fields aren't currently being populated, but have been added to the Commodity Codes Validation response in preparation for future use.

## Return label at package-level in create shipment request

A new field—**ReturnLabelsAtPackageLevel** has been added to the **ShipmentInformation** object of the Create Shipment request within the . This optional field allows customers to choose between returning labels at the shipment-level or at the package-level. Additionally, a **Label** field is also added to the **Packages** object in the Create Shipment response to return a Base64 string of the corresponding label when the **ReturnLabelsAtPackageLevel** field is set to True.

> 📘 _**Note**_
>
> _This functionality is currently**only supported for Royal Mail shipments**. The functionality is available with both consignment and multi-piece shipments. If the shipment is processed with this field populated, the labels will be returned at the package level, including Royal Mail partner carrier labels, if applicable. If using offline barcoding without Royal Mail partner labels, the field will be ignored._

## Get PUDO locations endpoint enhancements

A new **SupplementCode** field has been added to the **EnhancedLocationDetails** object of the **Get PUDO Locations** response. This field contains the Royal Mail supplement code associated with the location. It has been added so that any customers who are using the Get PUDO Locations API but not shipping via Sapient have the correct supplement code available. For customers creating Local Collect shipments via Sapient, the supplement code does **not **need to be provided in the create shipment request - Sapient applies the code automatically when a destinationPudoId is provided.

## InPost integration

The In Post integration has been added to the SAPIENT system, providing users with flexible shipping options, including lookup for convenient locker services for secure parcel pickups via the SAPIENT’s **PUDO Locations** endpoint. This enhancement streamlines shipment management and leverages new capabilities for a better shipping experience.

**New API endpoints**. A new **IN POST** block has been added to our carrier-specific APIs. This block includes the following API endpoints:

* **Shipping Account**
  * **Get Accounts**: Retrieve a list of the InPost shipping accounts.
  * **Add Account**: Add a new InPost shipping account.
  * **Get Account**: Retrieve details of a specific InPost shipping account.
  * **Update Account**: Update details of an existing InPost shipping account.
  * **Link Locations**: Link shipping locations to an InPost shipping accounts.
  * **Get Associated Locations**: Retrieve locations linked to the InPost shipping account.
  * **Get Associated Location**: Retrieve details for a specific InPost associated location.
  * **Shipments**
    * **Create Shipment**: Create a new InPost shipment request.
    * **Print Label**: Generate a label for the InPost shipment.
* **InPost shipping account screen**. As part of the InPost integration in Sapient, customer users and Carrier Account Administrators can now configure the InPost shipping account via the SAPIENT UI for creating shipments. This integration supports both outbound and return shipments using InPost’s eco-friendly parcel locker service across England, Wales, and Scotland. The **Add Shipping Account** screen will now include InPost as a carrier for selection, with mandatory fields required for configuration. Additionally, carrier-specific fields for the InPost integration include a mandatory **Client ID** and a **Bearer token** (to be provided by the carrier).

***

## New international UPS services

The following two new UPS international services have been added in addition to the existing ones.

| Service Name                  | Service Code |
| :---------------------------- | :----------- |
| **UPS Worldwide Economy DDU** | 17           |
| **UPS Economy DDP**           | 72           |

Both services support multipiece shipments and packages up to 99 per shipment (subject to SAPIENT maximum). These additional services aims to enhance the international shipping capabilities, providing customers with more flexible options for their shipping needs.

***

## Royal Mail Local Collect enhancements

The Royal Mail's Local Collect enhancement now provides the following two new location types:

* **Collect+**: Now receiving data from Royal Mail for collect+ location, enabling customers to choose from a wide range of collection points.
* **Lockers**: This location will be available soon as part of the Local Collect enhancement.

This update allows customers to access a broader range of collection points. To utilise these new location types, the customers need to request the **enhancedLocationDetails** object to be returned in the [GET PUDO Locations](https://docs.intersoftsapient.net/reference/get_v4-pudolocations-carriercode-countrycode-postcode#/) response, and save the **locationId** of the chosen location to be sent in the `pudoId` field of the destination address object when preparing the shipment. The existing Local Collect functionality will remain effective if the `pudoId` is not provided.

> 📘 _Note_
>
> _For more information on the new local collect enhancements, refer to the[Use local collect shipment service](https://docs.intersoftsapient.net/update/docs/use-local-collect-shipment-service#/) section._

## Swagger documentation updates

The following updates have been made to the swagger documentation:

* **Get PUDO Locations**. The **GET PUDO Locations** API has been updated to improve its functionality and user experience. Key enhancements include allowing for additional data to be returned from the new Local Collect file and introducing new query parameters for better filtering of pickup and drop-off points. The updates include the following:
  * The **Get PUDO Locations** endpoint has been updated to modify the default value for the **MaximumResults** field from 30 to 10 when a maximum number of locations is not specified by the customer.
  * The existing **locationId** field has been modified to return Royal Mail's unique ID for locations, replacing the previous postcode response.
  * A new **enhancedLocationDetails** object is included in the **GET PUDO Locations** API response when the **includeEnhancedLocationDetails** query parameter is set to true, providing more detailed information about the PUDO locations.

> 📘 _Note_
>
> _For more information on the new local collect enhancements, refer to the[Use local collect shipment service](https://docs.intersoftsapient.net/update/docs/use-local-collect-shipment-service#/) section._

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

> 📘 _Note_
>
> _For more information on how to set up a FedEx shipping account via the SAPIENT UI, refer to the[Add FedEx shipping account](https://docs.intersoftsapient.net/docs/add-fedex-shipping-account#/) section of our carrier-specific user guides._

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
