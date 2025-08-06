---
title: InPost PUDO service
excerpt: >-
  The Pick Up and Drop Off (PUDO) service enables customers to use a convenient
  out of home option to collect or return parcels at designated locations. These
  locations can include Automated Parcel Machines (APMs), that is Parcel Lockers
  and PUDOs (stores), offering greater convenience and flexibility for
  customers. 
deprecated: false
hidden: false
metadata:
  robots: index
---
For this service, InPost utilises the SAPIENT's [Get PUDO Locations](https://docs.intersoftsapient.net/reference/get_v4-pudolocations-carriercode-countrycode-postcode#/) endpoint that allows users to access essential shipping options for both sending and returning packages seamlessly by offering the following options:

* **Pick Up**: Allows customers to choose to collect their parcel from a <Glossary>PUDO</Glossary> point. It is particularly beneficial for those who may not always be available for direct delivery, helping to reduce missed delivery attempts and enhance overall customer satisfaction.
* **Drop-off**: Allows customers to find a location where they can drop off a parcel they want to return.

With this integration, InPost offers the following location types:

* **Lockers**: Convenient parcel lockers available for pickup.
* **Collect +**: A network of retail stores, offering parcel pick up an drop off services.

The SAPIENT's [PUDO API](https://docs.intersoftsapient.net/reference/get_v4-pudolocations-carriercode-countrycode-postcode#/), allows users to retrieve nearby collection points on an ad-hoc basis during checkout ensuring real-time access to essential location information.

SAPIENT not only supports retrieving the PUDO location information, but also the creation of InPost outbound shipments that will be collected from a PUDO location.

<Callout icon="🚧" theme="warn">
  ***Important***

  *Before you can use the PUDO API, make sure you have[enabled the pudo integration](https://docs.intersoftsapient.net/docs/integration-activation) with InPost.*
</Callout>

There are two distinct ways to [create an Inpost shipment](https://docs.intersoftsapient.net/reference/post_v4-shipments-inpost#/) aimed at delivery to a PUDO point:

1. By providing the full address of the PUDO:
   1. The request must include “c/o” with the location name.
   2. The destination's **ContactPhone** or **ContactEmail** information must be provided, so the end consumer can be notified when their item is ready to be collected from the PUDO location.

2. By providing PUDO ID:
   1. The request must include `PudoId`.
   2. The destination's **ContactPhone** or **ContactEmail** information must be provided, so the end consumer can be notified when their item is ready to be collected from the PUDO location.

If the `pudoId` field is included in **Address** object of the InPost Create Shipment request, then SAPIENT recognises the specific InPost location by its unique ID, and the label will be generated with the address information of that PUDO location.

<Callout icon="🚧" theme="warn">
  ***Important***

  *Before providing the`pudoId`, make sure of the following:*

  * *If the`pudoId` is provided for any address other than the destination address, an error will be returned.*
  * *The`pudoId` field is mandatory for B2C shipments.*
  * *The`pudoId` field must not be populated for the returns services. The consumer can drop their return at any parcel locker or PUDO location.*
  * *If the`pudoId` is provided for a carrier that does not use PUDO, an error will be returned.*
  * *If the destination company name includes “c/o” and the`PudoId` is not populated, an error will be returned.*
</Callout>