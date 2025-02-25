---
title: >-
  Windsor Framework: A new trade regulation between Great Britain and Northern
  Ireland 
excerpt: >-
  The _Windsor Framework_ is a crucial agreement established between the United
  Kingdom and the European Union to manage trade from Great Britain to Northern
  Ireland in the wake of Brexit. 
deprecated: false
hidden: false
metadata:
  robots: index
---
One of the most significant aspects of the Windsor Framework is its impact on all <Glossary>carriers</Glossary> and <Glossary>customer</Glossary>s involved in shipping goods from Great Britain (GB) to Northern Ireland (NI). The framework delineates clear guidelines for Business-to-Business (B2B) and Business-to-Consumer (B2C) shipments, ensuring that regulations are followed while facilitating smoother trade operations.

> 🚧 *Important*
>
> *Businesses must familiarise themselves with the specific requirements set out in the[ Windsor Framework](https://www.gov.uk/government/publications/moving-parcels-from-great-britain-to-northern-ireland-under-the-windsor-framework) by HMRC.*

To align with the Windsor Framework changes, customers using the Sapient system must update their shipping protocols and documentation processes. This includes integrating the new customs requirements into their logistics workflows and ensuring that all necessary data is captured correctly for both B2B and B2C shipments. Training staff on these updates will be crucial to ensure compliance and streamline operations.

If you are sending B2B shipments, make sure to populate the following fields in your create shipment API request.

> 📘 *Note*
>
> *Please note that the following script is only displaying the necessary fields that are required for B2B shipments to NI. Please make sure these fields are populated along with all the necessary fields associated to that particular object. For more information on how to populate the required fields, refer to the[ API References](https://docs.intersoftsapient.net/reference/post_v4-shipments-rm) section.*

```
curl --request POST \ 
     --url https://api.intersoftsapient.net/v4/shipments/rm \ 
     --header 'accept: application/json' \ 
     --header 'content-type: application/json' \ 
     --data ' 
  "ShipmentInformation": { 
   "BusinessTransactionType": "B2B"
    
  }, 
    
  "Shipper": { 
    "EoriNumber": "GB213456789000", 
  }, 
    
  "Destination": { 
    "EoriNumber": "GB123456789000", 
  }, 
 
  "Customs": { 
    "ReasonForExport": "Sale Of Goods", 
    "Incoterms": "DDU", 
    "PreRegistrationNumber": "XIUKIMGB123345566700020240712163125", 
    "PreRegistrationType": "UKIMS", 

  }, 
  "Items": [ 
    { 
      "SkuCode": "SKU123", 
      "PackageOccurrence": 1, 
      "Quantity": 1, 
      "Description": "White Mens Large T-shirt", 
      "Value": 19.99, 
      "Weight": 0.5, 
      "HSCode": "6109100010",
      "SuplementaryUnitCode":"25.78",
      "CountryOfOrigin": "CN" 
    }, 
  ] 
} 

```

> 🚧 *Important*
>
> *In the scope of the Windsor Framework changes, you might see some new fields in the API References. Some are carrier specific and some are used by commercial shipments. These new fields are optional and not required for shipments to NI.*

As a B2C customer shipping from Great Britain to Northern Ireland, you do not need to provide the Item **HSCode** or **CountryOfOrigin**. However, if you are a Royal Mail B2C customer, make sure the correct information is provided as explained in the following table:

| Transaction type                                                   | Fields                                                                                                                                                                                                                                                   |
| :----------------------------------------------------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Business 2 Consumer (B2C)**                                      | Goods description, confirmation of goods categorisation by item (optional), weight (by item), value (by item), and country of origin.                                                                                                                    |
| **Business 2 Business (B2B)** - value of goods above £135          | Exporter/Sender deatils (including EORI), Importer/Receiver details (including EORI), total value (not by item), country of origin, gross mass, description of goods, confirmation of goods categorisation by item(optional), UKIMS number.              |
| **Business 2 Business (B2B)** - value of goods up to £135 or less) | Exporter/Sender deatils (including EORI), Importer/Receiver details (including EORI), total value (not by item), country of origin, gross mass, description of goods, confirmation of goods categorisation by item (mandatory), UKIMS number (optional). |

> 📘 *Note*
>
> *The UKIMS or pre-registration number requirements are only applicable to to B2B shipments.*

<Cards columns={4}>
  <Card title="Windsor Framework FAQ's" href="https://docs.intersoftsapient.net/docs/windsor-framework-faqs#/" icon="fa fa-question-circle" target="_blank">
    Find answers to common queries and additional guidance on compliance.
  </Card>
</Cards>