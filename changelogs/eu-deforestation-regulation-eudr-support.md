---
title: EU Deforestation Regulation (EUDR) support
author: Syed Haroon Shah
hidden: true
published_at: '2026-11-17T14:05:12.946Z'
---
The EU Deforestation Regulation has introduced diligence requirements for products or items associated with deforestation, including wood, coffee, cocoa, rubber, palm oil, soy, and cattle-derived products. Businesses importing, exporting, or placing these goods on the EU market must submit an EUDR Due Diligence Statement (DDS) and provide the associated reference information.

To comply with this regulation, the following new fields have been added to the **Create Shipment** and **Products** endpoints, and **Products** UI.&#x20;

- **EUDRReferenceType**: Specifies the type of EUDR reference associated with the product, such as Due Diligence Statement (DDS) Reference Number, Conventional DDS Reference Number,  Simplified Declaration Identifier (SDI), TARIC document code, exemption code, or any carrier-specific codes that identifies the applicable customs declaration case.
- **EUDRReferenceValue**: Specifies the EUDR reference value applicable to the product and associated with the selected **EUDRReferenceType**.

<HTMLBlock>{`
    <table>
        <tr>
          <th>API object</th>
          <th>Location</th>
        </tr>
        <tr>
          <td style="text-align: center;" colspan="2"><strong>API Endpoints</strong></td>
        </tr>

        <tr>
          <td colspan="2">Create Shipment</td>
        </tr>

        <tr>
          <td colspan="2">Add Product</td>
        </tr>

        <tr>
          <td colspan="2">Update Product</td>
        </tr>

        <tr>
          <td colspan="2">Get Product</td>
        </tr>

        <tr>
          <td colspan="2">Get Products</td>
        </tr>

        <tr>
          <td style="text-align: center;" colspan="2"><strong>SAPIENT UI</strong></td>
        </tr>

        <tr>
          <td colspan="2">CountryCode</td>
        </tr>
      </table>
`}</HTMLBlock>

<Callout icon="far fa-circle-info" theme="info">
  ### **_Note_**

  _In the&#x20;_**_Create Shipment_**_&#x20;endpoint, these fields are captured at the&#x20;_**_Items_**_&#x20;level. For more information, refer to the carrier's Create Shipment endpoint in the &#x20;_[_API References_](https://docs.intersoftsapient.net/reference/introduction)_&#x20;section._

  _For Royal Mail shipments, these fields are also captured on the&#x20;_<Glossary>commercial invoice</Glossary>_&#x20;document._
</Callout>