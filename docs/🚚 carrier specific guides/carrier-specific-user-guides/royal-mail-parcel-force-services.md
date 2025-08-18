---
title: Royal Mail Parcel Force services
excerpt: >-
  Royal Mail has taken significant steps to enhance its operations by
  replicating the existing Parcelforce’s international and domestic services
  into their own software systems. This is done to expand the operational
  software capabilities within the Royal Mail Group, thereby streamlining
  operations within the Royal Mail network.
deprecated: false
hidden: true
icon: fad fa-square-dashed-circle-plus
metadata:
  robots: index
---
The introduction of the new services represents a comprehensive approach to international and domestic shipping needs. Some international services require a partner label for completing the final mile delivery.

A *partner label* is a shipping label utilised in collaboration with other carriers, which facilitates the last-mile delivery of shipments. For Royal Mail, partners such as GLS and FedEx will use these partner labels to manage the final stages of delivery to the recipient outside the UK.

Partner label involves utilising two separate labels on a shipment to reflect both the originating carrier (Royal Mail) and the partner carrier (GLS or FedEx) responsible for the last-mile delivery. Therefore, for services using partner labels, SAPIENT will generate both the Royal Mail and partner label and return them in the Create Shipment response. This dual labelling mechanism helps streamline the logistics process and enhances tracking and accountability throughout the delivery journey. By utilising partners, Royal Mail aims to provide an enhanced service that meets customer expectations around the globe.

The new Royal Mail international services are listed in the following table.

| Service Code | Service Name                     | Partner Label Required | Partner Carrier |
| :----------: | :------------------------------- | :--------------------- | :-------------- |
|      ERB     | EUROPRIORITY DDP                 | ✅                      | GLS             |
|      ER6     | EUROPRIORITY DDP-EXTRACOMP1      | ✅                      | GLS             |
|      ER7     | EUROPRIORITY DDP-EXTRACOMP2      | ✅                      | GLS             |
|      ER8     | EUROPRIORITY DDP-EXTRACOMP3      | ✅                      | GLS             |
|      ERA     | EUROPRIORITY DTP IOSS            | ✅                      | GLS             |
|      ER1     | EUROPRIORITY DTP IOSS-EXTRACOMP1 | ✅                      | GLS             |
|      ER2     | EUROPRIORITY DTP IOSS-EXTRCOMP2  | ✅                      | GLS             |
|      ER3     | EUROPRIORITY DTP IOSS-EXTRACOMP3 | ✅                      | GLS             |
|      GXR     | GLOBALEXPRESS                    | ✅                      | FedEx           |
|      GX1     | GLOBALEXPRESS-EXTRACOMP1         | ✅                      | FedEx           |
|      GX2     | GLOBALEXPRESS-EXTRACOMP2         | ✅                      | FedEx           |
|      GX3     | GLOBALEXPRESS-EXTRACOMP3         | ✅                      | FedEx           |
|      ECA     | GLOBALPRIORITY EUROPE            | ⛔                      | N/A             |
|      EC1     | GLOBALPRIORITY EUROPE-EXTRACOMP1 | ⛔                      | N/A             |
|      EC2     | GLOBALPRIORITY EUROPE-EXTRACOMP2 | ⛔                      | N/A             |
|      EC3     | GLOBALPRIORITY EUROPE-EXTRACOMP3 | ⛔                      | N/A             |
|      GPA     | GLOBALPRIORITY ROW               | ⛔                      | N/A             |
|      GP1     | GLOBALPRIORITY ROW-EXTRACOMP1    | ⛔                      | N/A             |
|      GP2     | GLOBALPRIORITY ROW-EXTRACOMP2    | ⛔                      | N/A             |
|      GP3     | GLOBALPRIORITY ROW-EXTRACOMP3    | ⛔                      | N/A             |
|      IXA     | IRELAND EXPRESS                  | ✅                      | GLS             |
|      IX1     | IRELAND EXPRESS-EXTRACOMP1       | ✅                      | GLS             |
|      IX2     | IRELAND EXPRESS-EXTRACOMP2       | ✅                      | GLS             |
|      IX3     | IRELAND EXPRESS-EXTRACOMP3       | ✅                      | GLS             |
|      CEO     | China Economy - Personal Effects | ⛔                      | N/A             |
|      CEP     | China Economy - POL Drop         | ⛔                      | N/A             |
|      CEQ     | China Economy - Depot Drop       | ⛔                      | N/A             |
|      CER     | China Economy - 3PC              | ⛔                      | N/A             |
|      CES     | China Economy - Direct Hub Drop  | ⛔                      | N/A             |

