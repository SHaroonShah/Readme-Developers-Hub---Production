---
title: 2023 release notes
excerpt: This section includes the archived release notes published in the year 2023.
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
## Back-end updates, performance enhancements and minor UI improvements

Back-end updates, performance enhancements and minor UI improvements.

***

## Improvements to Shipment Processing UI

Improvement to Shipment Processing UI, Narrow by Service will display the first 10 services with the most shipments by default, with the option to expand to show all services. The user will be able to scroll without losing sight of the number of shipments they will be manifesting.

***

## Royal Mail Integration – New International Letterbox-able Services

New International Letter-boxable services have been added to the Royal Mail integration. These can be used for sending single-package shipments to international destinations.

<Image align="center" className="border" border={true} src="https://files.readme.io/9c4301b-image.png" />

***

## Yodel Integration

The Yodel integration has been added to Sapient. The integration supports multi-piece shipments for domestic destinations and single-piece shipments for international destinations. The label will be common for all domestic services and the international services have a different label. The label format will be PDF or PNG.

A new Barcode Range Management screen has been added for customers to add a new barcode range for Yodel shipping accounts. For more information on how to create a Yodel shipment and manage Yodel shipping accounts, see the API reference page and the Yodel API section.

***

## Royal Mail Create Shipment API Updated to Support Multiple Package Offline Barcoding Shipments

