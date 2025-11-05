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

<Accordion title="My Accordion Title" icon="fa-info-circle">
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

<br />
