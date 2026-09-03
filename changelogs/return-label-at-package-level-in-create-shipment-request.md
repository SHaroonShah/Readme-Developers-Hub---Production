---
title: Return label at package-level in create shipment request
author: Syed Haroon Shah
hidden: true
published_at: '2025-07-25T11:03:32.991Z'
type: added
---
A new field—**ReturnLabelsAtPackageLevel** has been added to the **ShipmentInformation** object of the Create Shipment request within the . This optional field allows customers to choose between returning labels at the shipment-level or at the package-level. Additionally, a **Label** field is also added to the **Packages** object in the Create Shipment response to return a Base64 string of the corresponding label when the **ReturnLabelsAtPackageLevel** field is set to True.

> 📘 ***Note***
>
> *This functionality is currently **only supported for Royal Mail shipments**. The functionality is available with both consignment and multi-piece shipments. If the shipment is processed with this field populated, the labels will be returned at the package level, including Royal Mail partner carrier labels, if applicable. If using offline barcoding without Royal Mail partner labels, the field will be ignored.*