The Royal Mail [Create Shipment](https://docs.intersoftsapient.net/reference/post_v4-shipments-rm) request has been updated to allow offline barcoding shipments to contain multiple packages, **when all packages are going to the same destination as part of a single order**.

A new OfflineBarcodes object has been added to the request to allow multiple packages to be specified.

To create a multi-package offline barcode shipment, this new object must be used. The existing OfflineBarcode object only supports single-package shipments.

See the [API Reference](https://docs.intersoftsapient.net/reference/get_v4-shippingaccounts) page and the Royal Mail [Create Shipment](https://docs.intersoftsapient.net/reference/post_v4-shipments-rm) API for more information.

***

## Tracking webhook - Tracking Event Code added to API payload

The Tracking Webhook API payload will contain the tracking event code as well tracking event description.

Please note: The tracking event details are only sent when the tracking webhook is configured to send full tracking; not when it’s configured to send milestones only.

***

## Royal Mail Address Field Lengths Updated to 40 Characters

The maximum length of the address fields in the Royal Mail Create Shipment request has been increased from 35 characters to 40 characters.

This has been updated in the Shipper Address, Destination Address and Return to Sender Address objects.

**For more information, see the[API Reference](https://docs.intersoftsapient.net/reference/get_v4-shippingaccounts) page and the Royal Mail API section.**

***

## New API – Pre-Allocate Royal Mail Tracking Number

A new API has been added to allow a Royal Mail tracking number to be requested before creating a shipment.

This API will pre-allocate a tracking number without generating a shipment or label. The tracking number can then be used in the Create Shipment request to create a shipment using the same service and destination associated with the pre-allocated tracking number.

The API is available for Royal Mail shipments only. **For more information, see the** [API Reference](https://docs.intersoftsapient.net/reference/get_v4-shippingaccounts) page and the Royal Mail API section.

***

## Back-end updates, performance enhancements and minor UI improvements

Back-end updates, performance enhancements and minor UI improvements.

***

## Email Notification Added to Inform Customers of Tracking Webhook Deactivation

If the tracking webhook is deactivated due to one or more failed attempts to send the API call, an email will now be sent to the Contact Email Address set for the customer account to notify the customer the webhook has been deactivated.

***

## Optional Hurricane Services Data Cleansing Checks Added on Shipment Creation

The Hurricane services Item Verification, Prohibited Items and Denied Parties checks can now be configured to run as part of the shipment creation process. For these checks to run, Hurricane services will first need to be enabled on the customer’s account. The customer will then need to enable each check individually in the Hurricane integration screen. Once a Hurricane service has been enabled, Sapient will automatically run that data check each time a dutiable international shipment is created.

> 📘 *Note*
>
> *For more information please contact our[Sales ](onboardng@intersoft.co.uk)team.*

If the Hurricane Item Verification check is enabled, then customers can view details of the HS Code and Item Description changes made by Hurricane from the Shipment Processing screen and choose whether to accept or reject the changes. If the customer chooses to revert to the original values, they can re-print customs documents to ensure this contains the correct data.

> 🚧 *Important*
>
> *The Hurricane data checks can also be completed outside of the shipment creation process by calling the Hurricane Services APIs – see the API Reference section for more details.*

***

## EORI Number Format Validation Added to API and UI

When an **EORI** number is provided in either the createShipment request or Customs Settings UI, Pro Shipping will validate that the number is in a valid format and return an error if the **EORI** number is not valid.

***

## New API - Offline Barcoding Number Range for Royal Mail Shipments

A new API has been added to allow customers who are using Royal Mail offline barcoding (generating labels outside of Sapient) to request a barcode number range. This API will connect to Royal Mail’s systems to obtain a barcode range for the requested service, and return this range in the API response for the customer to store in their labelling system. For more information, see the API Reference page and the Royal Mail API section.

***

## Royal Mail Integration Update

The following updates have been made to the Royal Mail integration, in accordance with Royal Mail’s latest specifications:

* The maximum weight of the Tracked Returns 24 and 48 services has been changed from 30kg to 20 kg.
* The Special Delivery Uncommon Services LA1-LA6 have been removed, as Royal Mail have withdrawn these.
* The Consequential Loss service enhancements have been added. For more information on the available service enhancements, see the API Reference page, Royal Mail createShipment API schema and the carrierSpecifics element.

***

## Shipment Search Updated to Allow Future Date Searching

The **shipment search screen** has been updated to allow searching on future dates as well as past dates. The maximum date range that can be searched on, is 30 days.

***

## Delete Shipping Location via UI

The **Edit Shipping Location UI** screen has been updated to allow shipping locations to be deleted. It will not be possible to delete a shipping location linked to one or more shipping accounts or user accounts; in this scenario, the shipping location must be un-linked from the shipping account/user account via either the API or UI before it can be deleted. In all other scenarios, it will be possible to delete the shipping location.

***

## Royal Mail Integration Updates

The following updates have been made to the Royal Mail integration, in accordance with Royal Mail’s latest specifications:

* The maximum weight of the **Special Delivery Guaranteed** services has been increased from 10KG to 20KG
* The **Tracked 24** and **48 Returns** labels have been updated to match Royal Mail’s latest format. These labels will now contain the gazetteer information (in the same way as this is currently provided for outbound labels) and some minor formatting and wording changes have been made.

***

## What 3 Words field added to createShipment API, Shipping Location APIs and Shipping Location UIs

New fields have been added to the Address elements in the createShipment request, Shipping Location APIs and Shipping Location UI to capture the what3Words value for the address. What3Words is a location app used by many carriers to identify locations with a resolution of approximately 3 meters.

***

## New API – Hurricane Services – Denied Parties

A new Denied Parties API service has been added to the Hurricane Services API – see the API Reference section for full details of this new endpoint. This service allows you to identify if a person, organisation or company that is not permitted to engage in transactions such as sending products or goods to the destination country, because they have been proven to be in violation of international law and have links with a range of criminal activities.

***

## New API – Delete Shipping Location

A new Delete API service has been added to the Shipping Locations API – see the API Reference section for full details of this new API. This allows an existing shipping location to be deleted. It will not be possible to delete a shipping location that is linked to one or more shipping accounts or user accounts; in this scenario the shipping location will need to be un-linked from the shipping account/user account via either the API or UI before it can be deleted. In all other scenarios it will be possible to delete the shipping location.

***

## Shipping Account UI Updated to Allow Shipping Accounts to be Deleted

The Edit Shipping Account UI screen has been updated to allow shipping accounts to be deleted. It will not be possible to delete a shipping account that has Production shipments that are in either an unmanifested or uncancelled state. In all other scenarios, it will be possible to delete the shipping account.

***

## Changes to validation of Shipping Accounts with Account Type of Sandbox

The following changes have been made to the validation of Shipping Accounts that have the Account Type set as Sandbox:

* For Royal Mail Sandbox shipping accounts, the Department Number sent in the createShipment request does not need to be a valid Department for the Royal Mail account
* It will now be possible for a shipping account to be changed from Production to Sandbox if Production shipments have been created for the account. When this is done, the Production shipments will still be available for manifesting in the Manifesting UI.

***

## OBA Access Code Feature Improvements

The process for requesting an OBA access code when onboarding Royal Mail customers in SAPIENT has been updated. When an OBA is requested the user linked to the RM account will receive an email confirmation automatically when the OBA code has been generated. This code is a 7-digit code.\
These changes are designed to make the OBA Access Code request process smoother and more efficient.

***

## Hurricane Integration – first of the non-carrier integration on Sapient

Hurricane Commerce is the international data partner for postal operators, online retailers, eCommerce platforms and carriers. Nothing moves cross-border without the right data and increasing global regulation is providing huge challenges to those involved in cross-border eCommerce trade.

Hurricane is now fully integrated with Sapient, providing a suite of APIs to allow:

* HS Code look-up and validation.
* Prohibited & Restricted goods screening.
* Denied Parties screening.
* Full Landed-Cost duty and tax calculations

***

## Tracking Webhook

Tracking Webhook is a new event-driven API, rather than a request and response-based API. The tracking webhook is a webhook API that sends tracking data to a customer’s endpoint, triggered by the tracking data received from carriers

We have implemented performance improvement fixes and authentication changes for the Push Tracking Events API.

***

## Intersoft SAPIENT has been launched

## Toss the confetti!  — it’s our new Intersoft SAPIENT birthday!

Discover the latest Intersoft SAPIENT releases and features - and get a sneak peek at what's coming soon!

Looking to build an integration, easily create and manage shipments, generate labels, and more!