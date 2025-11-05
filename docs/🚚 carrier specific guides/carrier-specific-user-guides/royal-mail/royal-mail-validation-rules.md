---
title: Royal Mail validation rules
excerpt: >-
  To support seamless parcel shipping and delivery, Royal Mail has implemented a
  set of validation rules that ensure all required data is accurately provided
  to the carrier.
deprecated: false
hidden: true
icon: fad fa-truck-arrow-right
metadata:
  robots: index
---
These validation rules are defined in the Royal Mail Master Data File (MDF), which lists all the available services , destination coverage, and mandatory data fields for each destination. Required fields include—but are not limited to shipment content, business transaction type, and item information.

When creating a shipment, these validation rules verify that all necessary information is present and correctly formatted for each shipping scenario, reducing errors and streamlining the delivery process.

## Scope of validations

The following sections summarises the MDF validation rules, their respective shipment scenarios, and the mandatory fields for each rule. The field are mapped to their typical names for clarity and reference.

<Accordion title="Rule A: All domestic and international DOX shipments" icon="fa-info-circle">
  **Scenario description**: All domestic shipments and international <Glossary>DOX</Glossary> (document) shipments.

  <HTMLBlock>{`
                                  <table>
                                    <thead>
                                      <tr>
                                        <th>API object</th>
                                        <th>Mandatory fields</th>
                                      </tr>
                                    </thead>
                                    <tbody>
                                      <tr>
                                        <td rowspan="5"> <b>Shipper > Address</b></td>
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
                                      <tr>
                                        <td rowspan="4"><b>Destination > Address</b></td>
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
                                    </tbody>
                                  </table>
  `}</HTMLBlock>
</Accordion>

<Accordion title="Rule B: NDX shipments with DDU incoterm" icon="fa-info-circle">
  **Scenario description**: International non-document (<Glossary>NDX</Glossary>) shipments (goods) using <Glossary>DDU</Glossary> incoterm

  <table>
    <tr>
      <th>API object</th>
      <th>Mandatory fields</th>
    </tr>

    <tr>
      <td rowspan="5">Shipper > Address</td>
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

    <tr>
      <td rowspan="4">Destination > Address</td>
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
      <td rowspan="4">Items</td>
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
  </table>
</Accordion>

<Accordion title="Rule C: NDX shipment with DDU incoterm and additional mandatory customs data" icon="fa-info-circle">
  **Scenario description**: International non-document (<Glossary>NDX</Glossary>) shipments (goods) using <Glossary>DDU</Glossary> incoterm, with customs data

  <table>
    <tr>
      <th>API object</th>
      <th>Mandatory fields</th>
    </tr>

    <tr>
      <td rowspan="5">Shipper > Address</td>
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

    <tr>
      <td rowspan="4">Destination > Address</td>
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
      <td rowspan="6">Items</td>
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
  </table>
</Accordion>

<Accordion title="Rule D: NDX shipment with DDU incoterm, customs data, and mandatory receiver contact details" icon="fa-info-circle">
  **Scenario description**: International non-document (<Glossary>NDX</Glossary>) shipments (goods) using <Glossary>DDU</Glossary>, with extra customs data and mandatory receiver contact details

  <table>
    <tr>
      <th>API object</th>
      <th>Mandatory fields</th>
    </tr>

    <tr>
      <td rowspan="5">Shipper > Address</td>
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

    <tr>
      <td rowspan="6">Destination > Address</td>
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

    <tr>
      <td rowspan="6">Items</td>
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
  </table>
</Accordion>

<Accordion title="Rule E: NDX shipment with DDP incoterm and ROW destination" icon="fa-info-circle">
  **Scenario description**: International non-document (<Glossary>NDX</Glossary>) shipments (goods) using <Glossary>DDP</Glossary> incoterm, sent to non-EU destinations, that is Rest of the World (<Glossary>ROW</Glossary>)

  <table>
    <tr>
      <th>API object</th>
      <th>Mandatory fields</th>
    </tr>

    <tr>
      <td rowspan="5">Shipper > Address</td>
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

    <tr>
      <td rowspan="6">Destination > Address</td>
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

    <tr>
      <td rowspan="6">Items</td>
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

    <tr>
      <td rowspan="1">Customs</td>
      <td>QuotedLandedCost</td>
    </tr>
  </table>
</Accordion>

