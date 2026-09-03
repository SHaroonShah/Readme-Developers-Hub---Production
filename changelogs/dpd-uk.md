---
title: Royal Mail swagger documentation updates
author: Syed Haroon Shah
hidden: true
published_at: '2026-05-12T09:45:53.998Z'
type: improved
---
## Miscellaneous enhancements

The following enhancements have been made to the **SAPIENT ROYAL MAIL API** endpoints.

* **Create Shipment**:  The following two new categories have been added to the **Customs** > **ReasonForExport** field in addition to the existing categories:
  * **ECommerce Sale of Goods** - for B2C or D2C shipments, such as goods sold directly to consumers via online retail.
  * **Commercial Sale of Goods** - for B2B shipments, covering business to business commercial sales.

This is done so that the shipments are correctly classified as e-commerce or commercial sales, ensuring compliance with Royal Mail's latest specification.

> 📘 _Note_
>
> _Please keep in mind the following:_
>
> * _If the existing **Sale of Goods** value is selected as the reason for export, the system automatically determines whether the shipment is **Ecommerce (B2C or D2C)** or **Commercial (B2B)** based on the value provided in the **BusinessTransactionType** field in the create shipment request._
> * _If any of the new reason for export values are requested in the **Print Document** API, they will be displayed in the generated CN23 document._
> * _This enhancement will be live starting 1st June 2026._
>
> _For more information, refer to the <Anchor label="Create Shipment" target="_blank" href="https://docs.intersoftsapient.net/reference/post_v4-shipments-rm">Create Shipment</Anchor> and [Print Document](https://docs.intersoftsapient.net/reference/post_v4-shipments-printdocument-carriercode-shipmentid) API endpoints._

* **Get Carrier Services**. A new **Services** > **Get Carrier Services** endpoint has been added to the **SAPIENT ROYAL MAIL API** block, allowing users to retrieve the service levels associated with each requested service code.

```curl
[
  {
    "ServiceCode": "CRL1",
    "Description": "Royal Mail 24 Standard/Signed For (Parcel - Daily Rate Service)",
    "CarrierSpecifics": {
      "ServiceLevels": [
        "01",
        "02"
      ]
    }
  }
]
```

<p style={{ textAlign: "center" }}>
  <em>Response payload example</em>
</p>

## Field description updates

The query and response field descriptions for the following SAPIENT ROYAL MAIL API endpoints have been updated to improve clarity and support correct usage of the API:

<Columns layout="fixed">
  <Column>
    * **Shipping Accounts**
      * Get Accounts
      * Add Account
      * Get Account
      * Update Account
      * Link Locations
      * Get Associated Locations
      * Get Associate Location
      * Update Associated Location
  </Column>

  <Column>
    * **Shipments**
      * Create Shipment
      * Print Label
      * Print My Label QR Code
      * Pre Allocate Tracking Number
  </Column>

  <Column>
    * **Collections**
      * Book Collection
      * Cancel Collection
      * Get Collection Timeslots
  </Column>

  <Column>
    * **Offline Barcode Range**
      * Get Barcode Range
  </Column>
</Columns>

<Columns layout="auto">
  <Column>
    * **International Arrivals Containers**
      * Add Container
      * Get Containers
      * Update Containers
      * Add/Remove Shipments
      * Delete Containers
      * Get Containers
  </Column>
</Columns>

<br />