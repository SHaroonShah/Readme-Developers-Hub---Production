---
title: New SupplementaryUnits field
author: Laura Price
hidden: true
published_at: '2025-06-04T12:16:02.654Z'
type: added
---
A new field **supplementaryUnits** has been added to the **Items** object in the **Create Shipment** request. This field can be used to provide the measure of supplementary units for HS codes that support this, for example, the number of pieces, litres or square metres of the item. The unit of measure for the supplementary units does not need to be provided, as this is determined by the HS Code itself (litres, square metres, and so on).

For more information on this field, see the field description in the Create Shipment request under the [API References](https://docs.intersoftsapient.net/reference/get_v4-carriers#/) page.