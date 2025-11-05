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

<Accordion title="Rule A: " icon="fa-info-circle">
  Lorem ipsum dolor sit amet, **consectetur adipiscing elit.** Ut enim
  ad minim veniam, quis nostrud exercitation ullamco. Excepteur sint
  occaecat cupidatat non proident!

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

<Accordion title="Rule B:" icon="fa-info-circle">
  Lorem ipsum dolor sit amet, **consectetur adipiscing elit.** Ut enim
  ad minim veniam, quis nostrud exercitation ullamco. Excepteur sint
  occaecat cupidatat non proident!

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

<Accordion title="Rule C" icon="fa-info-circle">
  Lorem ipsum dolor sit amet, **consectetur adipiscing elit.** Ut enim
  ad minim veniam, quis nostrud exercitation ullamco. Excepteur sint
  occaecat cupidatat non proident!

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

<Accordion title="Rule D" icon="fa-info-circle">
  Lorem ipsum dolor sit amet, **consectetur adipiscing elit.** Ut enim
  ad minim veniam, quis nostrud exercitation ullamco. Excepteur sint
  occaecat cupidatat non proident!

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

<Accordion title="Rule E" icon="fa-info-circle">
  Lorem ipsum dolor sit amet, **consectetur adipiscing elit.** Ut enim
  ad minim veniam, quis nostrud exercitation ullamco. Excepteur sint
  occaecat cupidatat non proident!

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

<Accordion title="Rule F" icon="fa-info-circle">
  Lorem ipsum dolor sit amet, **consectetur adipiscing elit.** Ut enim
  ad minim veniam, quis nostrud exercitation ullamco. Excepteur sint
  occaecat cupidatat non proident!

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

<Accordion title="Rule G" icon="fa-info-circle">
  Lorem ipsum dolor sit amet, **consectetur adipiscing elit.** Ut enim
  ad minim veniam, quis nostrud exercitation ullamco. Excepteur sint
  occaecat cupidatat non proident!

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

<Accordion title="Rule H " icon="fa-info-circle">
  Lorem ipsum dolor sit amet, **consectetur adipiscing elit.** Ut enim
  ad minim veniam, quis nostrud exercitation ullamco. Excepteur sint
  occaecat cupidatat non proident!

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

<Accordion title="Rule K" icon="fa-info-circle">
  Lorem ipsum dolor sit amet, **consectetur adipiscing elit.** Ut enim
  ad minim veniam, quis nostrud exercitation ullamco. Excepteur sint
  occaecat cupidatat non proident!

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

<Accordion title="Rule L" icon="fa-info-circle">
  Lorem ipsum dolor sit amet, **consectetur adipiscing elit.** Ut enim
  ad minim veniam, quis nostrud exercitation ullamco. Excepteur sint
  occaecat cupidatat non proident!

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

    <tr>
      <td />
    </tr>

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

    <tr>
      <td />
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

<br />
