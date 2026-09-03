---
title: Swagger documentation updates
author: Syed Haroon Shah
hidden: true
published_at: '2025-06-19T08:52:11.360Z'
type: improved
---
The following updates have been made to the swagger documentation:

* **Get PUDO Locations**. The **GET PUDO Locations** API has been updated to improve its functionality and user experience. Key enhancements include allowing for additional data to be returned from the new Local Collect file and introducing new query parameters for better filtering of pickup and drop-off points. The updates include the following:
  * The **Get PUDO Locations** endpoint has been updated to modify the default value for the **MaximumResults** field from 30 to 10 when a maximum number of locations is not specified by the customer.
  * The existing **locationId** field has been modified to return Royal Mail's unique ID for locations, replacing the previous postcode response.
  * A new **enhancedLocationDetails** object is included in the **GET PUDO Locations** API response when the **includeEnhancedLocationDetails** query parameter is set to true, providing more detailed information about the PUDO locations.

> 📘 *Note*
>
> *For more information on the new local collect enhancements, refer to the <Anchor label="Use local collect shipment service" target="_blank" href="https://docs.intersoftsapient.net/update/docs/use-local-collect-shipment-service#/">Use local collect shipment service</Anchor> section.*

* **Royal Mail Create Shipment API endpoint**. A new **pudoId** field has been added to the **Address** object in the Royal Mail Create Shipment request, allowing the capture of the Location ID returned by the **Get PUDO Locations** endpoint. This optional field is only valid for the destination address in Royal Mail shipments and is essential for collection shipments.