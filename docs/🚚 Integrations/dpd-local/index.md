---
title: DPD Local
excerpt: >-
  DPD Local is part of DPD and Geopost, one of the world’s leading parcel
  delivery networks operating in over 50 countries. DPD Local is a sister
  company to DPD, and used to be called ‘Interlink Express’ until it was
  re-branded to DPD Local in 2017. Like DPD, DPD Local is a major carrier in the
  UK, offering both domestic and international shipping services.
deprecated: false
hidden: true
icon: fad fa-truck-fast
metadata:
  robots: index
---
<Callout icon="🚧" theme="warn">
  ### _Important_

  _This integration is currently under development. The contents are to be updated as soon as possible._
</Callout>

DPD Local offers a range of specialist solutions and services. With over 6,000 drop-off locations throughout the UK, DPD Local gives customers the flexibility to arrange their deliveries around their needs. DPD Local also offers a range of collection services as well as free DPD Local tracking on every booking, whilst international shipping is available to send to one of over 200 countries worldwide at a low cost.

This in an in-house integration, which means that the <Glossary>label</Glossary> will be generated in the SAPIENT system. Additionally, an electronic <Glossary>manifest</Glossary> data file is sent to DPD Local via SFTP when the shipments are manifested.

## Key features

This integration provides the following key features:

* **Ship from destinations**: The integration supports shipping from locations in Great Britain (GB) only.
* **Ship To Destinations**: Users can send <Glossary>shipments</Glossary> to Great Britain (GB), Europe (EU), and the Rest of the World (<Glossary>ROW</Glossary>) destinations.
* **Service Type**: The integration is focused on outbound shipping.
* **Incoterms**: <Glossary>DAP</Glossary> and <Glossary>DDP</Glossary>.
* **Label formats**: <Glossary>PDF</Glossary>, <Glossary>ZPL203DPI</Glossary>, and <Glossary>ZPL300DPI</Glossary>.

## Service enhancements

The following are the key services are provided by the DPD Local integration:

* **Proof of Identity**: Requires the receiver to present valid identification at the point of delivery.
* **Proof of Age**: Ensures the recipient meets a minimum age requirement, like for age-restricted goods.
* **Pin Required**: A secure PIN is sent to the receiver, which must be provided upon delivery.
* **Pin Required & Proof of Age**: Requires PIN and age verification at the point of delivery for added security.

## Additional features

The FedEx integration provides the following additional features:

* **Consignment services**:  <Glossary>consignment</Glossary> services are supported, and DPD Local allows a maximum of 99 <Glossary>package</Glossary>s per consignment.
* **Carrier specific fields**: The **CarrierSpecifics** object contains the following field:
  * **DeliveryInstructions**: To provide any additional instructions to the <Glossary>carrier</Glossary> regarding the delivery of the shipment.

## Carrier Services

Will be added soon.

## API Services

The following API services are provided by the DPD Local integration:

### Core Services

<Callout icon="🚧" theme="warn">
  ### _Important_

  _Please bear in mind that DPD Local have separate specifications for domestic and international shipping along with some other specification for certain types of shipments, such as shipments to Northern Ireland (NI)._
</Callout>

* **Create Shipment**: The integration for creating shipments to reflect Amazon as a primary carrier and allowing users to create individual shipments requests using the Create Shipment endpoint. This in-house integration feature simplifies the process of generating and managing shipping labels in the PDF format by the SAPIENT system. DPD Local use routing data to determine if the destination post code and shipment data (such as weight and maximum number of packages) are valid for the service. If the data is valid, then the routing data is printed on the generated label.

<Callout icon="📘" theme="info">
  ### _Note_

  _The system only imports the data for services that are in scope and does not add any additional services into the integration. It only updates the routing data for the existing service codes._
</Callout>

* **Manifest Shipment (via SFTP)**: Generates an electronic manifest data file in the SAPIENT's default <Glossary>PDF</Glossary> format and send it to DPD LOCAL via SFTP.
* **Get PUDO Locations**: Enable customers to users to access essential shipping options for both sending and returning packages seamlessly via the [Get PUDO Locations endpoint](https://docs.intersoftsapient.net/reference/get_v4-pudolocations-carriercode-countrycode-postcode).

### Other Services

* Print Label: [Generate and return the label](https://docs.intersoftsapient.net/reference/get_v4-shipments-printlabel-inpost-shipmentid) for an InPost shipment in the PDF format. This endpoint must be utilised when the label is not generated in the InPost Create Shipment request.
  <Callout icon="📘" theme="info">
    ### _Note_

    _This endpoint changes the status of the shipment to label printed. This endpoint should be called at the time of actual printing or label creation, depending on how your business operates. Shipments must be updated to label printed status prior to manifesting._
  </Callout>
* **Tracking integration (via SFTP)**: This integration allows customers to monitor their shipments in real-time, providing transparency and peace of mind. Users can access detailed tracking information, including, real-time updates, tracking numbers, and delivery notifications. For DPD Local shipments, the data files are sent via SFTP.

***

<Callout icon="📘" theme="info">
  ### _Note_

  _For more information on how to activate the DPD Local integration, refer to the&#x20;_[Activate integration](https://docs.intersoftsapient.net/docs/integration-activation#/)_&#x20;section._
</Callout>


