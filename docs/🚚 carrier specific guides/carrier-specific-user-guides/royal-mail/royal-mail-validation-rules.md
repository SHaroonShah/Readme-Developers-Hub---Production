---
title: Royal Mail validation rules
excerpt: >-
  To support seamless parcel shipping and delivery, Royal Mail has implemented a
  set of validation rules that ensure all required data is accurately provided
  to the carrier.
deprecated: false
hidden: true
icon: fad fa-truck-arrow-right
link:
  new_tab: false
metadata:
  robots: index
---
These validation rules are defined in the Royal Mail _Master Data File (MDF)_, which lists all the available services , destination coverage, and mandatory data fields for each destination. Required fields include—but are not limited to shipment content, business transaction type, and item information.

When creating a shipment, these validation rules verify that all necessary information is present and correctly formatted for each shipping scenario, reducing errors and streamlining the delivery process.

## Scope of validations

The following sections summarises the MDF validation rules, their respective shipment scenarios, and the mandatory fields for each rule. The field are mapped to their typical names for clarity and reference.

<Accordion title="All domestic DOX, NDX, and international DOX shipments" icon="fa-solid fa-shield-check">
  **Scenario description**: Domestic <Glossary>DOX</Glossary>, <Glossary>NDX</Glossary>, and international DOX shipments.

  <table>
    <tr>
      <th>API object</th>
      <th>Mandatory fields</th>
    </tr>

    <tr>
      <td rowspan="5"><strong>Shipper > Address</strong></td>
      <td>ContactName</td>
    </tr>

    <tr>
      <td>Line 1</td>
    </tr>

    <tr>
      <td>Town</td>
    </tr>

    <tr>
      <td>Postcode</td>
    </tr>

    <tr>
      <td>CountryCode</td>
    </tr>

    <Banner isInline={true} color="#ffb600" />

    <tr>
      <td rowspan="4"><strong>Destination > Address</strong></td>
      <td>ContactName</td>
    </tr>

    <tr>
      <td>Line 1</td>
    </tr>

    <tr>
      <td>Town</td>
    </tr>

    <tr>
      <td>CountryCode</td>
    </tr>

    <Banner isInline={true} color="#ffb600" />
  </table>
</Accordion>

<Accordion title="International NDX shipments with DDU incoterm" icon="fa-solid fa-shield-check">
  **Scenario description**: International non-document (<Glossary>NDX</Glossary>) shipments using <Glossary>DDU</Glossary> incoterm.

  <table>
    <tr>
      <th>API object</th>
      <th>Mandatory fields</th>
    </tr>

    <tr>
      <td rowspan="5"><strong>Shipper > Address</strong></td>
      <td>ContactName</td>
    </tr>

    <tr>
      <td>Line 1</td>
    </tr>

    <tr>
      <td>Town</td>
    </tr>

    <tr>
      <td>PostCode</td>
    </tr>

    <tr>
      <td>CountryCode</td>
    </tr>

    <Banner isInline={true} color="#ffb600" />

    <tr>
      <td rowspan="4"><strong>Destination > Address</strong></td>
      <td>ContactName</td>
    </tr>

    <tr>
      <td>Line 1</td>
    </tr>

    <tr>
      <td>Town</td>
    </tr>

    <tr>
      <td>CountryCode</td>
    </tr>

    <Banner isInline={true} color="#ffb600" />

    <tr>
      <td rowspan="4"><strong>Items</strong></td>
      <td>Quantity</td>
    </tr>

    <tr>
      <td>Description</td>
    </tr>

    <tr>
      <td>Value</td>
    </tr>

    <tr>
      <td>Weight</td>
    </tr>

    <Banner isInline={true} color="#ffb600" />
  </table>
</Accordion>

