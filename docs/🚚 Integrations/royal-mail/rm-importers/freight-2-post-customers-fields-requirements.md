---
title: Field requirements for Freight 2 Post customers
excerpt: >-
  Freight 2 post customers are businesses or organisations that utilise a
  shipping service that combines freight transport with postal delivery methods.
deprecated: false
hidden: false
icon: fad fa-file-circle-exclamation
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
If you are importing goods into the UK via Freight 2 Post route, please ensure to provide the following details.

<Callout icon="🚧" theme="warn">
  ### _Important_

  _The following requirements are Royal Mail specific in addition to Intersoft's mandatory fields._
</Callout>

<Table align={["center","left"]}>
  <thead>
    <tr>
      <th style={{ textAlign: "center" }}>
        Section
      </th>

      <th>
        Required details
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td style={{ textAlign: "center" }}>
        **Shipper**
      </td>

      <td>
        - ContactName - this must be an individual person's name, not a company name.
        - CompanyName
        - ContactEmail
        - ContactPhone
        - Line1
        - Town
        - Postcode
        - CountryCode
      </td>
    </tr>

    <tr>
      <td style={{ textAlign: "center" }}>
        **Destination**
      </td>

      <td>
        - ContactName
        - CompanyName - highly recommended
        - ContactEmail
        - ContactPhone
        - Line1
        - Town
        - Postcode
        - CountryCode
      </td>
    </tr>

    <tr>
      <td style={{ textAlign: "center" }}>
        **Shipment Information**
      </td>

      <td>
        - DescriptionOfGoods
        - DeclaredValue
        - DeclaredWeight
        - CurrencyCode
      </td>
    </tr>

    <tr>
      <td style={{ textAlign: "center" }}>
        **Items**
      </td>

      <td>
        - Quantity
        - Description
        - Value
        - Weight
        - HSCode
        - CountryOfOrigin
      </td>
    </tr>

    <tr>
      <td style={{ textAlign: "center" }}>
        **Customs**
      </td>

      <td>
        - ShippingCharges - please make sure to populate this field either with the exact amount the end customer was charged for shipping or with "0" if the shipping was for free.
      </td>
    </tr>
  </tbody>
</Table>

<Callout icon="📘" theme="info">
  ### _Note_

  _The requirements listed in the preceding table are also specific for Royal Mail customers creating international shipments._
</Callout>
