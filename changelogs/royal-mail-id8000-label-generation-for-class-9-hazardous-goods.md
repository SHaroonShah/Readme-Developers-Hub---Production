---
title: Royal Mail ID8000 Label Generation for Class 9 Hazardous Goods
author: Syed Haroon Shah
hidden: true
published_at: '2025-08-20T12:34:33.028Z'
type: improved
---
Royal Mail customers can now generate ID8000 label alongside the shipping label for Class 9 hazardous goods in SAPIENT. When creating a hazardous shipment, the **Id8000Category** field must be populated to specify the category, such as Medicines or Perfume. If the **PrintId8000Label** field is set to "yes," both the shipping label and ID8000 label will be included in the API response. For multiple Class 9 items, a single ID8000 label will be produced with all relevant categories checked.

> 📘 *Note*
>
> *The ID8000 labels are valid only within the UK; shipments destined for outside UK will not generate an ID8000 label*.