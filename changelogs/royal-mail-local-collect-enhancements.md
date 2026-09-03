---
title: Royal Mail Local Collect enhancements
author: Syed Haroon Shah
hidden: true
published_at: '2025-06-24T13:11:53.837Z'
type: improved
---
The Royal Mail's Local Collect enhancement now provides the following two new location types:

* **Collect+**: Now receiving data from Royal Mail for collect+ location, enabling customers to choose from a wide range of collection points.
* **Lockers**: This location will be available soon as part of the Local Collect enhancement.

This update allows customers to access a broader range of collection points. To utilise these new location types, the customers need to request the **enhancedLocationDetails** object to be returned in the [GET PUDO Locations](https://docs.intersoftsapient.net/reference/get_v4-pudolocations-carriercode-countrycode-postcode#/) response, and save the **locationId** of the chosen location to be sent in the `pudoId` field of the destination address object when preparing the shipment. The existing Local Collect functionality will remain effective if the `pudoId` is not provided.

> 📘 *Note*
>
> *For more information on the new local collect enhancements, refer to the<Anchor label="Use local collect shipment service" target="_blank" href="https://docs.intersoftsapient.net/update/docs/use-local-collect-shipment-service#/">Use local collect shipment service</Anchor> section.*