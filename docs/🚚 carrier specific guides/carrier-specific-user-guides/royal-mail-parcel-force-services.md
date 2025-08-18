---
title: Royal Mail Parcel Force services
excerpt: >-
  Royal Mail has taken significant steps to enhance its operations by
  replicating the existing Parcelforce’s international and domestic services
  into their own software systems. This is done to expand the operational
  software capabilities within the Royal Mail Group, thereby streamlining
  operations within the Royal Mail network.
deprecated: false
hidden: false
icon: fad fa-truck-arrow-right
metadata:
  robots: index
---
The introduction of the new services represents a comprehensive approach to international and domestic shipping needs. Some international services require a partner label for completing the final mile delivery.

A *partner label* is a shipping label utilised in collaboration with other carriers, which facilitates the last-mile delivery of shipments. For Royal Mail, partners such as GLS and FedEx will use these partner labels to manage the final stages of delivery to the recipient outside the UK.

Partner label involves utilising two separate labels on a shipment to reflect both the originating carrier (Royal Mail) and the partner carrier (GLS or FedEx) responsible for the last-mile delivery. Therefore, for services using partner labels, SAPIENT will generate both the Royal Mail and partner label and return them in the Create Shipment response. This dual labelling mechanism helps streamline the logistics process and enhances tracking and accountability throughout the delivery journey. By utilising partners, Royal Mail aims to provide an enhanced service that meets customer expectations around the globe.

<Accordion title="International services">
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

  <Image align="center" src="https://files.readme.io/dc8ee4c38fbca556406dffd6bed5af8af1336871730ec786bdbaf1d9ebf0e238-image.png" width="300px" />

  <Image align="center" border={true} src="https://files.readme.io/bb0e617b2ad053080ffaa51ae2d32b289789aa07072e167b07b835f4c6773e2a-image.png" width="300px" />

  <br />
</Accordion>

