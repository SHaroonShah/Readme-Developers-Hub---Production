---
title: Import requirements for Commercial Clearance customers
excerpt: >-
  Commercial Clearance is for customers importing goods into the UK who use
  their own customs broker or logistics provider to manage customs clearance.
deprecated: false
hidden: false
icon: fad fa-file-lines
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
Customers must prepare the required customs data and documents according to their customs broker's requirements.<br />Royal Mail does not require this customs information. Shipments are created in SAPIENT using domestic shipment requirements and domestic labels. However, Commercial Clearance shipments use different Royal Mail service codes.

Review the requirements in the table below.

<Callout icon="💡" theme="default">
  ### _Tip_

  _In the following table, the mandatory requirements are marked with an asterisk (*)._
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
        **Shipper Address**\*
      </td>

      <td>
        Must be a UK address.
      </td>
    </tr>

    <tr>
      <td style={{ textAlign: "center" }}>
        **Return Address**\*
      </td>

      <td>
        Must be a UK address.
      </td>
    </tr>

    <tr>
      <td style={{ textAlign: "center" }}>
        **Customs documentation**
      </td>

      <td>
        Not required.
      </td>
    </tr>

    <tr>
      <td style={{ textAlign: "center" }}>
        **Manifest - Royal Mail Sales Order Summary**\*
      </td>

      <td>
        Print the Royal Mail Sales Order Summary and give it to the driver when the parcels are collected.
      </td>
    </tr>

    <tr>
      <td style={{ textAlign: "center" }}>
        **Royal Mail Sign Off**\*
      </td>

      <td>
        Physical label sign-off is required. You must create and manifest the required test labels, print them, and send the physical labels to Royal Mail for approval.

        `Note:`_Instructions for the physical label sign-off will be provided after your&#x20;_[_Sandbox Test Pack_](https://docs.intersoftsapient.net/docs/royal-mail-importers-sandbox-test-pack)_&#x20;has been approved._
      </td>
    </tr>

    <tr>
      <td style={{ textAlign: "center" }}>
        **Create Shipment field requirements**
      </td>

      <td>
        * Follow the domestic shipment requirements in the [Create Shipment API specification](https://docs.intersoftsapient.net/reference/post_v4-shipments-rm)
        * Provide the Destination Contact Email
      </td>
    </tr>
  </tbody>
</Table>