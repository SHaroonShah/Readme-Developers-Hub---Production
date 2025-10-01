---
title: 'Manifest shipments asychronously  '
excerpt: >-
  An _asynchronous (async)_ process enables the system to perform tasks in the
  background without requiring the user to wait for the completion of those
  tasks. 
deprecated: false
hidden: false
icon: fad fa-loader
metadata:
  robots: index
---
## Manifesting shipments via asynchronous process

In the context of the <Glossary>shipment</Glossary> manifesting process, this means that when you submit a <Glossary>manifest</Glossary> request with a large volume of shipments, you will receive an immediate confirmation that their request has been received, while the actual processing of that manifest occurs in the background. You can continue using the system without interruption, improving overall efficiency.

This section provides detailed instructions and information regarding the asynchronous shipment manifesting process for customers using the shipment manifest API or by [setting up the manifest webhook](https://docs.intersoftsapient.net/docs/manifest-webhook#/) in SAPIENT.

The primary purpose of implementing an asynchronous manifesting process is to:

* **Enhanced performance**: By processing manifest requests in the background, the system avoids performance bottlenecks, especially when handling large volumes of shipments simultaneously.
* **Improved user experience**: You can submit requests without waiting for long processing times and can continue performing other tasks while the shipments are being manifested.
* **Utilise queueing system**: The requests are managed through a queueing system to ensure they are processed sequentially without overwhelming the system, allowing for more reliable service.

> 🚧 _Important_
>
> _We recommend using the **Manifest Shipments Async** API endpoint to manifest your shipments. However, if you are manifesting more than 20k shipments, then you must only use this endpoint to ensures that requests are processed through the new asynchronous queue, enabling better system performance and improved tracking._

### Manifesting via API

To manifest the shipments in an asynchronous manner via the API, you can use the following endpoints introduced in our core **Manifests** API endpoint:

<Accordion title="Manifest Shipments Async">
  With this endpoint, you can submit the manifest requests to be processed asynchronously. This endpoint accepts the same parameters as the existing [Manifests](https://docs.intersoftsapient.net/reference/post_v4-manifests-carriercode#/) endpoint, excluding the async parameter.

  A successful async manifest response returns the following parameters:

  * **ManifestRequestID**: GUID to uniquely identify the manifest request.
  * **ManifestStatus**: Status of the request, defaults to `PENDING`.
  * **ManifestCount**: Number of manifests created, which will be 0 when initially set to `PENDING`.

  **Example request**

  ```
  {  
   "ShippingLocationId": "16f91589-cb07-430f-aed8-6c0c025bdc32",  
   "ShippingAccountId": "24a8da75-a148-415c-802e-e37a72acfa7f",  
   "ServiceCode": "CRL1"  
  } 
  ```

  Example response (🟢200 - Successful)

  ```
  {  
   "ManifestRequestId": "3a0c17c5-0ca4-455c-ac65-a20d95e656bc",  
   "ManifestRequestStatus": "PENDING",  
   "ManifestCount": 0  
  }
  ```
</Accordion>

<Accordion title="Get Manifest Request Status">
  With this endpoint, you can check the status of a submitted manifest request. In this endpoint, you must consider the following request parameters:

  * **manifestDetail**: An optional parameter, if set to `false` or not populated, the response will include:

  → **manifestId**

  → **manifestStatus**

  → **manifestCount**

  If this parameter is set to `true`, and the status is `COMPLETE`, then a full manifest information response will be returned, including manifest images. If the status is `FAILED`, an error will be returned in the response.

  **Example request**

  ```
  {
  "ManifestRequestId": "3a0c17c5-0ca4-455c-ac65-a20d95e656bc"
  "ManifestDetail":"true"
  }  
  ```

  **Example response**(🟢200 - Successful)

  ```
  {  
   "ManifestRequestId": "3a0c17c5-0ca4-455c-ac65-a20d95e656bc",  
   "ManifestRequestStatus": "IN PROGRESS"  
   "ManifestCount": 0  
  }
  ```
</Accordion>

#### **See also**

* [Set up manifest webhook](https://docs.intersoftsapient.net/docs/manifest-webhook#/)
* [Manifest shipments via UI](https://docs.intersoftsapient.net/docs/manifesting-shipments#/)
* [View manifest history](https://docs.intersoftsapient.net/docs/manifest-history#/)

<br />
