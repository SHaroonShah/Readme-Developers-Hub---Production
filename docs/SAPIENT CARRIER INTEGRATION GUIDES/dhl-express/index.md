---
title: DHL Express
excerpt: >-
  DHL is the global leader in the logistics industry. DHL Express is a brand
  within the DHL Group known for its expedited delivery, both domestically
  within UK and internationally to EU and Rest of the World destinations.
deprecated: false
hidden: false
metadata:
  robots: index
---
The DHL Express integration supports outbound shipping from Great Britain to domestic, European, and Rest of the World destinations through SAPIENT.

***

DHL is the global leader in the logistics industry. DHL Express is a brand within the DHL Group known for expedited delivery, both domestically within the UK and internationally to EU and Rest of the World destinations.

## Overview

<Tabs>
  <Tab title="Key Features">
    <Cards columns={2}>
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

    <br />
  </Tab>

  <Tab title="Additional Features">
    <Cards columns={1}>
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

        * **Use DHL-generated invoices**: DHL creates and sends the invoice electronically to the customs agency on your behalf.
        * **Use SAPIENT-generated invoices**: SAPIENT generates the invoices from shipment data and sends them to DHL.
      </Card>
    </Cards>

    <br />

    <Callout icon="📘" theme="default">
      ### *Note*

      *For more information on Paperless Trade, refer to the<Anchor label="Add DHL Express shipping account" target="_blank" href="https://docs.intersoftsapient.net/docs/add-dhl-express-shipping-account">Add DHL Express shipping account</Anchor> section.*
    </Callout>
  </Tab>

  <Tab title="Service Enhancements">
    <Cards columns={2}>
      <Card title="Saturday Delivery (AA)" icon="fa-solid fa-calendar-day">
        Enables delivery on Saturdays, offering greater flexibility in shipping schedules.
      </Card>

      <Card title="Adult Signature (SD)" icon="fa-solid fa-signature">
        Requires an adult signature upon delivery of the shipment, ensuring that the package is received by someone of legal age.
      </Card>

      <Card title="Shipment Insurance (II)" icon="fa-solid fa-shield-halved">
        Provides insurance coverage for the shipment against loss or damage. If this enhancement is used, then the InsuranceValue field must be populated.
      </Card>

      <Card title="Neutral Label (PP)" icon="fa-solid fa-tag">
        Uses a generic shipment <Glossary>label</Glossary> that does not specify the shipment contents description. With this enhancement, shippers can keep the declared value of a shipment confidential from the final recipient. This service ensures that any document that could disclose the value of the contents is removed from the shipment before it is delivered.
      </Card>

      <Card title="Verified Delivery (TF)" icon="fa-solid fa-qrcode">
        Enables verified delivery using a QR code. DHL sends the QR code to the receiver, who must present it to the courier at the time of delivery.
      </Card>

      <Card title="Email Notifications" icon="fa-solid fa-envelope">
        Sends email notifications to the recipient regarding shipment status updates. This enhancement does not have a special service code, as it is automatically triggered by the system when the Destination > ContactEmail field is populated in the Create Shipment request.
      </Card>

      <Card title="ID8000 Dangerous Goods (HK)" icon="fa-solid fa-exclamation-triangle">
        Generates the ID8000 label for shipments containing dangerous goods, ensuring compliance with safety regulations.
      </Card>

      <Card title="Excepted Quantities (HH)" icon="fa-solid fa-flask">
        Specifies shipments that include small quantities of dangerous goods exempt from standard regulations.
      </Card>
    </Cards>

    <br />

    <Callout icon="💡" theme="default">
      ### *Tip*

      *For more information on the service enhancements and carrier services, refer to the API References section.*
    </Callout>
  </Tab>
</Tabs>

***

## API Services

<Tabs>
  <Tab title="Core Services">
    <Accordion title="Create Shipment" icon="plus-circle">
      The integration for creating shipments to reflect DHL Express as a primary carrier and allowing users to create shipments using the Create Shipment that returns the label in base64 encoded format.
    </Accordion>

    <br />

    <Accordion title="Manifest Shipment" icon="plus-circle">
      Enables customers to retrieve information about shipment manifests created by the system and track when shipments have been successfully manifested with the carrier. For customers who need real‑time updates, we strongly recommend using the INTERSOFT Manifest Webhook to keep track of shipments and their statuses by receiving real-time updates or notifications whenever specific events occur in the system, such as shipping updates and status changes.
    </Accordion>
  </Tab>

  <Tab title="Other Services">
    <Accordion title="Tracking" icon="print">
      Enables customers to receive tracking updates through their integration with the SAPIENT tracking webhook.
    </Accordion>

    <br />

    <Accordion title="Archive Labels" icon="print">
      Allows saving DHL waybill documents from the create shipment response in the database and includes them in the manifest PDF when shipments are manifested.
    </Accordion>
  </Tab>
</Tabs>

***

## Getting Started

<Tabs>
  <Tab title="Account Setup">
    <Cards columns={2}>
      <Card title="Add DHL Express Shipping Account" icon="fa-solid fa-truck" href="https://docs.intersoftsapient.net/docs/add-dhl-express-shipping-account">
        Set up your DHL Express shipping account to start creating shipments.
      </Card>

      <Card title="Add DHL Express Tracking Account" icon="fa-solid fa-search-location" href="https://docs.intersoftsapient.net/docs/add-dhl-express-tracking-account">
        Configure tracking for your DHL Express shipments.
      </Card>
    </Cards>
  </Tab>

  <Tab title="API References">
    <Cards columns={2}>
      <Cards columns={2}>
      <Card title="SAPIENT DHL Express API" icon="fa-solid fa-code" href="">
        Explore the Amazon API endpoints for a seamless shipping experience.
      </Card>
    </Cards>

      <Card title="Review DHL Express services" icon="fa-solid fa-list-check">
        Review the DHL Express features, service enhancements, and API services before activating the integration.
      </Card>
    </Cards>
  </Tab>
</Tabs>

<br />
