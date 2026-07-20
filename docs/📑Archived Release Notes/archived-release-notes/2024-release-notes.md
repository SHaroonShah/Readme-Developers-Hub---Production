---
title: 2024 release notes
excerpt: This section includes the archived release notes published in the year 2024.
deprecated: false
hidden: false
icon: fad fa-notes
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
## DX Freight integration (coming soon)

A new DX Freight integration is coming soon! This integration aims to enhance your shipping experience with improved functionality and efficiency. Stay tuned for more updates, as we will provide further details on features and availability shortly.

***

## Swagger documentation updates

The following information has been added to the swagger documentation:

* As part of our CORE API, the description of the **Trackings** endpoint has been updated to clarify that it is now a chargeable service, billing users automatically based on the number of shipments tracked. Previously, customers manually developed endpoints to register tracking numbers for shipments, which is no longer necessary as tracking data will automatically push to their webhook upon creating a tracking account.

## Local collect service enhancements

Based on the Royal Mail’s latest COSS specifications, the **Local Collect** service enhancement has been removed for shipments created using the Royal Mail **Tracked** and **Special Delivery Age Verification** services.

***

## DX integration enhancements

The ability to create a DX shipment to Channel Islands has been added in SAPIENT. With this enhancement, you can now create a shipment in SAPIENT specifically for Channel Islands (that is, a shipment to the GB country code with a postcode beginning with JE (for Jersey) and GY (for Guernsey, Alderney, and Sark)).

***

## Swagger documentation updates

The following information has been added to the swagger documentation:

* A new **Shipping Account ID** parameter has been added to the **Carriers** > **Get Carriers** section as part of our CORE API. This endpoint allows customers to get the list of services associated with a particular shipping account.

***

## Add hazardous details

A new **Hazardous Information** section has been added to the **Create** and **Edit** product screens. This is only applicable for products that have the Hazardous flag set to true. With this feature added, you can edit and manage the hazardous information of your products and use it when creating a shipment for carriers that accept dangerous goods.

***

## Extend BFPO shipments to all Royal Mail services

Customers creating Royal Mail shipments can now use all the available Royal Mail domestic services for shipments to British Forces Post Office (BFPO) destinations. This enhancement provides the customers with a broader range of domestic services offered by Royal Mail including, Standard, Special Delivery, and Tracked services, thus providing more flexibility and convenience for users sending mail to BFPO destinations.

***

## What3words management

The ability to add and edit what3words in shipping addresses has been added. With it, you can identify the customer location with a resolution of approximately 3 meters.

***

## Expired tracking events

Customers that have a webhook set up in SAPIENT, can now receive an ‘Expired’ event via the tracking webhook for shipments that have not received a tracking after a set number of days. This setting is added to the Tracking Webhook configuration screen in SAPIENT, allowing the customers to choose whether they want to receive the expired event or not.

***

## Swagger documentation updates

The following information has been added to the swagger documentation: 

* A new **Manifest Status** endpoint has been added to the **Manifest** section as part of our CORE API. This endpoint allows customers to manifest their shipments in large volumes and efficiently monitor the stages of the manifest status in real-time.
* A new **Manifest Async** endpoint has been added to the **Manifest** section as part of our CORE API.  This endpoint enables the system to process the shipments requests asynchronously, ensuring consistent performance even during high-volume shipment processing.

***

## Receive tracking events after the ‘Delivered’ event

Each tracking account screen now can receive tracking events after the ‘Delivered’ event to enhance the customer’s visibility of their Royal Mail shipment tracking. With it, customers can easily manage their settings through the **Add**, **Edit**, and **View** tracking account screens for Royal Mail, ensuring they receive timely and accurate push notifications on their shipments—and can still choose to receive the events recorded after the delivered event. This enhancement features the logic update of the Sapient system to generate push payloads for Royal Mail tracking accounts based on the newly defined UI setting and the time elapsed since a ‘Delivered’ tracking event.

***

## Swagger documentation updates

The following updated have been made to the swagger documentation: 

* ID8000 Category fields description and available values are updated in Hazmat Information element in Royal Mail Create Shipment Request and APIs under Products section.
* Error Responses for HTTP 400 error has been updated in the Get Time Zones API under Reference Data section.
* Section Description has been updated in the Get Collections Timeslots, Book Collection and Cancel Collection APIs under Collections section in Royal Mail API.

***

## Royal Mail Integration

The Royal Mail **Create Shipment** API response now includes the ‘PartnerDetails’ field. This field is populated when a partnerLabel is used and left blank when a partnerLabel is not used for the shipment. For more information on creating a Royal Mail shipment, please refer to the API reference page and the Royal Mail API section.

