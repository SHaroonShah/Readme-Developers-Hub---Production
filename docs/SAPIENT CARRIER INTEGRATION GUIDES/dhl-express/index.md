---
title: DHL Express
excerpt: >-
  DHL is the global leader in the logistics industry. DHL Express is a brand
  within the DHL Group known for its expedited delivery, both domestically
  within UK and internationally to EU and Rest of the World destinations.
deprecated: false
hidden: true
icon: fad fa-truck-fast
metadata:
  robots: index
---
The integration of DHL Express into the SAPIENT platform is a significant step in enhancing shipping capabilities. This section discusses the in-scope features of this integration and the services this carrier offers.

## Key features

This integration provides the following key features:

* **Ship from destinations**: The integration supports shipping from locations in Great Britain (GB) only.
* **Ship To Destinations**: Users can send shipments domestically within  Great Britain (GB), Europe (EU), and Rest of the World (<Glossary>ROW</Glossary>).
* **Service Type**: The integration is focused on outbound shipping only.
* **Incoterms**: <Glossary>DDU</Glossary>, <Glossary>DDP</Glossary>, <Glossary>DAP</Glossary>, and <Glossary>DAT</Glossary>.
* Label formats: <Glossary>PDF</Glossary> and <Glossary>PNG</Glossary>.

## Service enhancements

DHL Express supports a range of shipment enhancements, each of which must be used in conjunction with the appropriate DHL Express enhancement code. 

The following is a list of the key enhancements available through the DHL Express integration, along with their codes:

* **Saturday Delivery (AA)**: Enables delivery on Saturdays, offering greater flexibility in shipping schedules.   
* **Adult Signature (SD)**: Requires an adult signature upon delivery of the shipment, ensuring that the package is received by someone of legal age.
* **Shipment Insurance (II)**: Provides insurance coverage for the shipment against loss or damage. If this enhancement is used, then the InsuranceValue field must be populated.
* **Neutral Label (PP)**: Uses a generic shipment <Glossary>label</Glossary> that does not specify the shipment contents description. With this enhancement, shippers can keep the declared value of a shipment confidential from the final recipient. This service ensures that any document that could disclose the value of the contents is removed from the shipment before it is delivered.
* **Verified Delivery (TF)**: Enables verified delivery using a QR code. DHL sends the QR code to the receiver, who must present it to the courier at the time of delivery.
* **Email Notifications**: Sends email notifications to the recipient regarding shipment status updates. This enhancement does not have a special service code, as it is automatically triggered by the system when the Destination > ContactEmail filed is populated in the Create Shipment request.
* **Dangerous Goods**: 
  * **ID8000 (HK)**: Generates the ID8000 label for shipments containing dangerous goods, ensuring compliance with safety regulations.
  * **Excepted Quantities (HH)**: Specifies shipments that include small quantities of dangerous goods exempt from standard regulations.

<Callout icon="💡" theme="default">
  ### _Tip_

  _For more information on the service enhancements and carrier services, refer to the API References section._
</Callout>

## Additional features

The DHL Express integration supports the following additional features:

* **Consignment services**: DHL Express supports a maximum of 999 packages per consignment. In this case, the SAPIENT maximum of 99 will be used.
* **Hazardous shipments**: Allows creating shipments with class 9 hazardous goods, which includes miscellaneous items that pose a risk during transportation. These shipments must comply with specific regulations and labeling requirements to ensure safe handling and transport.
* **Archive Labels**: Allows saving DHL waybill documents from the create shipment response in the database and includes them in the manifest PDF when shipments are manifested.
* **Paperless Trade (PLT)**: Facilitates international shipping by enabling electronic submission of trade documents via the following two ways:
  * **Use DHL-generated invoices**: DHL creates and sends the invoice electronically to the customs agency on your behalf.
  * **Use SAPIENT-generated invoices**: SAPIENT generates the invoices from shipment data and send them to DHL.

> 📘 _Note_
>
> _For more information on Paperless Trade, refer to the <Anchor label="Add DHL Express shipping account" target="_blank" href="https://docs.intersoftsapient.net/docs/add-dhl-express-shipping-account">Add DHL Express shipping account</Anchor> section._

## Carrier API services

The following API services are provided by the DHL Express integration:

* **Create shipment**: The integration for creating shipments to reflect DHL Express as a primary carrier and allowing users to create shipments using the Create Shipment that returns the label in base64 encoded format.
* **Tracking**: Enables customers to receive tracking updates through their integration with the SAPIENT tracking webhook.
* **Manifest shipment**: Enable customers to retrieve information about shipment manifests created by the system and track when shipments have been successfully manifested with the carrier. For customers who need real‑time updates, we strongly recommend using the INTERSOFT Manifest Webhook to keep track of shipments and their statuses by to receiving real-time updates or notifications whenever specific events occur in the system (such as shipping updates, status changes, and so on).

<br />

