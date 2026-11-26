---
title: Use DPD Local collection service
excerpt: >-
  The DPD Local collection service allows you to arrange the collection of an
  existing shipment through SAPIENT. You can retrieve available collection
  timeslots, book a collection for a selected timeslot, and cancel an existing
  collection when required
deprecated: false
hidden: true
icon: fad fa-cart-flatbed
link:
  new_tab: false
metadata:
  robots: index
---
The **Collection** service supports collections from GB addresses only and can be used for both pre-labelled and unlabelled (Bring My Label) collections.

<Callout icon="🚧" theme="warning">
  ### _Important_

  _Before using this feature, make sure to enable the&#x20;_**_Collect_**_&#x20;integration via the&#x20;_[_integration activation_](https://docs.intersoftsapient.net/docs/integration-activation)_&#x20;page._
</Callout>

## Prerequisites

After activating the intergration and before booking a collection, make sure you have completed the following prerequisites:&#x20;

- Create the shipment and retain the `shipmentId` or tracking number returned for the shipment. This identifies the shipment when using the collection APIs.
- Retrieve the available collection timeslots before attempting to book a collection. This is a prerequisite for booking a DPD collection.
- Ensure the collection is from a GB address. DPD does not support collections from addresses outside GB.

## Retrieve available collection timeslots

Use the **Get Collections Timeslots** API endpoint to retrieve the available dates and time windows for the shipment.

You can request collection from either:

- the shipper address associated with the shipment; or
- an alternative collection address, by providing the collection postcode and country code.

If you do not provide an alternative postcode and country code, SAPIENT uses the shipper postcode and country code from the shipment.

The response provides the available collection date, start time, end time, and the applicable cut-off time.

<Callout icon="far fa-circle-info" theme="info">
  ### **_Note_**

  _DPD does not provide a timeslot ID. When booking the collection, provide the date and time of the timeslot you selected._
</Callout>

## Book collection

Once you have selected an available timeslot, use the **Book Collection** API endpoint to arrange the collection for your existing shipment.

When booking a collection for your shipment:

- Provide the selected collection date and start/end times.
- Provide the collection address and contact details, even when the collection address is the same as the sender address.
- Ensure a contact name and telephone number are available because these are required for DPD collections.
- Use BringMyLabel if the shipment requires the driver to provide the label. If it is not provided, it defaults to false.

After a successful booking, SAPIENT stores the collection details against the shipment so they can be used if the collection is subsequently cancelled.

## Cancel collection

If the collection is no longer required, use the **Cancel Collection** API endpoint and provide the shipmentId or tracking number for the shipment. SAPIENT retrieves the required collection information from the existing shipment record and submits the cancellation to DPD.

When the cancellation is successful, SAPIENT returns a success response and updates the shipment to indicate that the collection has been cancelled.

***

### See also

<Cards columns="2">
  <Card title="API References" icon="fa-solid fa-code" target="_blank">
    Explore the DPD Local API endpoints for a seamless shipping experience.
  </Card>
</Cards>