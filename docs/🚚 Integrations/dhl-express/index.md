---
title: DHL Express
excerpt: >-
  DHL is the global leader in the logistics industry. DHL Express is a brand
  within the DHL Group known for its expedited delivery, both domestically
  within UK and internationally to EU and Rest of the World destinations.
deprecated: false
hidden: false
icon: fad fa-truck-fast
metadata:
  robots: noindex
---
The DHL Express integration supports outbound shipping from Great Britain to domestic, European, and Rest of the World destinations through SAPIENT.

***

DHL is the global leader in the logistics industry. DHL Express is a brand within the DHL Group known for expedited delivery, both domestically within the UK and internationally to EU and Rest of the World destinations.

## Overview

<Tabs>
  <Tab title="Key Features">
    <Cards>
      <Card title="Shipping Origins" icon="fa-map-marker-alt">
        The integration supports shipping from locations in Great Britain (GB) only.
      </Card>

      <Card title="Shipping Destinations" icon="fa-solid fa-globe">
        Users can send shipments domestically within Great Britain (GB), Europe (EU), and Rest of the World (<Glossary>ROW</Glossary>).
      </Card>

      <Card title="Service Type" icon="fa-solid fa-shipping-fast">
        The integration is focused on outbound shipping only.
      </Card>

      <Card title="Incoterms Support" icon="fa-solid fa-file-contract">
        The integration supports <Glossary>DDU</Glossary>, <Glossary>DDP</Glossary>, <Glossary>DAP</Glossary>, and <Glossary>DAT</Glossary>.
      </Card>

      <Card title="Label Formats" icon="fa-solid fa-tag">
        <Glossary>PDF</Glossary> and <Glossary>PNG</Glossary>.
      </Card>
    </Cards>
  </Tab>

  <Tab title="Additional Features">
    <Cards>
      <Card title="Consignment Services" icon="fa-solid fa-boxes-stacked">
        DHL Express supports a maximum of 999 packages per consignment. In this case, the SAPIENT maximum of 99 will be used.
      </Card>

      <Card title="Hazardous Shipments" icon="fa-solid fa-triangle-exclamation">
        Allows creating shipments with class 9 hazardous goods, which includes miscellaneous items that pose a risk during transportation. These shipments must comply with specific regulations and labelling requirements to ensure safe handling and transport.
      </Card>

      <Card title="Archive Labels" icon="fa-solid fa-box-archive">
        Allows saving DHL waybill documents from the create shipment response in the database and includes them in the manifest PDF when shipments are manifested.
      </Card>

      <Card title="Paperless Trade (PLT)" icon="fa-solid fa-file-invoice">
        Facilitates international shipping by enabling electronic submission of trade documents in the following two ways:

        - **Use DHL-generated invoices**: DHL creates and sends the invoice electronically to the customs agency on your behalf.
        - **Use SAPIENT-generated invoices**: SAPIENT generates the invoices from shipment data and sends them to DHL.
      </Card>
    </Cards>

    <Callout icon="📘" theme="default">
      ### _Note_

      _For more information on Paperless Trade, refer to the <Anchor target="_blank" href="https://docs.intersoftsapient.net/docs/add-dhl-express-shipping-account">Add DHL Express shipping account</Anchor> section._
    </Callout>
  </Tab>

  <Tab title="Service Enhancements">
    The following are the key services enhancements provided by the DHL Express integration:

    - **Saturday Delivery (AA)**: Enables delivery on Saturdays, offering greater flexibility in shipping schedules.
    - **Adult Signature (SD)**: Requires an adult signature upon delivery of the shipment, ensuring that the package is received by someone of legal age.
    - **Shipment Insurance (II)**: Provides insurance coverage for the shipment against loss or damage. If this enhancement is used, then the InsuranceValue field must be populated.
    - **Neutral Label (PP)**: Uses a generic shipment <Glossary>label</Glossary> that does not specify the shipment contents description. With this enhancement, shippers can keep the declared value of a shipment confidential from the final recipient. This service ensures that any document that could disclose the value of the contents is removed from the shipment before it is delivered.
    - **Verified Delivery (TF)**: Enables verified delivery using a QR code. DHL sends the QR code to the receiver, who must present it to the courier at the time of delivery.
    - **Email Notifications**: Sends email notifications to the recipient regarding shipment status updates. This enhancement does not have a special service code, as it is automatically triggered by the system when the Destination > ContactEmail field is populated in the Create Shipment request.
    - **ID8000 Dangerous Goods (HK)**: Generates the ID8000 label for shipments containing dangerous goods, ensuring compliance with safety regulations.
    - **Excepted Quantities (HH)**: Specifies shipments that include small quantities of dangerous goods exempt from standard regulations.

    <Callout icon="💡" theme="default">
      ### _Tip_

      _For more information on the service enhancements and carrier services, refer to the API References section._
    </Callout>
  </Tab>

  <Tab title="Carrier Services">
    The following key services are provided by the DHL Express integration.

    | Service Name                            | Description                                                                                                                                                                                                 |
    | :-------------------------------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
    | **Express 12:00 documents**             | This service provides time-definite international delivery of document shipments before 12:00 PM on the next possible business day, with full tracking and expedited handling.                              |
    | **Express Domestic 12:00**              | This service provides time-definite domestic delivery before 12:00 PM on the next working day, with full tracking and priority handling for urgent shipments.                                               |
    | **Express Domestic 9:00**               | This service provides early-morning domestic delivery before 9:00 AM on the next working day, ensuring urgent shipments arrive at the start of the business day.                                            |
    | **Express 12:00 non documents**         | This service provides time-definite international delivery of parcels before 12:00 PM on the next possible business day, with customs clearance and full tracking visibility.                               |
    | **Express Worldwide documents**         | This service provides fast international delivery of document shipments by the end of the next possible business day, with door-to-door service and full tracking.                                          |
    | **Express Domestic**                    | This service provides reliable domestic express delivery by the end of the next working day, with full tracking and door-to-door service.                                                                   |
    | **Express Worldwide ROW non documents** | This service provides international delivery of parcels to rest-of-world destinations by the end of the next possible business day or within a few business days, with customs clearance and full tracking. |
    | **Express Worldwide EU non documents**  | This service provides expedited delivery of parcels across Europe, typically by the end of the next working day, with full tracking and customs-enabled processing where applicable                         |
    | **Economy Select documents**            | This service provides cost-effective delivery of document shipments across Europe within a defined number of business days, using road transport with full tracking.                                        |
    | **Economy Select non documents**        | This service provides cost-effective delivery of parcels across Europe within 2–4 business days, offering a balance between speed and cost with full tracking.                                              |
    | **Express 09:00 non documents**         | This service provides early morning international delivery of parcels before 9:00 AM on the next working day, with priority handling and full tracking.                                                     |
    | **Express 10:30 non documents**         | This service provides time-definite international delivery of parcels before 10:30 AM on the next working day, offering expedited transit and full tracking visibility.                                     |
    | **Express 09:00 documents**             | This service provides early morning international delivery of document shipments before 9:00 AM on the next working day, ensuring urgent delivery with priority handling and tracking.                      |
    | **Express 10:30 documents**             | This service provides time-definite international delivery of document shipments before 10:30 AM on the next working day, with expedited transit and full tracking visibility.                              |



    <Callout icon="💡" theme="default">
      ### _Tip_

      _For the most up-to-date carrier services, use the [Get Carrier Services](https://docs.intersoftsapient.net/reference/get_v4-carriers-carriercode-services) endpoint._
    </Callout>
  </Tab>
</Tabs>

***

## API Services

<Tabs>
  <Tab title="Core Services">
    <Accordion title="Create Shipment">
      The integration for creating shipments to reflect DHL Express as a primary carrier and allowing users to create shipments using the Create Shipment that returns the label in base64 encoded format.
    </Accordion>

    <Accordion title="Manifest Shipment">
      Enables customers to retrieve information about shipment manifests created by the system and track when shipments have been successfully manifested with the carrier. For customers who need real‑time updates, we strongly recommend using the INTERSOFT [Manifest Webhook](https://docs.intersoftsapient.net/v4.03/docs/manifest-webhook), which provides updates on manifest requests, allowing you to track the progress and status of shipments prepared for carrier collection and delivery.
    </Accordion>
  </Tab>

  <Tab title="Other Services">
    <Accordion title="Print Label">
      Generate and return the label for DHL Express shipment in the PDF or PNG format. This endpoint must be utilised when the label is not generated in the DHL Express Create Shipment request.

      <Callout icon="📘" theme="info">
        ### _Note_

        _This endpoint changes the status of the shipment to label printed. This endpoint should be called at the time of actual printing or label creation, depending on how your business operates. Shipments must be updated to label printed status prior to manifesting._
      </Callout>
    </Accordion>

    <Accordion title="Tracking">
      Enables customers to receive tracking updates through their integration with the SAPIENT tracking webhook.
    </Accordion>

    <Accordion title="Archive Labels">
      Allows saving DHL waybill documents from the create shipment response in the database and includes them in the manifest PDF when shipments are manifested.
    </Accordion>
  </Tab>
</Tabs>

***

## Getting Started

<Tabs>
  <Tab title="Account Setup">
    <Cards>
      <Card title="Add DHL Express Shipping Account" href="https://docs.intersoftsapient.net/docs/add-dhl-express-shipping-account" icon="fa-solid fa-truck" target="_blank">
        Set up your DHL Express shipping account to start creating shipments.
      </Card>

      <Card title="Add DHL Express Tracking Account" href="https://docs.intersoftsapient.net/docs/add-dhl-express-tracking-account" icon="fa-solid fa-search-location" target="_blank">
        Configure tracking for your DHL Express shipments.
      </Card>
    </Cards>
  </Tab>

  <Tab title="API References">
    <Cards columns="2">
      <Card title="SAPIENT DHL Express API" href="https://docs.intersoftsapient.net/reference/post_v4-shippingaccounts-dhlexpress" icon="fa-solid fa-code" target="_blank">
        Explore the DHL Express API endpoints for a seamless shipping experience.
      </Card>
    </Cards>
  </Tab>
</Tabs>

<Banner isInline={true} message="Ready to integrate?" color="#ffb600" textColor="#ffffff" fontSize="20px" fontWeight="bold" width="120px" />

<Cards>
  <Card title="Activate this integration" href="https://docs.intersoftsapient.net/docs/integration-activation#/" icon="fa-solid fa-circle-play fa-beat" target="_blank">
    Seamlessly connect with DHL Express and manage your shipping operations from a single platform.
  </Card>
</Cards>