<Accordion title="Domestic services">
  The new Royal Mail domestic services are listed in the following table.

  | Service Code | Service Name                                                                                             |
  | :----------: | :------------------------------------------------------------------------------------------------------- |
  |      TE1     | **EXPRESS10** - delivery next working day by 10am.                                                       |
  |      TA1     | EXPRESS10 AGE                                                                                            |
  |      TA2     | EXPRESS10 AGE COMP 1                                                                                     |
  |      TA3     | EXPRESS10 AGE COMP 2                                                                                     |
  |      TA4     | EXPRESS10 AGE COMP 3                                                                                     |
  |      TE2     | EXPRESS10 COMP 1                                                                                         |
  |      TE3     | EXPRESS10 COMP 2                                                                                         |
  |      TE4     | EXPRESS10 COMP 3                                                                                         |
  |      NDA     | **EXPRESS 24** – delivery next working day by close of business.                                         |
  |      NDH     | EXPRESS24 AGE                                                                                            |
  |      NDI     | EXPRESS24 AGE COMP 1                                                                                     |
  |      NDJ     | EXPRESS24 AGE COMP 2                                                                                     |
  |      NDK     | EXPRESS24 AGE COMP 3                                                                                     |
  |      NDB     | EXPRESS24 COMP 1                                                                                         |
  |      NDC     | EXPRESS24 COMP 2                                                                                         |
  |      NDE     | EXPRESS24 COMP 3                                                                                         |
  |      RT0     | **EXPRESS24 RETURNS** – collection next day from your home or nearby post office.                        |
  |      RT1     | EXPRESS24 RETURNS COMP 1                                                                                 |
  |      RT2     | EXPRESS24 RETURNS COMP 2                                                                                 |
  |      RT3     | EXPRESS24 RETURNS COMP 3                                                                                 |
  |      FEK     | **EXPRESS24 WEEKEND** – delivery next day on weekend.                                                    |
  |      NDO     | EXPRESS24 WEEKEND AGE                                                                                    |
  |      FEQ     | EXPRESS24 WEEKEND COMP 1                                                                                 |
  |      DS      | EXPRESS24 WEEKEND COMP 1 AGE                                                                             |
  |      FER     | EXPRESS24 WEEKEND COMP 2                                                                                 |
  |      NDT     | EXPRESS24 WEEKEND COMP 2 AGE                                                                             |
  |      FEU     | EXPRESS24 WEEKEND COMP 3                                                                                 |
  |      NDV     | EXPRESS24 WEEKEND COMP 3 AGE                                                                             |
  |      TEA     | **EXPRESS24 WITH PIN** – delivery next working day by close of business with PIN required upon delivery. |
  |      TEB     | EXPRESS24 WITH PIN COMP 1                                                                                |
  |      TEC     | EXPRESS24 WITH PIN COMP 2                                                                                |
  |      TED     | EXPRESS24 WITH PIN COMP 3                                                                                |
  |      RT4     | EXPRESS24 WITH PIN WEEKEND                                                                               |
  |      RT5     | EXPRESS24 WITH PIN WEEKEND COMP 1                                                                        |
  |      RTE     | EXPRESS24 WITH PIN WEEKEND COMP 2                                                                        |
  |      RTF     | EXPRESS24 WITH PIN WEEKEND COMP 3                                                                        |
  |      FE0     | **EXPRESS48** – delivery within 2 working days.                                                          |
  |      FEA     | EXPRESS48 AGE                                                                                            |
  |      FEB     | EXPRESS48 AGE COMP 1                                                                                     |
  |      FEC     | EXPRESS48 AGE COMP 2                                                                                     |
  |      FED     | EXPRESS48 AGE COMP 3                                                                                     |
  |      FE1     | EXPRESS48 COMP 1                                                                                         |
  |      FE2     | EXPRESS48 COMP 2                                                                                         |
  |      FE3     | EXPRESS48 COMP 3                                                                                         |
  |      FEM     | **EXPRESS48 LARGE** – delivery within 2 working days for items up to 2.5m long.                          |
  |      FEN     | EXPRESS48 LARGE COMP 1                                                                                   |
  |      FEO     | EXPRESS48 LARGE COMP 2                                                                                   |
  |      FEP     | EXPRESS48 LARGE COMP 3                                                                                   |
  |      RTA     | **EXPRESS48 RETURNS** – collection within 2 working days from your home or  nearby post office.          |
  |      RTB     | EXPRESS48 RETURNS COMP 1                                                                                 |
  |      RTC     | EXPRESS48 RETURNS COMP 2                                                                                 |
  |      RTD     | EXPRESS48 RETURNS COMP 3                                                                                 |
  |      FEE     | **EXPRESSAM** – delivery next working day by 12 noon.                                                    |
  |      MA1     | EXPRESSAM AGE                                                                                            |
  |      MA2     | EXPRESSAM AGE COMP 1                                                                                     |
  |      MA3     | EXPRESSAM AGE COMP 2                                                                                     |
  |      MA4     | EXPRESSAM AGE COMP 3                                                                                     |
  |      FEF     | EXPRESSAM COMP 1                                                                                         |
  |      FEG     | EXPRESSAM COMP 2                                                                                         |
  |      FEL     | EXPRESSAM COMP 3                                                                                         |
  |      TEH     | **EXPRESSAM WEEKEND** – delivery on weekend by 12 noon.                                                  |
  |      M07     | EXPRESSAM WEEKEND AGE                                                                                    |
  |      M08     | EXPRESSAM WEEKEND AGE COMP 1                                                                             |
  |      M09     | EXPRESSAM WEEKEND AGE COMP 2                                                                             |
  |      M10     | EXPRESSAM WEEKEND AGE COMP 3                                                                             |
  |      TEI     | EXPRESSAM WEEKEND COMP 1                                                                                 |
  |      TEJ     | EXPRESSAM WEEKEND COMP 2                                                                                 |
  |      TEK     | EXPRESSAM WEEKEND COMP 3                                                                                 |

  ## API request and response for domestic label

  ```
  <?xml version="1.0" encoding="UTF-8"?>
  <createShipmentRequest>
      <integrationHeader>
          <transactionId>BCMYH-ZOOFY-XPRKB-FKCCT-NYUGH-ZY</transactionId>
          <applicationId>XXXXX</applicationId>
          <userId>XXXXXXX</userId>
          <password>XXXXXXXX</password>
      </integrationHeader>
      <shipment>
          <shipper>
              <shipperCompanyName>PeptideProtein Research Ltd</shipperCompanyName>
              <shipperAddressLine1>Bridge House Farm</shipperAddressLine1>
              <shipperAddressLine2>184 Funtley Road</shipperAddressLine2>
              <shipperAddressLine3/>
              <shipperCity>Hampshire</shipperCity>
              <shipperCounty/>
              <shipperCountryCode>GB</shipperCountryCode>
              <shipperPostCode>PO15 6DP</shipperPostCode>
              <shipperContactName>James Milton</shipperContactName>
              <shipperPhoneNumber>01753689292</shipperPhoneNumber>
              <shipperVatNumber>GB846276319</shipperVatNumber>
              <shipperEoriNumber>0123456789123</shipperEoriNumber>
              <shipperEmailAddress>SUPPORT@Petone.CO.UK</shipperEmailAddress>
              <shipperReference>99-AP01</shipperReference>
              <shipperReference2></shipperReference2>
              <shipperDeptCode/>
          </shipper>
          <destination>
              <destinationCompanyName></destinationCompanyName>
              <destinationAddressLine1>Interlink Way E</destinationAddressLine1>
              <destinationAddressLine2>Bardon Hill</destinationAddressLine2>
              <destinationAddressLine3/>
              <destinationCity>Coalville</destinationCity>
              <destinationCounty></destinationCounty>
              <destinationCountryCode>GB</destinationCountryCode>
              <destinationPostCode>IG11 9JF</destinationPostCode>
              <destinationContactName>Charlie Harper</destinationContactName>
              <destinationPhoneNumber>07123456789</destinationPhoneNumber>
              <destinationVatNumber/>
              <destinationEmailAddress>Charlieharper@hotmail.com</destinationEmailAddress>
              <destinationPudoId></destinationPudoId>
          </destination>
          <shipmentInformation>
              <shipmentDate>2025-07-09</shipmentDate>
              <serviceCode>NDAN</serviceCode>
              <serviceOptions>
                  <postingLocation>9000257150</postingLocation>
                  <serviceLevel></serviceLevel>
                  <serviceFormat></serviceFormat>
                  <safePlace/>
                  <serviceEnhancements>
                      <serviceEnhancementCode></serviceEnhancementCode>
                  </serviceEnhancements>
              </serviceOptions>
                      <totalPackages>1</totalPackages>
                      <totalWeight>0.2</totalWeight>
                      <weightId>K</weightId>
                      <unitOfMeasurement>C</unitOfMeasurement>
                      <product>NDX</product>
                      <descriptionOfGoods>Sale of Goods</descriptionOfGoods>
                      <declaredValue>250</declaredValue>
                      <declaredCurrencyCode>GBP</declaredCurrencyCode>
                      <terms>DDU</terms>
                      <labelImageFormat>PDF</labelImageFormat>
                      <businessTransactionType>B2C</businessTransactionType>
                      <silentPrintProfile/>
                      <shipmentAction/>
                      <packages>
                          <package>
                              <packageId>1</packageId>
                              <weight>0.2</weight>
                              <length>2</length>
                              <width>3</width>
                              <height>4</height>
                          </package>
                      </packages>
                      <itemInformation>
                          <packageId>1</packageId>
                          <itemHsCode>3504009090</itemHsCode>
                          <itemDescription>Peptones and derivatives; hide powder</itemDescription>
                          <itemQuantity>50</itemQuantity>
                          <itemValue>4.94</itemValue>
                          <itemCOO>GB</itemCOO>
                          <itemSku>TRU-COL 200G</itemSku>
                          <itemNetWeight>0.608</itemNetWeight>
                      </itemInformation>
                  </shipmentInformation>
              </shipment>
    </createShipmentRequest>

  RESPONSE

  <createShipmentResponse xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <integrationHeader>
          <dateTimeStamp>2025-07-09 08:20</dateTimeStamp>
          <transactionId>BCMYH-ZOOFY-XPRKB-FKCCT-NYUGH-ZY</transactionId>
          <applicationId>XXXXXXX</applicationId>
      </integrationHeader>
      <completedShipment>
          <packages>
              <package>
                  <packageId>1</packageId>
                  <trackingNumber>PK000450027GB</trackingNumber>
                  <uniqueId>28006978600000032D60B</uniqueId>
                  <packageTrackingUrl>http://www.royalmail.com/portal/rm/track?trackNumber=PK000450027GB</packageTrackingUrl>
                  <formattedUniqueId>28006978600000032D60B</formattedUniqueId>
              </package>
          </packages>
          <carrierCode>RYML</carrierCode>
          <labelImage>image String</labelImage>
          <labelImageFormat>PDF</labelImageFormat>
      </completedShipment>
  </createShipmentResponse>


  ```

  ## Domestic label template example

  <Image align="center" border={true} src="https://files.readme.io/c9bd0fc953ff5ea7953e9b41461c16de453bb7a6ab10c3bf2f12368bd3031c80-image.png" width="300px" />
</Accordion>