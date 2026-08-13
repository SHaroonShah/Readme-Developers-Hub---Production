---
title: Import requirements for Freight 2 Post customers
excerpt: >-
  Freight 2 Post customers are businesses or organisations that utilise a
  shipping service that combines freight transport with postal delivery methods.
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
This service typically involves the transportation of goods via a freight <Glossary>carrier</Glossary> (such as trucks, ships, or air freight) to a central location, followed by delivery through postal service to the final location.

In UK, the <Glossary>shipments</Glossary> arrive as freight. For custom clearance purposes, Royal Mail collect these items from the airline handler before converting them from Freight 2 Post. Once converted/recognised as postal, Royal Mail presents these items to customs as postal before injecting them into the UK network.

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
        Based in another country (that is, outside the UK).
      </td>
    </tr>

    <tr>
      <td style={{ textAlign: "center" }}>
        **Return Address**
      </td>

      <td>
        **Return to Sender** section of the **Create Shipment** request to be populated with the Royal Mail Heathrow Distribution Centre address:

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

        This can be either a combined label + <Glossary>CN22</Glossary> or <Glossary>CN23</Glossary> separately. Please see [here ](https://docs.intersoftsapient.net/docs/combined-label#/)for more information on this.
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

        `Note:`_Details on this label are shared once the [Sandbox Test Pack](https://docs.intersoftsapient.net/docs/royal-mail-importers-sandbox-test-pack)  is approved._
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