## API request and response for partner label

```
{
       "Shipper": {
     "ShippingAccountId": "27676a50-afe3-42be-bbdf-a46a51046bb8",
        "ShippingLocationID": "a46ce242-9235-4fce-a1bc-b15d45f02517",
        "Reference1": "",
        "DepartmentNumber": "",
        "EORInumber":"GB12345",
        "Address": {
            "ContactName": "Deepali Patil",
            "CompanyName": "Intersoft",
            "ContactEmail": "deepali.patil@intersoft.co.uk",
            "ContactPhone": "01753 689292",
            "Line1": "Blays House ",
            "Line2": "Wick Road",
            "Line3": "Englefield Green",
            "Town": "Egham",
            "Postcode": "TW20 0HJ",
            "County": "",
            "CountryCode": "GB"
        }},
    "Destination": {
        "Address": {
            "ContactName": "Max Mustermann",
           "companyname":"",
            "ContactEmail": "testingcustomer@intersoft.co.uk",
            "ContactPhone": "+33 123456",
         "Line1": "Berger Str. 36",
         "Line2":"",
         "Line3": "",
        "Town": "Frankfurt",
        "County": "Hesse",
        "Postcode": "60598",
         "CountryCode": "DE"
        }},
         "ShipmentInformation": {
        "ContentType": "NDX",
        "DescriptionOfGoods": "miscellaneous",
        "LabelFormat": "",
        "ShipmentDate": "",
        "CurrencyCode": "EUR",
        "WeightUnitOfMeasure": "Grams",
        "ServiceCode": "GXR",
        "BusinessTransactionType":"",
          "Action": "process"
    },
    "CarrierSpecifics": {
        "ServiceLevel": "01",
        "EbayVtn": "",
        "ServiceEnhancements": [          
]
    },
    "Packages": [
        {
              "PackageType": "parcel",
            "PackageOccurrence": 1,
            "DeclaredWeight": 1687,
            "DeclaredValue": 335,
            "Dimensions": {
                "Length":40,
                "Width": 30,
                "Height": 1
            }
        },
    ],
    "Items": [
         {
             "SkuCode": "SKU123",
      "PackageOccurrence": 1,
      "Quantity": 1,
      "Description": "Printer",
      "Value":331,
      "Weight": 1377,
      "HSCode": "61868224",
      "CountryOfOrigin": "CN"
        },
    ],
    "Customs": {
        "ReasonForExport": "Gift",
        "Incoterms": "DDU",
        "PreRegistrationNumber": "",
        "PreRegistrationType": "",
        "ShippingCharges": 45.82,
        "OtherCharges": 32,
        "QuotedLandedCost": 42.74,
        "InvoiceNumber": "INV-12345",
        "InvoiceDate": "2022-04-23T00:00:00.000Z",
        "ExportLicenceRequired": true,
        "Airn": "231.002.999-00"
    },
    "ReturnToSender": {
        "Address": {
              "ContactName": "Deepali Patil",
            "CompanyName": "Intersoft",
            "ContactEmail": "deepali.patil@intersoft.co.uk",
            "ContactPhone": "01753 689292",
            "Line1": "Blays House ",
            "Line2": "Wick Road",
            "Line3": "Englefield Green",
            "Town": "Egham",
            "Postcode": "TW20 0HJ",
            "County": "Surrey",
            "CountryCode": "GB"
        }
    }
}

RESPOSNE

{
“Labels”: label string
     "LabelFormat": "PDF",
    "Packages": [
        {
            "CarrierDetails": {
                "UniqueId": "4F0069786000000E452FE",
                "PartnerDetails": {
                    "PartnerName": "FedEx",
                    "PartnerCode": "FedEx",
                    "PartnerTrackingNumber": "794880860709",
                    "PartnerTrackingUrl": "https://www.fedex.com/wtrk/track/?trknbr=794880860709"
                }
            },
            "ShipmentId": "f4fb041e-0d28-4370-95b3-4e09b1938cf8",
            "PackageOccurrence": 1,
            "TrackingNumber": "EI000055401GB",
            "CarrierTrackingUrl": "https://www.royalmail.com/track-your-item#/tracking-results/EI000055401GB"
        }
    ]
}

```

## Partner label template example

<Image align="center" width="300px" src="https://files.readme.io/dc8ee4c38fbca556406dffd6bed5af8af1336871730ec786bdbaf1d9ebf0e238-image.png" />

<Image align="center" className="border" border={true} width="300px" src="https://files.readme.io/bb0e617b2ad053080ffaa51ae2d32b289789aa07072e167b07b835f4c6773e2a-image.png" />