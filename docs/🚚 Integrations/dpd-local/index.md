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
<Image src="https://files.readme.io/b26280ece7a6768b3fd4eba85780740a3589a1ac583036df185651d98e5073a2-DPD_Local_banner_White.png" align="center" width="900px" />

***

DPD Local offers a range of specialist solutions and services. With over 6,000 drop-off locations throughout the UK, DPD Local gives customers the flexibility to arrange their deliveries around their needs. DPD Local also offers a range of collection services as well as free DPD Local tracking on every booking, whilst international shipping is available to send to one of over 200 countries worldwide at a low cost.

This in an in-house integration, which means that the <Glossary>label</Glossary> will be generated in the SAPIENT system. Additionally, an electronic <Glossary>manifest</Glossary> data file is sent to DPD Local via SFTP when the shipments are manifested.

## Overview

<Tabs>
  <Tab title="Key Features">
    <Cards columns="3">
      <Card title="Shipping Origins" icon="fad fa-location-dot">
        The integration supports shipping from locations in Great Britain (GB) only.
      </Card>

      <Card title="Shipping Destinations" icon="fad fa-globe">
        Users can send <Glossary>shipments</Glossary> to Great Britain (GB), Europe (EU), and the Rest of the World (<Glossary>ROW</Glossary>) destinations.
      </Card>

      <Card title="Service Type" icon="fad fa-truck-fast">
        The integration is focused on outbound shipping.
      </Card>

      <Card title="Incoterms Support" icon="fad fa-file-contract">
        The integration supports <Glossary>DAP</Glossary> and <Glossary>DDP</Glossary> incoterms.
      </Card>

      <Card title="Label Formats" icon="fad fa-tag">
        The integration supports labels in the <Glossary>PDF</Glossary>, <Glossary>ZPL203DPI</Glossary>, and <Glossary>ZPL300DPI</Glossary> formats.
      </Card>
    </Cards>
  </Tab>

  <Tab title="Additional Features">
    The FedEx integration provides the following additional features:

    <Cards>
      <Card title="Consignment Services" icon="fad fa-boxes-stacked">
        <Glossary>consignment</Glossary> services are supported, and DPD Local allows a maximum of 99 <Glossary>package</Glossary>s per consignment.
      </Card>

      <Card title="Future Date Shipments" icon="fad fa-box-circle-check">
        DPD Local allow shipments to be created up to 7 days in advance, but can be extended to 30 days if approved by your DPD Local account manager. If not, then the SAPIENT maximum of 28 days will apply.
      </Card>

      <Card title="Ship to Shop" icon="fad fa-person-carry-box">
        Provides parcel delivery to a selected DPD Pickup location, allowing the recipient to collect the parcel at their convenience.
      </Card>
    </Cards>
  </Tab>

  <Tab title="Service Enhancements">
    The following are the key services are provided by the DPD Local integration:

    <Callout icon="🚧" theme="warn">
      ### _Important_

      _The following service enhancements are not passed through the standard Create Shipment request. Instead, they are configured at the account level. If you require multiple service enhancements, you must configure a separate DPD Local shipping account for each one._
    </Callout>

    <br />

    <Cards>
      <Card title="Proof of Identity" icon="fad fa-id-card">
        Requires the receiver to present valid identification at the point of delivery.
      </Card>

      <Card title="Proof of Age" icon="fad fa-calendar-circle-user">
        Ensures the recipient meets a minimum age requirement, like for age-restricted goods.
      </Card>

      <Card title="Pin Required" icon="fad fa-location-pin-lock">
        A secure PIN is sent to the receiver, which must be provided upon delivery.
      </Card>

      <Card title="Pin Required & Proof of Age" icon="fad fa-location-pin-lock">
        Requires PIN and age verification at the point of delivery for added security.
      </Card>
    </Cards>
  </Tab>

  <Tab title="Carrier Services">
    Will be added soon.
  </Tab>
</Tabs>

***

## API Services

<Tabs>
  <Tab title="Core Services">
    <Callout icon="🚧" theme="warn">
      ### _Important_

      _Please bear in mind that DPD Local have separate specifications for domestic and international shipping along with some other specification for certain types of shipments, such as shipments to Northern Ireland (NI)._
    </Callout>

    <Accordion title="Create Shipment">
      The integration for creating shipments to reflect DPD Local as a primary carrier and allowing users to create individual shipments requests using the Create Shipment endpoint. This in-house integration feature simplifies the process of generating and managing shipping labels in the PDF format by the SAPIENT system. DPD Local use routing data to determine if the destination post code and shipment data (such as weight and maximum number of packages) are valid for the service. If the data is valid, then the routing data is printed on the generated label.

      <Callout icon="📘" theme="info">
        ### _Note_

        _The system only imports the data for services that are in scope and does not add any additional services into the integration. It only updates the routing data for the existing service codes._
      </Callout>
    </Accordion>

    <Accordion title="Manifest Shipment (via SFTP)">
      Generates an electronic manifest data file in the SAPIENT's default <Glossary>PDF</Glossary> format and send it to DPD LOCAL via SFTP.
    </Accordion>

    <Accordion title="Get PUDO Locations">
      Enable customers to users to access essential shipping options for both sending and returning packages seamlessly via the [Get PUDO Locations endpoint](https://docs.intersoftsapient.net/reference/get_v4-pudolocations-carriercode-countrycode-postcode).
    </Accordion>
  </Tab>

  <Tab title="Other Services">
    <Accordion title="Print Label">
      [Generate and return the label](https://docs.intersoftsapient.net/reference/get_v4-shipments-printlabel-inpost-shipmentid) for a DPD Local shipment in the PDF format. This endpoint must be utilised when the label is not generated in the InPost Create Shipment request.

      <Callout icon="📘" theme="info">
        ### _Note_

        _This endpoint changes the status of the shipment to label printed. This endpoint should be called at the time of actual printing or label creation, depending on how your business operates. Shipments must be updated to label printed status prior to manifesting._
      </Callout>
    </Accordion>

    <Accordion title="Tracking integration (via SFTP)">
      This integration allows customers to monitor their shipments in real-time, providing transparency and peace of mind. Users can access detailed tracking information, including, real-time updates, tracking numbers, and delivery notifications. For DPD Local shipments, the data files are sent via SFTP.
    </Accordion>
  </Tab>
</Tabs>

***

## Getting Started

<Tabs>
  <Tab title="Account Setup">
    <Cards>
      <Card title="Add DPD Local Shipping Account" href="https://docs.intersoftsapient.net/docs/add-dpd-local-shipping-account" icon="far fa-truck" target="_blank">
        Set up your DPD Local shipping account to start creating shipments.
      </Card>

      <Card title="Add DPD Local Tracking Account" href="https://docs.intersoftsapient.net/docs/add-dpd-local-tracking-account" icon="far fa-search-location" target="_blank">
        Configure tracking for your DPD Local shipments.
      </Card>
    </Cards>
  </Tab>

  <Tab title="API References">
    will be added soon
  </Tab>
</Tabs>

<Banner isInline={true} message="Ready to integrate?" color="#ffb600" textColor="#ffffff" fontSize="20px" fontWeight="bold" width="120px" />

<Cards>
  <Card title="Activate this integration" href="https://docs.intersoftsapient.net/docs/integration-activation#/" icon="far fa-circle-play" target="_blank">
    For more information on how to activate the DPD Local integration, refer to the Activate integration section.
  </Card>
</Cards>