---
title: Get PUDO locations endpoint enhancements
author: Syed Haroon Shah
hidden: true
published_at: '2025-07-25T11:02:40.199Z'
type: improved
---
A new **SupplementCode** field has been added to the **EnhancedLocationDetails** object of the **Get PUDO Locations** response. This field contains the Royal Mail supplement code associated with the location. It has been added so that any customers who are using the Get PUDO Locations API but not shipping via Sapient have the correct supplement code available. For customers creating Local Collect shipments via Sapient, the supplement code does \*\*not \*\*need to be provided in the create shipment request - Sapient applies the code automatically when a destinationPudoId is provided.