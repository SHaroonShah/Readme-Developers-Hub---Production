---
title: Sandbox Test Pack for Royal Mail import service
excerpt: >-
  A _test pack_ is a critical step in the implementation process, ensuring a
  smooth transition to the live environment and minimising disruptions in
  shipping operations.
deprecated: false
hidden: false
icon: fad fa-folder-gear
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
Before going live on SAPIENT, you are required to complete our Test Pack and submit it. To proceed, make sure to adhere to the following API Test Pack requirements:

1. **Create Labels**

   Provide a minimum of 3 <Glossary>labels</Glossary> created by you from requests against our services. These labels must have different destination information and different weights, relevant to the service being requested.

* **Additionally Freight 2 Post customers only:** customs documentation in a form of combined label + CN22 and separate label and CN23. Please see [here ](https://docs.intersoftsapient.net/docs/combined-label#/)for more information on this.

1. **Produce Manifest / Sales Order Summary**

   <Accordion title="Commercial Clearance customers only" icon="fa-solid fa-file-invoice">
     The <Glossary>manifest</Glossary> must be produced by calling the [Manifest Shipments](https://docs.intersoftsapient.net/reference/post_v4-manifests-carriercode) API request for the labels being supplied in the Test Pack.
   </Accordion>

2. **Gather Request and Response Examples**

   Provide an example of an API request and response for each of the following:

   * Creating a <Glossary>shipment</Glossary>
   * Cancelling a shipment
   * Manifesting a shipment
   * **Additionally Freight 2 Post customers only:** example of an API requests and responses for International Arrivals Containers (A-scan) related calls.

3. **Print Test Labels**

   Print test labels on a production printer. Share an image or scan of these labels, together with the rest of the required documents, for initial approval.

4. **Submit the Test Pack** at [onboarding@intersoft.co.uk](mailto:onboarding@intersoft.co.uk).

> 📘 _Note_
>
> _Once the complete Test Pack is submitted, you can expect to hear from us within 5 working days._

<br />
