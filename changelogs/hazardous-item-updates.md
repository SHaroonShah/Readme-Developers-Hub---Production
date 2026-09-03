---
title: Hazardous Item Updates
author: Laura Price
hidden: true
published_at: '2026-02-23T13:14:35.599Z'
type: improved
---
The validation rules applied to hazardous items have been updated. The fields **UNCode**, **Quantity**, and **UnitOfMeasure** have changed from mandatory to conditional. These fields do not need to be provided for hazardous items, but if any of these fields is provided then all three must be. This change applies to the Royal Mail Create Shipment Request, Add Product and Update Product API requests, Get Product and Get Products API responses, and the Products UI.

> 📘 _Note_
>
> _For more details on the API updates, refer to the <Anchor label="API References" target="_blank" href="https://docs.intersoftsapient.net/reference/">API References</Anchor> page._

<br />

<br />