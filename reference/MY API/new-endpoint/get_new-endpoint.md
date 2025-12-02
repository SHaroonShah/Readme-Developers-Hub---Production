---
title: Create Shipment
excerpt: This is your first endpoint! Edit this page to start documenting your API.
api:
  file: my-api.json
  operationId: get_new-endpoint
hidden: false
---
<br />

Indicates the operation to be performed for the shipment, determines the shipment status that is set on shipment creation and whether a shipment tracking number and labels are generated.

Valid values are:

**Process**: Creates a shipment tracking number, generates and prints a label for each package in the shipment, and returns the labels in the createShipment response. With this action, the shipment status is set to Ready to Manifest.

**Create**: Creates the shipment but does not allocate a tracking number, print the labels or return them in the createShipment response. The label(s) must be printed before the shipment is ready to manifest.
Allocate: Creates the tracking number and label but does not print the labels or return them in the createShipment response. The label(s) must be printed before the shipment is ready to manifest.

_**Note**_: By default, this field is set to Process. Please be advised that if the shipment is created using a consignment service (shipments with multiple packages) with a partner carrier—via the Create or Allocate actions—then the system will split the packages into multiple individual shipments without generating the consignment number.