<Accordion title="Rule F: NDX shipment with DDP incoterm and EU destination" icon="fa-info-circle">
  **Scenario description**: International non-document (<Glossary>NDX</Glossary>) shipments (goods) using <Glossary>DDP</Glossary> incoterm, sent to EU destinations

  <table>
    <tr>
      <th>API object</th>
      <th>Mandatory fields</th>
    </tr>

    <tr>
      <td rowspan="5">Shipper > Address</td>
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

    <tr>
      <td>Shipper</td>
      <td>EoriNumber</td>
    </tr>

    <tr>
      <td rowspan="6">Destination > Address</td>
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

    <tr>
      <td rowspan="6">Items</td>
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

    <tr>
      <td>Customs</td>
      <td>QuotedLandedCost</td>
    </tr>
  </table>
</Accordion>

<Accordion title="Rule G: NDX shipment with IOSS information" icon="fa-info-circle">
  **Scenario description**: International non-document (<Glossary>NDX</Glossary>) shipments (goods) with <Glossary>IOSS</Glossary> <Glossary>Pre-registration number</Glossary>

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

    <tr>
      <td rowspan="2"><strong>Customs</strong></td>
      <td>IOSS PreRegistrationNumber</td>
    </tr>

    <tr>
      <td>IOSS PreRegistrationType</td>
    </tr>
  </table>
</Accordion>

<Accordion title="Rule H: NDX shipment with Pre-registration number" icon="fa-info-circle">
  **Scenario description**: International non-document (<Glossary>NDX</Glossary>) shipments (goods) with <Glossary>Pre-registration number</Glossary>

  <table border="1" cellpadding="5" cellspacing="0">
    <thead>
      <tr>
        <th>API object</th>
        <th>Mandatory fields</th>
      </tr>
    </thead>

    <tbody>
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

      <tr>
        <td rowspan="2"><strong>Customs</strong></td>
        <td>Non-IOSS PreRegistrationNumber</td>
      </tr>

      <tr>
        <td>Non-IOSS PreRegistrationType</td>
      </tr>
    </tbody>
  </table>
</Accordion>

<Accordion title="Rule K: B2B shipment" icon="fa-info-circle">
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
  </table>
</Accordion>

<Accordion title="Rule L: NDX shipment with DDP incoterm and Importer details" icon="fa-info-circle">
**Scenario description**: International non-document (<Glossary>NDX</Glossary>) shipments (goods) using <Glossary>DDP</Glossary> incoterm, with importer details required

  <table>
    <tr>
      <th>API object</th>
      <th>Mandatory fields</th>
    </tr>

    <tr>
      <td rowspan="5">Shipper > Address</td>
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

    <tr>
      <td rowspan="2">Shipper</td>
      <td>EoriNumber</td>
    </tr>

    <tr />

    <tr>
      <td rowspan="5">Destination > Address</td>
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

    <tr>
      <td rowspan="2">Destination</td>
      <td>EoriNumber</td>
    </tr>

    <tr />

    <tr>
      <td rowspan="6">Items</td>
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

    <tr>
      <td rowspan="1">Customs</td>
      <td>QuotedLandedCost</td>
    </tr>

    <tr>
      <td rowspan="5">CarrierSpecifics > Importer > Address</td>
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
  </table>
</Accordion>

A. **Scenario description**: All domestic shipments and international <Glossary>DOX</Glossary> (document) shipments.

B. **Scenario description**: International non-document (<Glossary>NDX</Glossary>) shipments (goods) using <Glossary>DDU</Glossary> incoterm

C. **Scenario description**: International non-document (<Glossary>NDX</Glossary>) shipments (goods) using <Glossary>DDU</Glossary> incoterm, with customs data

D. **Scenario description**: International non-document (<Glossary>NDX</Glossary>) shipments (goods) using <Glossary>DDU</Glossary>, with extra customs data and mandatory receiver contact details

E. **Scenario description**: International non-document (<Glossary>NDX</Glossary>) shipments (goods) using <Glossary>DDP</Glossary> incoterm, sent to non-EU destinations, that is Rest of the World (<Glossary>ROW</Glossary>)

F. **Scenario description**: International non-document (<Glossary>NDX</Glossary>) shipments (goods) using <Glossary>DDP</Glossary> incoterm, sent to EU destinations

G. **Scenario description**: International non-document (<Glossary>NDX</Glossary>) shipments (goods) with <Glossary>IOSS</Glossary> <Glossary>Pre-registration number</Glossary>

H. **Scenario description**: International non-document (<Glossary>NDX</Glossary>) shipments (goods) with <Glossary>Pre-registration number</Glossary>

K. **Scenario description**: Shipments with B2B <Glossary>business transaction type</Glossary>.

L. **Scenario description**: International non-document (<Glossary>NDX</Glossary>) shipments (goods) using <Glossary>DDP</Glossary> incoterm, with importer details required

<br />