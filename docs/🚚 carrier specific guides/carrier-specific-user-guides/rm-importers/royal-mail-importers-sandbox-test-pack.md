---
title: Sandbox Test Pack for Royal Mail import service
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
Before going live on SAPIENT, you are required to complete our Test Pack and submit it. To proceed, make sure to adhere to the following API Test Pack requirements:

* **Labels**- For the required services, you must provide a minimum of 3 <Glossary>labels</Glossary> which have been created by you from requests against our services. These labels must have different destination information, different weights, that are relevant to the service being requested.
* **Manifest/Sales Order Summary**- **Commercial Clearance customers only:** the <Glossary>manifest</Glossary> must be produced by calling the [Manifest Shipments](https://docs.intersoftsapient.net/reference/post_v4-manifests-carriercode) API request for the labels being supplied in the Test Pack.
* **Request and Response examples**\
  **For all customers:** example of an API request and response for creating <Glossary>shipment</Glossary>, cancelling shipment and for manifesting shipment.
  **Additionally for Freight 2 Post customers:** example of an API requests and responses for International Arrivals Containers (A-scan) related calls.
* **Test labels**. Test labels must be printed on a production printer and an image, or a scan of these labels, together with the rest of the required documents shared with us for an initial approval.
* **Test pack submission**. Submit the complete **Test Pack** at [onboarding@intersoft.co.uk](mailto:onboarding@intersoft.co.uk).

> 📘 *Note*
>
> *Once the complete Test Pack is submitted, you can expect to hear from us within 5 working days.*