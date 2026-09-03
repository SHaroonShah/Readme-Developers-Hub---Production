---
title: >-
  Royal Mail Create Shipment API Updated to Support Multiple Package Offline
  Barcoding Shipments
author: Intersoft
hidden: true
published_at: '2023-09-18T18:52:27.492Z'
type: improved
---
The Royal Mail [Create Shipment](https://docs.intersoftsapient.net/reference/post_v4-shipments-rm) request has been updated to allow offline barcoding shipments to contain multiple packages, **when all packages are going to the same destination as part of a single order**. 

A new OfflineBarcodes object has been added to the request to allow multiple packages to be specified.

 To create a multi-package offline barcode shipment, this new object must be used. The existing OfflineBarcode object only supports single-package shipments.

See the [API Reference](https://docs.intersoftsapient.net/reference/get_v4-shippingaccounts) page and the Royal Mail [Create Shipment](https://docs.intersoftsapient.net/reference/post_v4-shipments-rm) API for more information.