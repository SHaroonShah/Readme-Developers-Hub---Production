---
title: Import requirements for Freight 2 Post customers
excerpt: >-
  Freight 2 Post is for customers who send goods to the UK as freight before the
  goods enter the Royal Mail postal network.
deprecated: false
hidden: false
icon: fad fa-file-circle-info
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
Goods are transported to the UK by freight and then enter the Royal Mail network for final delivery.

When the shipments arrive in the UK, they arrive as freight. Royal Mail collects the shipments from the airline handler and processes them as postal items for customs clearance. After customs clearance, the shipments enter the Royal Mail network for final delivery.

<Callout icon="💡" theme="default">
  ### _Tip_

  _In the following table, the mandatory requirements are marked with an asterisk (\*)._
</Callout>

<Table align={["center","left"]}>
  <thead>
    <tr>
      <th style={{ textAlign: "center" }}>
        Requirement
      </th>

      <th>
        Description
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td style={{ textAlign: "center" }}>
        **Shipper Address**
      </td>

      <td>
        Must be an address outside the UK.
      </td>
    </tr>

    <tr>
      <td style={{ textAlign: "center" }}>
        **Return Address**
      </td>

      <td>
        In the **Create Shipment** request, use the Royal Mail Heathrow Distribution Centre address in the **Return to Sender** section:

        - **CompanyName**: COMPANY NAME - Royal Mail HWDC
        - **Line1:** Axis Park, Hurricane Way
        - **Town:** SLOUGH
        - **Postcode:** SL95 1FP
      </td>
    </tr>

    <tr>
      <td style={{ textAlign: "center" }}>
        **Customs documentation**
      </td>

      <td>
        Required.

        Depending on the shipment, SAPIENT will generate either a combined shipping label + <Glossary>CN22</Glossary>, or a shipping label with a separate <Glossary>CN23</Glossary>. See [Combined label + CN22](https://docs.intersoftsapient.net/docs/combined-label#/) for more information on this.
      </td>
    </tr>

    <tr>
      <td style={{ textAlign: "center" }}>
        **Manifest - Royal Mail Sales Order Summary**
      </td>

      <td>
        Not required.

        There is no one to hand over the paperwork and the customers provide the pre-alert data to HWDC which acts as a replacement of the manifest paperwork.
      </td>
    </tr>

    <tr>
      <td style={{ textAlign: "center" }}>
        **Royal Mail Sign Off**
      </td>

      <td>
        Required – CDS checks and physical labels.

        For CDS checks, you will be requested to create couple of labels, manifest them and share with us the PDFs so they can be reviewed and signed off.<br />For physical label sign off, you will be requested to create couple of labels, manifest them and ship them to Royal Mail.

        `Note:`_Details on this label are shared once the&#x20;_[Sandbox Test Pack](https://docs.intersoftsapient.net/docs/royal-mail-importers-sandbox-test-pack)_&#x20; is approved._
      </td>
    </tr>

    <tr>
      <td style={{ textAlign: "center" }}>
        **Create Shipment field requirements**
      </td>

      <td>
        To access the list of all of the **Create Shipment** fields required for Freight 2 Post customers, refer to the [Field requirements for Freight 2 post customers](https://docs.intersoftsapient.net/docs/freight-2-post-customers-fields-requirements) section.
      </td>
    </tr>
  </tbody>
</Table>

<Callout icon="🚧" theme="warn">
  ### _Important_

  _Please also remember to develop our&#x20;_**_International Arrivals Containers (A-scan) API calls_**_. It's mandatory for Freight 2 Post customers._
</Callout>