---
title: Import requirements for Freight 2 Post customers
excerpt: >-
  Freight 2 Post customers are businesses or organisations that utilise a
  shipping service that combines freight transport with postal delivery methods.
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
This service typically involves the transportation of goods via a freight <Glossary>carrier</Glossary> (such as trucks, ships, or air freight) to a central location, followed by delivery through postal service to the final location. 

In UK, the <Glossary>shipments</Glossary> arrive as freight. For custom clearance purposes, Royal Mail collect these items from the airline handler before converting them from Freight 2 Post. Once converted/recognised as postal, Royal Mail presents these items to customs as postal before injecting them into the UK network.

> 💡 *Tip*
>
> *In the following table, the mandatory requirements are marked with an asterisk (\*).*

<Table align={["center","left"]}>
  <thead>
    <tr>
      <th style={{ textAlign: "center" }}>
        Requirement
      </th>

      <th style={{ textAlign: "left" }}>
        Description
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td style={{ textAlign: "center" }}>
        **Shipper Address**
      </td>

      <td style={{ textAlign: "left" }}>
        Represents the address based in another country (that is, outside the UK).
      </td>
    </tr>

    <tr>
      <td style={{ textAlign: "center" }}>
        **Return Address**
      </td>

      <td style={{ textAlign: "left" }}>
        Represents the return address.\
        Return to **Sender** section of the **Create Shipment** request to be populated with the Royal Mail HWDC Distribution Centre address:  

        * \*CompanyName\*\*: COMPANY NAME - Royal Mail HWDC  
        * \*Line1:\*\* Axis Park, Hurricane Way  
        * \*Town:\*\* SLOUGH  
        * \*Postcode:\*\* SL95 1FP
      </td>
    </tr>

    <tr>
      <td style={{ textAlign: "center" }}>
        **Customs documentation\***
      </td>

      <td style={{ textAlign: "left" }}>
        Represents the essential forms, papers, and electronic records required to facilitate the import and export of goods across international borders.  

        This can be either a combined label + <Glossary>CN22</Glossary> or <Glossary>CN23</Glossary>separately.
      </td>
    </tr>

    <tr>
      <td style={{ textAlign: "center" }}>
        **Manifest - Royal Mail Sales Order Summary**
      </td>

      <td style={{ textAlign: "left" }}>
        Not required.  

        There is no one to hand over the paperwork and the customers provide the pre-alert data to HWDC which acts as a replacement of the manifest paperwork.
      </td>
    </tr>

    <tr>
      <td style={{ textAlign: "center" }}>
        **Royal Mail Sign Off\***
      </td>

      <td style={{ textAlign: "left" }}>
        Represents the customer data services (CDS) checks and physical sign off label.  

        *`Note:`Details on this label are shared once the[Sandbox Test Pack](https://docs.intersoftsapient.net/docs/royal-mail-importers-sandbox-test-pack)  is approved.*
      </td>
    </tr>

    <tr>
      <td style={{ textAlign: "center" }}>
        **Create Shipment field requirements**
      </td>

      <td style={{ textAlign: "left" }}>
        To access the list of all of the **Create Shipment** fields required for Freight 2 Post customers, refer to the [Field requirements for Freight 2 post customers](https://docs.intersoftsapient.net/docs/freight-2-post-customers-fields-requirements) sectio
      </td>
    </tr>
  </tbody>
</Table>

<br />

> 🚧 *Important*
>
> Please also remember to develop our International Arrivals Containers (A-scan) API. It's one of the sets of API calls mandatory for Freight 2 Post customers.
