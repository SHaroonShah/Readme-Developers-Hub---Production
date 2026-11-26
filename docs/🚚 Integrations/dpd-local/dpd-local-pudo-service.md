---
title: Use DPD Local PUDO service
deprecated: false
hidden: true
icon: fad fa-map-location-dot
link:
  new_tab: false
metadata:
  robots: index
---
Use the DPD Local Pick Up and Drop Off (PUDO) service to retrieve collection and drop-off locations, then create outbound shipments for delivery to a PUDO point.

SAPIENT uses the [Get PUDO Locations](https://docs.intersoftsapient.net/reference/get_v4-pudolocations-carriercode-countrycode-postcode#/) endpoint to return available DPD Local PUDO locations. You can use this endpoint during checkout to show nearby DPD Local collection points in real time.

## Supported PUDO options

<Cards columns="2">
  <Card title="Pick Up" icon="fa-solid fa-truck-ramp-box">
    DPD Local supports Ship To Shop services through its Pickup Network, allowing parcels to be delivered to a DPD Local <Glossary>PUDO</Glossary> location. This option helps reduce missed delivery attempts when customers are not available for direct delivery.
  </Card>

  <Card title="Drop-off" icon="fa-solid fa-map-location-dot">
    Let customers find a DPD Local location where they can drop off a parcel they want to return.
  </Card>
</Cards>

## Prerequisite

<Callout icon="🚧" theme="warn">
  ### _Important_

  _Before you use the PUDO API, make sure:&#x20;_

  - _You have &#x20;_[_enabled the PUDO integration_](https://docs.intersoftsapient.net/docs/integration-activation)_&#x20;with InPost_
  - _You have obtained a valid Pickup Location Code before creating a Ship To Shop shipment_
</Callout>

## Create shipments to a PUDO location

To [create an InPost shipment](https://docs.intersoftsapient.net/reference/post_v4-shipments-inpost#/) for delivery to a PUDO point, provide the PUDO ID in the request.

The request must include:

* `PudoId`
* The destination **ContactPhone** or **ContactEmail**, so the end consumer can be notified when their item is ready to collect from the PUDO location.

If the `pudoId` field is included in the **Address** object of the DPD Local Create Shipment request, SAPIENT recognises the specific DP Local location by its unique ID. The label is then generated with the address information of that PUDO location.

<Callout icon="🚧" theme="warn">
  ### _Important_

  _Before providing the&#x20;_`pudoId`_, make sure of the following:_

  * _If the&#x20;_`pudoId`_&#x20;is provided for any address other than the destination address, an error will be returned._
  * _The&#x20;_`pudoId`_&#x20;field is mandatory for B2C shipments._
  * _The&#x20;_`pudoId`_&#x20;field must not be populated for returns services. The consumer can drop their return at any DPD Local PUDO location._
  * _If the&#x20;_`pudoId`_&#x20;is provided for a carrier that does not use PUDO, an error will be returned._
</Callout>

***
