---
title: 'Manifest shipments asychronously '
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

> 🚧 _Important_
>
> _We recommend using the **Manifest Shipments Async** API endpoint to manifest your shipments. However, if you are manifesting more than 20k shipments, then you must only use this endpoint to ensures that requests are processed through the new asynchronous queue, enabling better system performance and improved tracking._

***

## Key benefits

<Cards columns="3">
  <Card title="Enhanced Performance" icon="tachometer-alt">
    By processing manifest requests in the background, the system avoids performance bottlenecks, especially when handling large volumes of shipments simultaneously.
  </Card>

  <Card title="Improved User Experience" icon="user-check">
    Submit requests without waiting for long processing times and continue performing other tasks while shipments are being manifested.
  </Card>

  <Card title="Reliable Queueing System" icon="list-ol">
    Requests are managed through a queueing system to ensure they are processed sequentially without overwhelming the system.
  </Card>
</Cards>

***

## Manifesting via API

To manifest the shipments in an asynchronous manner via the API, you can use the following endpoints introduced in our core **Manifests** API endpoint:

> ❗️ _Caution_
>
> _If there are shipments that cannot be manifested, the system will validate only the first 50 shipments and return any associated errors. However, the entire request will fail, and none of the shipments will be manifested._

<Tabs>
  <Tab title="API Integration">
    ### Manifesting via API

    Use the following endpoints introduced in our core **Manifests** API to manifest shipments asynchronously:

    <Accordion title="Manifest Shipments Async" icon="paper-plane">
      Submit manifest requests to be processed asynchronously. This endpoint accepts the same parameters as the existing [Manifests](https://docs.intersoftsapient.net/reference/post_v4-manifests-carriercode#/) endpoint, excluding the async parameter.

      A successful async manifest response returns the following parameters:

      * **ManifestRequestID**: GUID to uniquely identify the manifest request.
      * **ManifestStatus**: Status of the request, defaults to `PENDING`.
      * **ManifestCount**: Number of manifests created, which will be 0 when initially set to `PENDING`.

      **Example request with service code parameter**

      ```json
      {  
       "ShippingLocationId": "16f91589-cb07-430f-aed8-6c0c025bdc32",  
       "ShippingAccountId": "24a8da75-a148-415c-802e-e37a72acfa7f",  
       "ServiceCode": "CRL1"  
      } 
      ```

      **Example response** (🟢200 - Successful)

      ```json
      {  
       "ManifestRequestId": "3a0c17c5-0ca4-455c-ac65-a20d95e656bc",  
       "ManifestRequestStatus": "PENDING",  
       "ManifestCount": 0  
      }
      ```
    </Accordion>

    <br />

    <Accordion title="Get Manifest Request Status" icon="search">
      Check the status of a submitted manifest request using the following parameters:

      * **manifestDetail**: An optional parameter that controls the response detail level:

        → If set to `false` or not populated: Returns basic information (manifestId, manifestStatus, manifestCount)

        → If set to `true` and status is `COMPLETE`: Returns full manifest information including manifest images

        → If set to `true` and status is `FAILED`: Returns error information in the response

      **Example request**

      ```json
      {
      "ManifestRequestId": "3a0c17c5-0ca4-455c-ac65-a20d95e656bc",
      "ManifestDetail": "true"
      }  
      ```

      **Example response** (🟢200 - Successful)

      ```json
      {  
       "ManifestRequestId": "3a0c17c5-0ca4-455c-ac65-a20d95e656bc",  
       "ManifestRequestStatus": "IN PROGRESS",
       "ManifestCount": 0  
      }
      ```
    </Accordion>
  </Tab>

  <Tab title="Webhook Setup">
    ### Webhook Integration

    For automated processing and real-time updates, you can set up manifest webhooks in SAPIENT. This allows you to receive notifications when manifest processing is complete.

    For more information on webhook, refer to the following sections:

    <Cards columns="3">
      <Card title="Set up manifest webhook" href="https://docs.intersoftsapient.net/docs/manifest-webhook#/" icon="fa-solid fa-webhook">
        Configure webhooks to receive real-time notifications about manifest processing status.
      </Card>

      <Card title="Manifest shipments via UI" href="https://docs.intersoftsapient.net/docs/manifesting-shipments#/" icon="fa-solid fa-desktop">
        Learn how to manifest shipments using the SAPIENT user interface.
      </Card>

      <Card title="View manifest history" href="https://docs.intersoftsapient.net/docs/manifest-history#/" icon="fa-solid fa-history">
        Access and review your previous manifest requests and their status.
      </Card>

      <Card title="Manifests API Reference" href="https://docs.intersoftsapient.net/reference/post_v4-manifests-carriercode#/" icon="fa-solid fa-code">
        View the complete API reference for the synchronous manifests endpoint.
      </Card>
    </Cards>
  </Tab>
</Tabs>

<br />
