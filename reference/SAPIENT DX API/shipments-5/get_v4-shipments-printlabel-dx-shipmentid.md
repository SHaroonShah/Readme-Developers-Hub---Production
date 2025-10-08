---
title: Print Label
excerpt: "Generate and return the label for the DX shipment. This endpoint is utilised after a DX shipment has been created and is meant to facilitate the printing of the label required for that shipment. \r<br />\r<br />***Note:** This endpoint changes the status of the shipment to label printed.This endpoint should be called at the time of actual printing or label creation, depending on how your business operates.Shipments must be updated to label printed status prior to manifesting.*"
api:
  file: sapient-dx-api.json
  operationId: get_v4-shipments-printlabel-dx-shipmentid
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---