---
title: Swagger documentation updates
author: Syed Haroon Shah
hidden: false
published_at: '2026-10-26T10:57:06.388Z'
type: improved
---
The following updates have been made to the swagger documentation:

- As part of the US global trade changes, a new **PGAReferenceNumber** field has been added to the **Items** object of the Create Shipment request to capture the Partner Government Agency (PGA) reference information for shipments to United States and its territories.&#x20;
  <Callout icon="far fa-circle-info" theme="info">
    ### **_Note_**

    _For more information, refer to the&#x20;_[_Create Shipment_](https://docs.intersoftsapient.net/reference/post_v4-shipments-rm)_&#x20;endpoint._
  </Callout>
- The **Items** object description in the **Create Shipment** request has been updated to to correctly indicate the Hurricane validation on the maximum number of items per shipment request, improving clarity and help ensure correct API implementation and usage.