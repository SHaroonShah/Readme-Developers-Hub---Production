---
title: Use local collect shipment service
excerpt: >-
  _Local collect_ is a convenient delivery service through which you can have
  your parcels sent to a nearby post office or a designated collection point
  instead of your home address. With it, you can choose a preferred location for
  collection, making it easier to pick up packages at your convenience.
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
The [PUDO API](https://docs.intersoftsapient.net/reference/get_v4-pudolocations-carriercode-countrycode-postcode#/) and the [PUDO via SFTP](https://docs.intersoftsapient.net/docs/pudo-data-via-sftp#/) solution enhances the convenience of shipping by allowing you to integrate pick-up and drop-off locations into your shipping processes. This flexibility offers more choices in how and where you receive you orders. Currently, these locations include Post Offices (POL), Customer Service Points (CSP), and PSH (parcel Shops) via the Local Collect CSV file. When you send the [Get PUDO Locations](https://docs.intersoftsapient.net/reference/get_v4-pudolocations-carriercode-countrycode-postcode#/) request, the data imported from this file is used to determine the available PUDO locations that are returned in the response for your to choose.

<Image align="center" className="border" border={true} width="400px" src="https://files.readme.io/fc9948cba5b87c15e89ceda1d55fe6f022a938bb2b8661ace1f6f9c9e5572799-Post_office.gif" />

In SAPIENT, the local collect shipments can be created using the Royal Mail [Create Shipment](https://docs.intersoftsapient.net/reference/post_v4-shipments-rm) API.

To make the **LocalCollect** shipment request, it is necessary to provide the following information:

1. The destination's **CompanyName** value must be set to either *c/o\[Location] Post Office* or *c/o\[Location] Enquiry Office*, where \[Location] is a Location Alias / Office Name, e.g. *c/o Cobham Post Office*
2. The **ServiceEnhancements** code—**LocalCollect** must be used.
3. The **Email** or **SMS** notification service enhancement must be used by providing the destination's **ContactPhone** or **ContactEmail** information, so the end consumer can be notified when their item is ready to be collected from the post office.