***

## Royal Mail Shipments Allowed with all Classes of Dangerous Goods

The Royal Mail integration has been updated to allow customers to create dangerous goods shipments belonging to any class. The previous restriction limiting dangerous goods to Class 9 has been removed. Customers can now create dangerous goods shipments of any accepted class, provided the UN code is in the list of accepted Royal Mail UN codes and the class is in the list of approved classes. The existing ID8000 category remains mandatory only for Class 9 products.

***

## Error Classification and Retry Mechanism Updated in Tracking Webhook

The Tracking Webhook system has been updated to classify all HTTP responses from the carrier API outside the HTTP 200-299 range as errors and return the corresponding error response. Additionally, the retry mechanism has been revised to cease retry attempts to fetch tracking data from the carrier API after 24 hours of continuous failure, following specific retry intervals.

***

## Data Storage Mechanism for Manifested Containers Updated

<br />

The information about manifested containers is now stored in the database for future reference. A new field called ‘Container Status’ has been added to all the relevant Container APIs to store and retrieve the container information based on status. The ‘Container Status’ can either be ‘Active’ or ‘Manifested’. Customers can only add or remove shipments from containers with an ‘Active’ status. Containers can only be manifested if they have an ‘Active’ status. Containers in the ‘Manifested’ status cannot be deleted. 

For example, in the Get Containers API, the query parameters in the API request have been updated to include the optional parameter 'containerStatus,' and the API response now includes the containerStatus field populated with the container's status, either 'Active' or 'Manifested'. For more information on managing shipments in a container, please refer to the API reference page and the Sapient Core API section.

***

## Royal Mail – Swagger Documentation Updated for Get Collections Timeslot Endpoint

The Swagger Documentation for the Royal Mail Get Collections Timeslot endpoint has been updated in the Section Description. This section now includes information on creating collections, obtaining collection timeslots, and cancelling collections for Royal Mail shipments.

***

## EVRi – Swagger Documentation Updated for Contact Phone field

The Swagger Documentation for EVRI Create Shipment endpoint has been updated for Contact Phone field to accept 15 characters only instead of 20 characters.

***

## Royal Mail Type 3 Pre-Advice File Updated to include Container ID

For shipments in a container, the Detail Supplement Record (03) is populated with the supplement code "SO" and the Container ID (truncated to 40 characters if necessary). For shipments not in a container, the Detail Supplement Record (03) will not contain the supplement code “SO”.

***

## Yodel Maximum Weight Validation Source Updated to use Routing File

The Yodel maximum weight validation source for creating shipments has been updated to use the routing file instead of the service information spreadsheet. This change ensures that accurate weight restrictions are applied, maintaining compliance with Yodel regulations during shipment creation.

***

## Shipment Creation to USA Army Post Office (APO) Destinations

Create Shipment endpoint has been updated to include USA Army Post Office (APO) county codes for destination address. The change applies to all current and future carriers. 

The destinations include:

* Armed Forces Pacific (County Code - **AP**)
* Armed Forces Europe (County Code - **AE**)

***

## Shipment Creation to US Unincorporated Territories

<br />

The Royal Mail Create Shipment endpoint now includes four unincorporated territories: 

1. The Virgin Islands
2. American Samoa
3. Guam
4. The Northern Mariana Islands 

> 📘 *Note*
>
> *The State Code on the label uses the ISO Country Code from the request, and the Country on the label is USA. The billing code follows the service billing code for the USA.*

***

## Royal Mail Integration – Archived Services Removed

The following services have been removed from the Royal Mail integration and are no longer in use for shipment creation.

BG3, BP3, DG3, DG6, IE3, IG3, IG6, IP3, IP6, MB3, PS6, PS8, WE3, WG3, WG6, WP3, DP4, IP4, WP4, OZ1, OZ3, OZ4, OZ6, WW1, WW3, WW4, DE1, DG1, DP1, HVC, and HVF.

***

## Royal Mail Integration – New Services Added

### New import services:

* ITI, ITJ, DE9, DEO, DEP, DEQ, DER, DEU, DEV, DEX, DEY, DEZ, DE5, DE7, and DE8. 
* They come with domestic labels as shipments created with these services are entering Great Britain from international locations. All these services are closed, requiring a service contract for use.

### New international cross-border services:

