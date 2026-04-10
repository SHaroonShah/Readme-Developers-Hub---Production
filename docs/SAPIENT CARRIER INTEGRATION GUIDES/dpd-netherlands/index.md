---
title: DPD Netherlands (NL)
excerpt: >-
  DPD Netherlands (NL) is the branch of DPD operating in the Netherlands and is
  part of Geopost group.
deprecated: false
hidden: true
icon: fad fa-truck-fast
metadata:
  robots: index
---
DPD NL ship domestically and internationally, and approximately 60% of their outbound volume is cross-border.

The integration of DPD NL into the SAPIENT platform is a significant step in enhancing shipping capabilities. This section discusses the in-scope features of this integration and the services this carrier offers

## Key features

This integration provides the following key features:

* **Ship from destinations**: The integration supports shipping from locations in Netherlands (NL) only.
* **Ship To Destinations**: Users can send shipments domestically within Netherlands, to Great Britain (GB), Europe, and <Glossary>ROW</Glossary> (Rest of the World).
* **Service Type**: The integration is focused on inbounds and outbound shipping.
* **Incoterms**: <Glossary>DAP</Glossary> and <Glossary>DDP</Glossary>.
* **Label formats**: <Glossary>PDF</Glossary>, <Glossary>ZPL203DPI</Glossary>, and <Glossary>ZPL203DPI</Glossary>.

> 📘 _Note_
>
> For returns shipments, the carrier uses the following label formats:
>
> * _QRCode_
> * _QRCodeAndPDF_

## Service enhancements

The following are the key services are provided by the DPD NL integration:

* **Email**: Delivery updates are sent via email. To use this enhancement code, the destination **ContactEmail** must be provided with a valid email address.   
* **SMS**: Delivery updates are sent via SMS. To use this enhancement code, the destination **ContactPhone** field must be provided with a valid phone number.

<Callout icon="💡" theme="default">
  ### _Tip_

  _For more information on the service enhancements and carrier services, refer to the API References section_
</Callout>

## Additional features

The DPD NL integration provides the following additional features:

* **Consignment services**:  Consignment services are supported for all destinations except for GB.

## API Services

The following API services are provided by the DPD NL integration:

* **Create shipment**: The integration for creating shipments to reflect DPD NL as a primary carrier and allowing users to create shipments using the Create Shipment that returns the label in base64 encoded format.
* **Manifest webhook**: 
* **Tracking**: Enables data files to be sent via SFTP and received through the SAPIENT tracking webhook.

<br />
