---
title: Manifest Shipments
excerpt: "By manifesting shipments you declare what shipments are ready for dispatch and will be handed over to the carrier. \r<br />The API allows you to manifest via the below methods (parameters):\r<br />\r<br />- shipping location\r<br />- shipping account\r<br />- shipment status (picked)\r<br />- service code\r<br />- container\r<br />\r<br />Note: If no parameters are set, all shipments in the LabelPrinted or Picked status will be manifested (excluding future dated shipments or shipments assigned to a container).\r<br />\r<br />The API response contains a manifest image which should be printed and handed over to the driver (if required)."
api:
  file: sapient-core-api.json
  operationId: post_v4-manifests-carriercode
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---