<Accordion title="International NDX shipment with DDU incoterm and additional item information" icon="fa-solid fa-shield-check">
  **Scenario description**: International non-document (<Glossary>NDX</Glossary>) shipments using <Glossary>DDU</Glossary> incoterm, with additional item information.

  <table>
    <tr>
      <th>API object</th>
      <th>Mandatory fields</th>
    </tr>

    <tr>
      <td rowspan="5"><strong>Shipper > Address</strong></td>
      <td>ContactName</td>
    </tr>

    <tr>
      <td>Line 1</td>
    </tr>

    <tr>
      <td>Town</td>
    </tr>

    <tr>
      <td>PostCode</td>
    </tr>

    <tr>
      <td>CountryCode</td>
    </tr>

    <Banner isInline={true} color="#ffb600" />

    <tr>
      <td rowspan="4"><strong>Destination > Address</strong></td>
      <td>ContactName</td>
    </tr>

    <tr>
      <td>Line 1</td>
    </tr>

    <tr>
      <td>Town</td>
    </tr>

    <tr>
      <td>CountryCode</td>
    </tr>

    <Banner isInline={true} color="#ffb600" />

    <tr>
      <td rowspan="6"><strong>Items</strong></td>
      <td>Quantity</td>
    </tr>

    <tr>
      <td>Description</td>
    </tr>

    <tr>
      <td>Value</td>
    </tr>

    <tr>
      <td>Weight</td>
    </tr>

    <tr>
      <td>HSCode</td>
    </tr>

    <tr>
      <td>CountryOfOrigin</td>
    </tr>

    <Banner isInline={true} color="#ffb600" />
  </table>
</Accordion>

<Accordion title="International NDX shipment with DDU incoterm, customs data, and mandatory receiver contact details" icon="fa-solid fa-shield-check">
  **Scenario description**: International non-document (<Glossary>NDX</Glossary>) shipments using <Glossary>DDU</Glossary>, with extra customs data and mandatory receiver contact details.

  <table>
    <tr>
      <th>API object</th>
      <th>Mandatory fields</th>
    </tr>

    <tr>
      <td rowspan="5"><strong>Shipper > Address</strong></td>
      <td>ContactName</td>
    </tr>

    <tr>
      <td>Line 1</td>
    </tr>

    <tr>
      <td>Town</td>
    </tr>

    <tr>
      <td>PostCode</td>
    </tr>

    <tr>
      <td>CountryCode</td>
    </tr>

    <Banner isInline={true} color="#ffb600" />

    <tr>
      <td rowspan="6"><strong>Destination > Address</strong></td>
      <td>ContactName</td>
    </tr>

    <tr>
      <td>Line 1</td>
    </tr>

    <tr>
      <td>Town</td>
    </tr>

    <tr>
      <td>CountryCode</td>
    </tr>

    <tr>
      <td>ContactEmail</td>
    </tr>

    <tr>
      <td>ContactPhone</td>
    </tr>

    <Banner isInline={true} color="#ffb600" />

    <tr>
      <td rowspan="6"><strong>Items</strong></td>
      <td>Quantity</td>
    </tr>

    <tr>
      <td>Description</td>
    </tr>

    <tr>
      <td>Value</td>
    </tr>

    <tr>
      <td>Weight</td>
    </tr>

    <tr>
      <td>HSCode</td>
    </tr>

    <tr>
      <td>CountryOfOrigin</td>
    </tr>

    <Banner isInline={true} color="#ffb600" />
  </table>
</Accordion>

