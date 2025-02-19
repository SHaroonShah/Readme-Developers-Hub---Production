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
This service typically involves the transportation of goods via a freight <<glossary:carrier>> (such as trucks, ships, or air freight) to a central location, followed by delivery through postal service to the final location. 

In UK, the <<glossary:shipments>> arrive as freight. For custom clearance purposes, Royal Mail collect these items from the airline handler before converting them from Freight 2 Post. Once converted/recognised as postal, Royal Mail presents these items to customs as postal before injecting them into the UK network.

> 💡 _Tip_
> 
> _In the following table, the mandatory requirements are marked with an asterisk (\*)._

[block:parameters]
{
  "data": {
    "h-0": "Requirement",
    "h-1": "Description",
    "0-0": "**Shipper Address**",
    "0-1": "Represents the address based in another country (that is, outside the UK).",
    "1-0": "**Return Address**",
    "1-1": "Represents the return address.  \nReturn to **Sender** section of the **Create Shipment** request to be populated with the Royal Mail HWDC Distribution Centre address:  \n  \n**CompanyName**: COMPANY NAME - Royal Mail HWDC  \n**Line1:** Axis Park, Hurricane Way  \n**Town:** SLOUGH  \n**Postcode:** SL95 1FP",
    "2-0": "**Customs documentation\\***",
    "2-1": "Represents the essential forms, papers, and electronic records required to facilitate the import and export of goods across international borders.  \n  \nThis can be either a combined label + <<glossary:CN22>> or <<glossary:CN23>>separately.",
    "3-0": "**Manifest - Royal Mail Sales Order Summary**",
    "3-1": "Not required.  \n  \nThere is no one to hand over the paperwork and the customers provide the pre-alert data to HWDC which acts as a replacement of the manifest paperwork.",
    "4-0": "**Royal Mail Sign Off\\***",
    "4-1": "Represents the customer data services (CDS) checks and physical sign off label.  \n  \n_`Note:`Details on this label are shared once the [Sandbox Test Pack](https://docs.intersoftsapient.net/docs/royal-mail-importers-sandbox-test-pack)  is approved._",
    "5-0": "**Create Shipment field requirements**",
    "5-1": "To access the list of all of the **Create Shipment** fields required for Freight 2 Post customers, refer to the [Field requirements for Freight 2 post customers](https://docs.intersoftsapient.net/docs/freight-2-post-customers-fields-requirements) sectio"
  },
  "cols": 2,
  "rows": 6,
  "align": [
    "center",
    "left"
  ]
}
[/block]


<br />

> 🚧 _Important_
> 
> Please also remember to develop our International Arrivals Containers (A-scan) API. It's one of the sets of API calls mandatory for Freight 2 Post customers.