* DE0, ITO, ITQ, ITT, ITV, ITW, IYX, ITY, ITZ, IT1, IT5, IT6, IT7, IT8, IT9, IT0, TIF, and TIH. 
* They come with international labels. All these services are closed and require a service contract for use.

***

## Swagger Documentation Updated

Swagger documentation has been updated as per below:

* **EVRI Create Shipment API** - Description for ‘Packages’ field has been updated to reflect that EVRI supports single-piece shipment only.
* **Royal Mail Create Shipment API** - The County field description has been revised to specify that when provided for the USA, Australia, and Canada, it must contain a valid state code or name.
* **Royal Mail Create Shipment API** - The description for the SpecialistPhoneNumber field has been revised and highlighted in bold for customer reference.

***

## Registered Billing Postcode and Posting Location Postcode added to Royal Mail Account Activation Email

<br />

In readiness to release Royal Mail API for OBA and to improve the Royal Mail onboarding process, an additional step is being introduced by Royal Mail. In addition to the existing validation of the Account number posting location (PLN) and the OBA-registered email address, there will also be the validation of the postcode registered for the billing address as well as the postcode set up against the PLN (Shipping Location Postcode).

The Registered Billing Postcode and Shipping Location Postcode fields have been added to the Royal Mail Account Activation Email. The Registered Billing Postcode field is optional, with its value automatically included in the activation email when provided. Posting Location Postcode is recorded upon customer selection of the shipping location for linking to the shipping account. Activation emails are dispatched to both the Royal Mail OBA team and the activating user. This enhancement aims to improve the Royal Mail onboarding process and reduce activation errors.

***

## Royal Mail Integration – Update to Create Shipment API Request

The Royal Mail create shipment API request has been modified to accommodate a non-GB Return to Sender address. This adjustment aligns with the support for new ETOE services, allowing shipments to feature a US shipper address while facilitating the use of a return to sender address located outside of the UK.

***

## Royal Mail Integration – New International ETOE Services Added

Royal Mail are introducing a set of new International services intended for use by a new Extra-Territorial Office of Exchange (ETOE) in the USA. An ETOE is an office or facility operated by or in connection with a postal operator outside its national territory on the territory of another country.

The ETOE will be shipping into China initially with the potential to expand to other countries in future. Royal Mail are intending to onboard the ETOE onto the shipping platform, and for the ETOE to integrate with the shipping platform to create shipments.

New International Extra-Territorial Office of Exchange (ETOE) services have been added to the Royal Mail integration. The list of services added are ETK, ETL, ETM, ETN, ETO, ETP, ETQ, ETR, ETG, ETH, ETI, ETA, ETB, ETC, ETD, ETE, and ETF. 

These services require a service contract and utilize the International Label template. They are classified as either Personal Correspondence or Non-Personal Correspondence services. The Get Carrier Services API can be called to retrieve the service descriptions. See the API Reference Page and Carriers API section for details.

***

## Royal Mail Integration – OBA Sales Order Create API Updated with Container ID

The OBA Sales Order Create Request sent to Royal Mail for untracked shipments has been updated to include the Container ID instead of the Manifest Number when shipments allocated to a container are manifested. This helps in reflecting the actual containerisation of the shipments and improves tracking and billing accuracy.

***

## Royal Mail Integration – Updated the tracking translation for events EVKLS and EVKLC

The Royal Mail tracking events EVKLS and EVKLC pertain to delivery to a collection point for collection, not to the final delivery. To accurately reflect this, the tracking events EVKLS and EVKLC have been remapped to indicate "Ready for Collection," rather than treating them as "Delivered" events. This ensures that the correct tracking information is sent to customers.

***

## Containers – Number of Add/Remove shipments increased to 10,000

The maximum number of records accepted in the Add/Remove Shipments request under the Containers API has been increased from 99 to 10,000. This means customers can add a maximum of 10,000 shipments to a container or remove a maximum of 10,000 shipments from a container in a single request. This gives greater flexibility for customers using the container functionality and helps in reducing the number of API calls needed to Sapient.

***

## Parcel Collection Service Added

Parcel Collect Service has been added to Royal Mail Integration. This service enables customers to have their parcels collected from any specified address at their preferred timeslot. It is applicable to Royal Mail shipments that have already been created. Should customers omit selecting a preferred timeslot, the first available collection date will be chosen automatically. Please note, the Parcel Collection service does not cover pick-ups from Safeplace locations or areas with animal warnings.

***

## DX Integration Added to Sapient

The integration supports single piece shipments only to domestic destinations. The label formats available are PDF and ZPL. The integration doesn’t support any service enhancements. For more information on creating a DX shipment and managing DX shipping accounts, please refer to the API reference page and the DX API section.

