---
title: Use local collect shipment service
excerpt: >-
  _Local collect_ is a convenient delivery service through which customers can
  have their parcels sent to a nearby post office or a designated collection
  point instead of their home address. Recipients can choose their preferred
  location for collection, making it easier to pick up packages at their
  convenience.
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
The PUDO API and the PUDO via SFTP solution enhances the convenience of shipping by allowing you to integrate pick-up and drop-off locations into your shipping processes. This flexibility enables you to offer more choices in how and where you receive you orders. Currently, these locations include Post Offices (POL) and Customer Service Points (CSP) via the Local Collect CSV file.

<Image align="center" className="border" border={true} width="400px" src="https://files.readme.io/fc9948cba5b87c15e89ceda1d55fe6f022a938bb2b8661ace1f6f9c9e5572799-Post_office.gif" />

Royal Mail utilises the **Local Collect** API service to implement and manage this delivery option within its shipping framework. Through the API function, the following functions can be facilitated:

* **Collection point lookup**: enables customers to search for nearby collection points to select the most convenient location for their delivery.
* **Parcel tracking**: provides updates on the status of the parcel and notifications when it is ready for collection.
* **Integrations**: allows businesses to offer the **Local Collect** service at the point of sale, so that the customers can  retrieve an up-to-date list of Post Offices and Royal Mail customer service points, where the item can be held awaiting collection, thereby enhancing the overall customer experience and streamlining the shipping process.

In SAPIENT, the local collect shipments can be created using the Royal Mail [Create Shipment](https://docs.intersoftsapient.net/reference/post_v4-shipments-rm) API.

To make the **LocalCollect** shipment request, it is necessary to provide the following information:

1. The destination's **CompanyName** value must be set to either *c/o\[Location] Post Office* or *c/o\[Location] Enquiry Office*, where \[Location] is a Location Alias / Office Name, e.g. *c/o Cobham Post Office*
2. The **ServiceEnhancements** code—**LocalCollect** must be used.
3. The **Email** or **SMS** notification service enhancement must be used by providing the destination's **ContactPhone** or **ContactEmail** information, so the end consumer can be notified when their item is ready to be collected from the post office.

## Use local collect with TPLMS file

Royal Mail’s Local Collect service is evolving to meet the needs of modern consumers. By enabling customers to send their parcels to more diverse locations and providing a more robust data structure through the TPLMS file format, Royal Mail is enhancing the user experience and ensuring compliance with future shipping requirements

With the introduction of a new TPLMS file, Royal Mail now supports the following new additional location types while also updating the <Glossary>label</Glossary> and <Glossary>pre-advice</Glossary> file.

* **Lockers (LOK)**: Convenient parcel lockers available for pickup.
* **Collect+ Stores (PSH)**: A network of retail outlets, offering parcel collection services.

The following new fields have been introduced in the TPLMS file.

|             Field            | Description                                                                                                                         |
| :--------------------------: | :---------------------------------------------------------------------------------------------------------------------------------- |
|        **Supplier**\*        | Represents the name of the location supplier.                                                                                       |
|     **Supplement Code**\*    | Represents additional identification code for the location supplier.                                                                |
| **Supplier Location Type**\* | Represents the category of the supplier location.                                                                                   |
|        **Unique ID**\*       | Represents a distinct identifier for each collection point.                                                                         |
|        **Label ID**\*        | Represents a unique identifier associated with the shipment label.                                                                  |
|    **What3Words Value**\*    | Represents a precise address identifier for the location.                                                                           |
| **Final Collection Times**\* | Represents specified collection times for each day of the week.                                                                     |
|         **Products**         | Represents the list products accepted at the location.                                                                              |
|      **Max dimensions**      | Represents details regarding parcel size (small, medium, large) and weight limits for parcels that can be accepted at the location. |
|         **Signature**        | Represents whether the location accepts signature or non-signature shipments                                                        |
|         **Services**         | Represents the list of services offered at the location, for example, pick-up, drop-off, print label.                               |
|        **Facilities**        | Represents the information about the available facilities, for example, disabled access, indoor locker, car parking.                |
|  **Additional Information**  | Any additional information associated with the location.                                                                            |

A new `PudoId` field is included in the Royal Mail Create Shipment request to recognise the specific Royal Mail location by its unique ID. When the `PudoId` field is utilised, the label and pre-advice will be generated with the updated information.

> 🚧 *Important*
>
> *If the destination company name includes “c/o” and the`PudoId` is not populated, the existing Local Collect functionality will continue to apply until customers update their integration with SAPIENT.*