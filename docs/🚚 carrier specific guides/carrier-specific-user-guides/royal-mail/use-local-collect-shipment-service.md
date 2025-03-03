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
With the Royal Mail’s *click and collect* scheme, many of the UK’s leading small and medium size enterprises can offer their customers the option to collect purchases from a post office branch.

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