<Accordion title="International NDX shipment with DDP incoterm and ROW destination" icon="fa-solid fa-shield-check">
  **Scenario description**: International non-document (<Glossary>NDX</Glossary>) shipments using <Glossary>DDP</Glossary> incoterm, sent to non-EU destinations, that is Rest of the World (<Glossary>ROW</Glossary>).

  <table>
    <tr>
      <th>API object</th>
      <th>Mandatory fields</th>
    </tr>

    <tr>
      <td rowspan="5"><strong>Shipper > Address</strong></td>
      <td>ContactName</td>
    </tr>

    <tr>
      <td>Line 1</td>
    </tr>

    <tr>
      <td>Town</td>
    </tr>

    <tr>
      <td>PostCode</td>
    </tr>

    <tr>
      <td>CountryCode</td>
    </tr>

    <Banner isInline={true} color="#ffb600" />

    <tr>
      <td rowspan="6"><strong>Destination > Address</strong></td>
      <td>ContactName</td>
    </tr>

    <tr>
      <td>Line 1</td>
    </tr>

    <tr>
      <td>Town</td>
    </tr>

    <tr>
      <td>CountryCode</td>
    </tr>

    <tr>
      <td>ContactEmail</td>
    </tr>

    <tr>
      <td>ContactPhone</td>
    </tr>

    <Banner isInline={true} color="#ffb600" />

    <tr>
      <td rowspan="6"><strong>Items</strong></td>
      <td>Quantity</td>
    </tr>

    <tr>
      <td>Description</td>
    </tr>

    <tr>
      <td>Value</td>
    </tr>

    <tr>
      <td>Weight</td>
    </tr>

    <tr>
      <td>HSCode</td>
    </tr>

    <tr>
      <td>CountryOfOrigin</td>
    </tr>

    <Banner isInline={true} color="#ffb600" />

    <tr>
      <td rowspan="1"><strong>Customs</strong></td>
      <td>QuotedLandedCost</td>
    </tr>

    <Banner isInline={true} color="#ffb600" />
  </table>
</Accordion>

<Accordion title="International NDX shipment with DDP incoterm to EU destination" icon="fa-solid fa-shield-check">
  **Scenario description**: International non-document (<Glossary>NDX</Glossary>) shipments using <Glossary>DDP</Glossary> incoterm, sent to EU destinations.

  <table>
    <tr>
      <th>API object</th>
      <th>Mandatory fields</th>
    </tr>

    <tr>
      <td rowspan="5"><strong>Shipper > Address</strong></td>
      <td>ContactName</td>
    </tr>

    <tr>
      <td>Line 1</td>
    </tr>

    <tr>
      <td>Town</td>
    </tr>

    <tr>
      <td>PostCode</td>
    </tr>

    <tr>
      <td>CountryCode</td>
    </tr>

    <Banner isInline={true} color="#ffb600" />

    <tr>
      <td><strong>Shipper</strong></td>
      <td>EoriNumber</td>
    </tr>

    <Banner isInline={true} color="#ffb600" />

    <tr>
      <td rowspan="6"><strong>Destination > Address</strong></td>
      <td>ContactName</td>
    </tr>

    <tr>
      <td>Line 1</td>
    </tr>

    <tr>
      <td>Town</td>
    </tr>

    <tr>
      <td>CountryCode</td>
    </tr>

    <tr>
      <td>ContactEmail</td>
    </tr>

    <tr>
      <td>ContactPhone</td>
    </tr>

    <Banner isInline={true} color="#ffb600" />

    <tr>
      <td rowspan="6"><strong>Items</strong></td>
      <td>Quantity</td>
    </tr>

    <tr>
      <td>Description</td>
    </tr>

    <tr>
      <td>Value</td>
    </tr>

    <tr>
      <td>Weight</td>
    </tr>

    <tr>
      <td>HSCode</td>
    </tr>

    <tr>
      <td>CountryOfOrigin</td>
    </tr>

    <Banner isInline={true} color="#ffb600" />

    <tr>
      <td><strong>Customs</strong></td>
      <td>QuotedLandedCost</td>
    </tr>

    <Banner isInline={true} color="#ffb600" />
  </table>
</Accordion>

