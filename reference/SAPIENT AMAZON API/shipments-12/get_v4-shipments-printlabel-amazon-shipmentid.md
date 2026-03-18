---
title: Print Label
excerpt: "Generate and return the label for the Amazon shipment. This endpoint is utilised after an Amazon shipment has been created and is meant to facilitate the printing of the label required for that shipment.\r<br />\r<br />***Note:** This endpoint changes the shipment status to \"label printed\"​. This endpoint should be called at the time of actual printing or label creation, depending on how your business operates. Shipments must be updated to label printed status prior to manifesting.*"
api:
  file: sapient-amazon-api.json.json
  operationId: get_v4-shipments-printlabel-amazon-shipmentid
hidden: false
---