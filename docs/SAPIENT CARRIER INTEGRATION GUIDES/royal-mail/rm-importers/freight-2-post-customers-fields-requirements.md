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

> 🚧 _Important_
>
> _The following requirements are Royal Mail specific in addition to Intersoft's mandatory fields._

<Table align={["center","left"]}>
  <thead>
    <tr>
      <th>
        Section
      </th>

      <th>
        Required details
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        **SHIPPER**
      </td>

      <td>
        * ContactName - this must be an individual person's name, not a company name.
        * CompanyName
        * ContactEmail
        * ContactPhone
        * Line1
        * Town
        * Postcode
        * CountryCode
      </td>
    </tr>

    <tr>
      <td>
        **DESTINATION**
      </td>

      <td>
        * ContactName
        * CompanyName - highly recommended
        * ContactEmail
        * ContactPhone
        * Line1
        * Town
        * Postcode
        * CountryCode
      </td>
    </tr>

    <tr>
      <td>
        **SHIPMENT INFORMATION**
      </td>

      <td>
        * DescriptionOfGoods
        * DeclaredValue
        * DeclaredWeight
        * CurrencyCode
      </td>
    </tr>

    <tr>
      <td>
        **ITEMS**
      </td>

      <td>
        * Quantity
        * Description
        * Value
        * Weight
        * HSCode
        * CountryOfOrigin
      </td>
    </tr>

    <tr>
      <td>
        **CUSTOMS**
      </td>

      <td>
        * ShippingCharges - please make sure to populate this field either with the exact amount the end customer was charged for shipping or with "0" if the shipping was for free.
      </td>
    </tr>

    <tr>
      <td>
        **CODE**
      </td>

      <td>
        * **CustomsEmail** (receiver email address) – Mandatory for PDDP, DDP, DTP, and Royal Mail Cross Border or Import products. The **Code** field must be set to **EM**, with a valid email provided in the **Destination** > **Address** > **ContactEmail** field.
      </td>
    </tr>
  </tbody>
</Table>

> 🚧 _Please note_
>
> _The above are also requirements specific for Royal Mail customers creating international shipments._