<Accordion title="International NDX shipment with IOSS information to EU destination" icon="fa-solid fa-shield-check">
  **Scenario description**: International non-document (<Glossary>NDX</Glossary>) shipments with an <Glossary>IOSS</Glossary> <Glossary>Pre-registration number</Glossary>, shipped to EU destinations.

  <table>
    <tr>
      <th>API object</th>
      <th>Mandatory fields</th>
    </tr>

    <tr>
      <td rowspan="5"><strong>Shipper > Address</strong></td>
      <td>ContactName</td>
    </tr>

    <tr>
      <td>Line 1</td>
    </tr>

    <tr>
      <td>Town</td>
    </tr>

    <tr>
      <td>PostCode</td>
    </tr>

    <tr>
      <td>CountryCode</td>
    </tr>

    <Banner isInline={true} color="#ffb600" />

    <tr>
      <td rowspan="6"><strong>Destination > Address</strong></td>
      <td>ContactName</td>
    </tr>

    <tr>
      <td>Line 1</td>
    </tr>

    <tr>
      <td>Town</td>
    </tr>

    <tr>
      <td>CountryCode</td>
    </tr>

    <tr>
      <td>ContactEmail</td>
    </tr>

    <tr>
      <td>ContactPhone</td>
    </tr>

    <Banner isInline={true} color="#ffb600" />

    <tr>
      <td rowspan="6"><strong>Items</strong></td>
      <td>Quantity</td>
    </tr>

    <tr>
      <td>Description</td>
    </tr>

    <tr>
      <td>Value</td>
    </tr>

    <tr>
      <td>Weight</td>
    </tr>

    <tr>
      <td>HSCode</td>
    </tr>

    <tr>
      <td>CountryOfOrigin</td>
    </tr>

    <Banner isInline={true} color="#ffb600" />

    <tr>
      <td rowspan="2"><strong>Customs</strong></td>
      <td>PreRegistrationNumber populated with the IOSS number</td>
    </tr>

    <tr>
      <td>PreRegistrationType defined as IOSS</td>
    </tr>

    <Banner isInline={true} color="#ffb600" />
  </table>
</Accordion>

<Accordion title="International NDX shipment with Pre-registration number" icon="fa-solid fa-shield-check">
  **Scenario description**: International non-document (<Glossary>NDX</Glossary>) shipments with <Glossary>Pre-registration number</Glossary>.

  <table>
    <tr>
      <th>API object</th>
      <th>Mandatory fields</th>
    </tr>

    <tr>
      <td rowspan="5"><strong>Shipper > Address</strong></td>
      <td>ContactName</td>
    </tr>

    <tr>
      <td>Line 1</td>
    </tr>

    <tr>
      <td>Town</td>
    </tr>

    <tr>
      <td>PostCode</td>
    </tr>

    <tr>
      <td>CountryCode</td>
    </tr>

    <Banner isInline={true} color="#ffb600" />

    <tr>
      <td rowspan="6"><strong>Destination > Address</strong></td>
      <td>ContactName</td>
    </tr>

    <tr>
      <td>Line 1</td>
    </tr>

    <tr>
      <td>Town</td>
    </tr>

    <tr>
      <td>CountryCode</td>
    </tr>

    <tr>
      <td>ContactEmail</td>
    </tr>

    <tr>
      <td>ContactPhone</td>
    </tr>

    <Banner isInline={true} color="#ffb600" />

    <tr>
      <td rowspan="6"><strong>Items</strong></td>
      <td>Quantity</td>
    </tr>

    <tr>
      <td>Description</td>
    </tr>

    <tr>
      <td>Value</td>
    </tr>

    <tr>
      <td>Weight</td>
    </tr>

    <tr>
      <td>HSCode</td>
    </tr>

    <tr>
      <td>CountryOfOrigin</td>
    </tr>

    <Banner isInline={true} color="#ffb600" />

    <tr>
      <td rowspan="2"><strong>Customs</strong></td>
      <td>PreRegistrationNumber</td>
    </tr>

    <tr>
      <td>PreRegistrationType</td>
    </tr>

    <Banner isInline={true} color="#ffb600" />
  </table>
</Accordion>

