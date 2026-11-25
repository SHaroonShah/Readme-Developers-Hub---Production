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

        Depending on the shipment, SAPIENT will generate either a combined shipping label + <Glossary>CN22</Glossary> or a shipping label with a separate <Glossary>CN23</Glossary>. See [Combined label + CN22](https://docs.intersoftsapient.net/docs/combined-label#/) for more information.
      </td>
    </tr>

    <tr>
      <td style={{ textAlign: "center" }}>
        **Manifest - Royal Mail Sales Order Summary**
      </td>

      <td>
        Not required.

        Freight 2 Post customers provide pre-alert data to HWDC instead of a Royal Mail Sales Order Summary.
      </td>
    </tr>

    <tr>
      <td style={{ textAlign: "center" }}>
        **Royal Mail Sign-off**
      </td>

      <td>
        Required. Royal Mail requires both CDS checks and physical label sign-off.

        For CDS checks, you must create and manifest the required test labels and send the label PDFs to Intersoft for review and approval.<br />For physical label sign-off, you must create and manifest the required test labels, print them, and send the physical labels to Royal Mail for approval.

        `Note: `_Instructions for the CDS checks and physical label sign-off will be provided after your&#x20;_[_Sandbox Test Pack_](https://docs.intersoftsapient.net/docs/royal-mail-importers-sandbox-test-pack)_&#x20; has been approved._
      </td>
    </tr>

    <tr>
      <td style={{ textAlign: "center" }}>
        **Create Shipment field requirements**
      </td>

      <td>
        See [Field requirements for Freight 2 Post customers](https://docs.intersoftsapient.net/docs/freight-2-post-customers-fields-requirements) for the required Create Shipment fields.
      </td>
    </tr>
  </tbody>
</Table>

<Callout icon="🚧" theme="warn">
  ### _Important_

  _Freight 2 Post customers must develop the International Arrivals Containers (A-Scan) API calls. See&#x20;_[_International Arrivals Containers (A-Scan)_](https://docs.intersoftsapient.net/reference/post_v4-internationalarrivalscontainers-rm)_&#x20;for more information.&#x20;_
</Callout>
