---
title: Manifest history
excerpt: >-
  The manifest history feature provides a comprehensive record of all shipping
  manifests generated over time. It is primarily used to review , track, and
  manage past shipments, ensuring visibility into shipping activities and
  helping with audit or compliance checks.
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
In SAPIENT, you can search and view manifested <<glossary:shipments>> based on <<glossary:customer>>, <<glossary:shipping location>>, and date ranges.  
To search manifested shipments in SAPIENT, follow the steps as explained in the following procedure.

1. In the side navigation panel, select the **Shipment Processing** > **Manifest History** option.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/2dd0be5964170ba8e4d0b9956c1c4cd105810b50071de35c1494e585185b5aa9-Manifest_history_option.png",
        "",
        "Accessing shipments"
      ],
      "align": "center",
      "border": true,
      "caption": "Accessing manifest history"
    }
  ]
}
[/block]


2. In the **Manifest History** page that opens, in the **FILTERS** block, specify your filters based on which you want to search your shipments, and then select ![alt text](https://files.readme.io/34fc7db79563540c7ec5a0d5ec80b50898cfa4ddd9fba622f178d517803116e6-Show_shipments_button.png). 

> 📘 _Note_
> 
> _The maximum date range for manifest search is 30 days_.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/deeb8cf7c4927c2b815c757d722955250f58d02c85345f159c594a7fb238c59b-Manifest_history_filter.png",
        "",
        "Specifying filters"
      ],
      "align": "center",
      "border": true,
      "caption": "Specifying filters"
    }
  ]
}
[/block]


3. Once filtered, the **Manifest History** table displays the manifested shipments matching your search criteria. The columns displayed in the table are explained in the following table.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/7b056fb156b7f9215b4ed0ded2bc9a47f55ba8a45e473c7a72f7609259e26e52-Manifest_history_table.png",
        "",
        "Viewing shipments"
      ],
      "align": "center",
      "border": true,
      "caption": "Viewing filtered shipments"
    }
  ]
}
[/block]


[block:parameters]
{
  "data": {
    "h-0": "Element",
    "h-1": "Description",
    "0-0": "**Date**",
    "0-1": "Represents the specific date when the manifest was created, crucial for tracking and historical reference.",
    "1-0": "**Customer**",
    "1-1": "Represents the  name or identifier of the customer associated with the shipment, helping to manage relationships and service levels.",
    "2-0": "**Shipping Location**",
    "2-1": "Represents the <<glossary:shipping location>> or dispatch point of the shipment, important for logistics planning and route optimisation.",
    "3-0": "**Shipping Account**",
    "3-1": "Represents the <<glossary:shipping account>> number linked to the shipments for billing and record-keeping purposes.",
    "4-0": "**Manifest Number**",
    "4-1": "Represents the unique identifier assigned to each manifest, used for tracking and organizational purposes.  \n  \nSelect the manifest number link to open and download the <<glossary:manifest>> file either in <<glossary:CSV>> or <<glossary:PDF>>.",
    "5-0": "**Carrier**",
    "5-1": "Represents the name and logo of the <<glossary:carrier>> responsible for delivering the shipment.",
    "6-0": "**Service**",
    "6-1": "Represents the type of shipping service used (for example, standard, express), influencing delivery speed and cost.",
    "7-0": "**Weight**",
    "7-1": "Represents the total weight of the shipment included in the manifest, essential for billing and compliance.",
    "8-0": "**Packages**",
    "8-1": "Represents the total number of <<glossary:package>>s included in the shipment, vital for planning and inventory management.",
    "9-0": "**Created**",
    "9-1": "Represents the date and time when the manifest was generated, providing a timeline for shipping actions and record tracking."
  },
  "cols": 2,
  "rows": 10,
  "align": [
    "center",
    "left"
  ]
}
[/block]


After viewing the manifest history, you can now return to the Home page and continue working with your ongoing shipments as needed.