---
title: New API – Pre-Allocate Royal Mail Tracking Number
author: Intersoft
hidden: true
published_at: '2023-08-18T12:50:45.230Z'
type: added
---
A new API has been added to allow a Royal Mail tracking number to be requested before creating a shipment. 

This API will pre-allocate a tracking number without generating a shipment or label. The tracking number can then be used in the Create Shipment request to create a shipment using the same service and destination associated with the pre-allocated tracking number. 

The API is available for Royal Mail shipments only. **For more information, see the** [API Reference](https://docs.intersoftsapient.net/reference/get_v4-shippingaccounts) page and the Royal Mail API section.\*\*