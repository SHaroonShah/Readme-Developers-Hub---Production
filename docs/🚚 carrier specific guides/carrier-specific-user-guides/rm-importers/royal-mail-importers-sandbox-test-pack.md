---
title: Sandbox test pack for Royal Mail import service
excerpt: >-
  A _test pack_ is a critical step in the implementation process, ensuring a
  smooth transition to the live environment and minimising disruptions in
  shipping operations.
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
Before going live on SAPIENT, you are required to complete our test pack and submit it. To proceed, make sure to adhere to the following API test pack requirements: 

- **Labels**. For the required services, you must provide a minimum of 3 <<glossary:labels>> which have been created by you from requests against our services. These labels must have different destination information, different weights, that are relevant to the service being requested.
- **Manifest/Sales Order Summary**. The <<glossary:manifest>> must be produced by calling the [Manifest Shipments](https://docs.intersoftsapient.net/reference/post_v4-manifests-carriercode) API request for the labels being supplied in the test pack.
- **Request and Response examples**.  
  For all customers: example of an API request and response for creating <<glossary:shipment>>, cancelling shipment and for manifesting shipment.  
  Additionally for Freight 2 Post customer: example of an API request and response for International Arrivals Containers (A-scan) related calls. 
- **Test labels**. Test labels must be printed on a production printer and an image, or a scan of these labels, together with the rest of the required documents are shared with us for an initial approval.
- **Test pack submission**. Submit the complete **Test Pack** at [onboarding@intersoft.co.uk](mailto:onboarding@intersoft.co.uk).

> 📘 _Note_
> 
> _Once the complete test pack is submitted, you can expect to hear from us within 5 working days._