<Accordion title="International B2B shipment" icon="fa-solid fa-shield-check">
  **Scenario description**: Shipment with B2B <Glossary>business transaction type</Glossary>.

  <table>
    <tr>
      <th>API object</th>
      <th>Mandatory fields</th>
    </tr>

    <tr>
      <td rowspan="5"><strong>Shipper</strong></td>
      <td>ContactName</td>
    </tr>

    <tr>
      <td>Line 1</td>
    </tr>

    <tr>
      <td>Town</td>
    </tr>

    <tr>
      <td>PostCode</td>
    </tr>

    <tr>
      <td>CountryCode</td>
    </tr>

    <Banner isInline={true} color="#ffb600" />

    <tr>
      <td rowspan="3"><strong>Destination</strong></td>
      <td>ContactName</td>
    </tr>

    <tr>
      <td>Line 1</td>
    </tr>

    <tr>
      <td>Town</td>
    </tr>

    <Banner isInline={true} color="#ffb600" />

    <tr>
      <td rowspan="6"><strong>Items</strong></td>
      <td>Quantity</td>
    </tr>

    <tr>
      <td>Description</td>
    </tr>

    <tr>
      <td>Value</td>
    </tr>

    <tr>
      <td>Weight</td>
    </tr>

    <tr>
      <td>HSCode</td>
    </tr>

    <tr>
      <td>CountryOfOrigin</td>
    </tr>

    <Banner isInline={true} color="#ffb600" />
  </table>
</Accordion>

<Accordion title="International NDX shipment with DDP incoterm and Importer details" icon="fa-solid fa-shield-check">
  **Scenario description**: International non-document (<Glossary>NDX</Glossary>) shipments using <Glossary>DDP</Glossary> incoterm, with importer details required.

  <table>
    <tr>
      <th>API object</th>
      <th>Mandatory fields</th>
    </tr>

    <tr>
      <td rowspan="5"><strong>Shipper > Address</strong></td>
      <td>ContactName</td>
    </tr>

    <tr>
      <td>Line1</td>
    </tr>

    <tr>
      <td>Town</td>
    </tr>

    <tr>
      <td>PostCode</td>
    </tr>

    <tr>
      <td>CountryCode</td>
    </tr>

    <Banner isInline={true} color="#ffb600" />

    <tr>
      <td><strong>Shipper</strong></td>
      <td>EoriNumber</td>
    </tr>

    <Banner isInline={true} color="#ffb600" />

    <tr>
      <td rowspan="5"><strong>Destination > Address</strong></td>
      <td>ContactName</td>
    </tr>

    <tr>
      <td>Line 1</td>
    </tr>

    <tr>
      <td>Town</td>
    </tr>

    <tr>
      <td>CountryCode</td>
    </tr>

    <tr>
      <td>ContactPhone</td>
    </tr>
<Banner isInline={true} color="#ffb600" />
    <tr>
      <td><strong>Destination</strong></td>
      <td>EoriNumber</td>
    </tr>

    <Banner isInline={true} color="#ffb600" />

    <tr>
      <td rowspan="6"><strong>Items</strong></td>
      <td>Quantity</td>
    </tr>

    <tr>
      <td>Description</td>
    </tr>

    <tr>
      <td>Value</td>
    </tr>

    <tr>
      <td>Weight</td>
    </tr>

    <tr>
      <td>HSCode</td>
    </tr>

    <tr>
      <td>CountryOfOrigin</td>
    </tr>

    <Banner isInline={true} color="#ffb600" />

    <tr>
      <td><strong>Customs</strong></td>
      <td>QuotedLandedCost</td>
    </tr>

    <Banner isInline={true} color="#ffb600" />

    <tr>
      <td rowspan="4"><strong>CarrierSpecifics > Importer > Address</strong></td>
      <td>ContactName</td>
    </tr>

    <tr>
      <td>Line1</td>
    </tr>

    <tr>
      <td>Town</td>
    </tr>

    <tr>
      <td>CountryCode</td>
    </tr>

    <Banner isInline={true} color="#ffb600" />
  </table>
</Accordion>

***

<Banner isInline={true} color="#ffb600" />