***

## Royal Mail Shipping Account - Registered Billing Postcode Field Added

Registered billing postcode field has been added to Royal Mail Shipping Account API and UI. The field is optional and accepts a GB postcode only. Addition of this field will help Royal Mail in automating the generation of new OBA Access Code API.

***

## Royal Mail Integration – Allow customers to use addresses set in the Address Book

Customers can now utilize the addresses stored in their Address Book when creating a Royal Mail shipment. When customers provide the AddressId in the create shipment request as a Destination/Shipper/Return To Sender address, then the correspondent address in the Address Book will be used and the address will be filled as per the details stored in Address Book. Additionally, this feature will empower customers to seamlessly add addresses to a Shipping Location by leveraging the addresses stored in their Address Book.

***

## Evri Integration – Ability to add multiple Child Client IDs to the main Shipping Account

Customers can now select ‘Child Client Departments’ button on the Shipping Account screen to add or remove Child Client subaccounts. It can enable customers selling multiple brands to create separate subaccounts per brand for creating Evri shipments.

***

## UPS Integration Added

This integration supports multi-piece shipments to domestic and international destinations. The label formats available are PDF, PNG and ZPL. Tracking updates for UPS shipments are also available via the Sapient Tracking Webhook. For more information on creating a UPS shipment and managing UPS shipping accounts, please refer to the API reference page and the UPS API section.

***

## Royal Mail Integration Update to Allow Limited Quantity Dangerous Goods (LQDG)

The Royal Mail integration has been updated to allow shipments to be created containing Limited Quantity Dangerous Goods. LQDG is currently available with Tracked 48 services only and for shipments with a maximum weight of 10kg or less. The Add Product endpoint and Royal Mail Create Shipment endpoint have both been updated to include a Hazmat endpoint which can be used for providing LQDG information, and Hazmat fields have also been added to the Product UI. When a Royal Mail shipment is created with either hazmat information provided in the Create Shipment request or using a stored product with hazmat information provided for the product, it will be validated as an LQDG shipment. Providing the shipment is using a valid service, has a total weight of 10kg or less, and the hazardous UN Class and destination postcode are supported by Royal Mail for LQDG shipments, then the shipment will be successfully created as an LQDG shipment and the label will contain a “Do not fly” statement.

LQDG can also be used with offline barcodes and pre-allocated tracking numbers.

> 📘 *Note*
>
> *See the API Reference page for more information on the updates to the Add Product and Royal Mail Create Shipment endpoints.*

***

## Tracking Webhook – New Event Code Added in the Payload

New Event Code field has been added to the Tracking Webhook payload. Customers using ‘Tracking Webhook’ with configuration set to ‘Milestones only’ will receive full details of the tracking event that triggered the milestone.

***

## New Tracking Event Code Added

New Intersoft Tracking Event code ‘PRET’ has been added for ‘Shipment Retention’ with Milestone name ‘Transit Delay’. This will help customers receiving accurate shipment tracking information for Royal Mail shipments.

***

## New API Added – PUDO Locations

A new API has been added that allows customers to specify a location to pick up or drop off their shipments. The PUDO location is likely to be a Post Office, Local Shop, Retail Outlet etc. For more information on this API, please refer to the API Reference page and the Royal Mail section.

***

## Unmanifested Shipments to be cancelled after 90 Days

Shipments that are currently unmanifested or on hold for more than 90 days from the shipment creation date will be automatically cancelled.

***

## Integration Activation

The integration activation feature has been added to Sapient allowing existing customers to self-serve and self-onboard for all new integrations by navigating through different screens added under the Integration menu. Customers can activate and configure the integration types available for a specific carrier/Integration without the manual intervention from Intersoft Customer Solutions team.

***

## EVRi Integration Added

The integration supports single-package shipments and can be used to ship domestically and internationally. The Evri shipping account allows multiple Child Client IDs to be added under one shipping account which can be used for shipment creation. For more information on creating an Evri shipment and managing Evri shipping accounts, please refer to the API Reference page and the Evri API section.

***

## Yodel Integration Added

The integration supports multi-piece shipments for domestic destinations and single-piece shipments for international destinations. The label will be common for all domestic services, while the international services will have a different label. The label format will be PDF or PNG. 

Additionally, a new Barcode Range Management screen has been added for customers to add new barcode ranges for Yodel shipping accounts. For more information on creating a Yodel shipment and managing Yodel shipping accounts, please refer to the API reference page and the Yodel API section.