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
icon: fad fa-map-location
metadata:
  robots: index
---
Use the InPost Pick Up and Drop Off (PUDO) service to retrieve collection and drop-off locations, then create outbound shipments for delivery to a PUDO point.

SAPIENT uses the [Get PUDO Locations](https://docs.intersoftsapient.net/reference/get_v4-pudolocations-carriercode-countrycode-postcode#/) endpoint to return available InPost PUDO locations. You can use this endpoint during checkout to show nearby collection points in real time.

SAPIENT also supports creating InPost outbound shipments that will be collected from a PUDO location.

## Supported PUDO options

<Cards columns={2}>
  <Card title="Pick Up" icon="fa-solid fa-truck-ramp-box">
    Let customers collect their parcel from a <Glossary>PUDO</Glossary> point. This option helps reduce missed delivery attempts when customers are not available for direct delivery.
  </Card>

  <Card title="Drop-off" icon="fa-solid fa-map-location-dot">
    Let customers find a location where they can drop off a parcel they want to return.
  </Card>
</Cards>

## Location types

<Columns layout="auto">
  <Column>
  >  ### Lockers

    Convenient parcel lockers available for pickup.
  </Column>

  <Column>
  >  ### Parcel shops

    Retail stores that offer parcel pickup and drop-off services.
  </Column>
</Columns>

## Prerequisite

> 🚧 _Important_
>
> _Before you use the PUDO API, make sure you have [enabled the PUDO integration](https://docs.intersoftsapient.net/docs/integration-activation) with InPost._

## Create shipments to a PUDO point

To [create an InPost shipment](https://docs.intersoftsapient.net/reference/post_v4-shipments-inpost#/) for delivery to a PUDO point, provide the PUDO ID in the request.

The request must include:

* `PudoId`
* The destination **ContactPhone** or **ContactEmail**, so the end consumer can be notified when their item is ready to collect from the PUDO location

If the `pudoId` field is included in the **Address** object of the InPost Create Shipment request, SAPIENT recognises the specific InPost location by its unique ID. The label is then generated with the address information of that PUDO location.

> 🚧 _Important_
>
> _Before providing the `pudoId`, make sure of the following:_
>
> * _If the `pudoId` is provided for any address other than the destination address, an error will be returned._
> * _The `pudoId` field is mandatory for B2C shipments._
> * _The `pudoId` field must not be populated for returns services. The consumer can drop their return at any parcel locker or PUDO location._
> * _If the `pudoId` is provided for a carrier that does not use PUDO, an error will be returned._
