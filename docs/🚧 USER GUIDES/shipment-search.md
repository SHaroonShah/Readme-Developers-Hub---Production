---
title: Search shipments
excerpt: >-
  The *Shipment Search* feature is designed to serve as a tool for users to find
  and track shipments based on specific criteria.  The purpose is to provide
  visibility and updates on the status and details of shipments, helping users
  manage logistics more efficiently.
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
In SAPIENT, you can search your <<glossary:shipments>> based on <<glossary:customer>>, <<glossary:shipping location>>, and date ranges.  
To search shipments in SAPIENT, follow the steps as explained in the following procedure.

1. In the side navigation panel, select the **Shipment Search** option.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/61c56d1eac2f021d25812b6f6bda320ace57046cc188b77226161bca4a73963e-Shipment_search_option.png",
        "",
        "Accessing shipments"
      ],
      "align": "center",
      "border": true,
      "caption": "Accessing shipments"
    }
  ]
}
[/block]


2. In the **Shipment Search** page that opens, in the **FILTERS** block, specify your filters based on which you want to search your shipments, and then select ![alt text](https://files.readme.io/34fc7db79563540c7ec5a0d5ec80b50898cfa4ddd9fba622f178d517803116e6-Show_shipments_button.png). 

> 📘 _Note_
> 
> _The maximum date range for shipment search is 30 days_.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/f9ddcaf850dfd3eab60dd8b53e411e104e71000c4a4447df5a251a6368f39409-Shipment_search_filter.png",
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


3. Once filtered, the **Shipment Search** table displays the shipments matching your search criteria. The columns displayed in the table are explained in the following table.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/c285916b7f58433871d17666a0e9fc2aa38ea4b929a4cb089304fd5b608b87ba-Shipment_search_table.png",
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
    "0-0": "**Tracking Number**",
    "0-1": "Represents the unique identifier assigned to each shipment, allowing users to monitor its progress through the shipping system.  \n  \nNote: in this column, you can also download the shipment <<glossary:label>> or copy the <<glossary:tracking number>> by selecting the corresponding icons. ",
    "1-0": "**Shipment date**",
    "1-1": "Represents  date on which the shipment was processed and dispatched, essential for tracking timelines and delivery expectations.",
    "2-0": "**Carrier**",
    "2-1": "Represents the name and logo of the <<glossary:carrier>> responsible for delivering the shipment.",
    "3-0": "**Account**",
    "3-1": "Represents the account name associated with the shipment, used for billing and record-keeping purposes within the system.",
    "4-0": "**Reference**",
    "4-1": "Represents an additional identifier information, such as an order number or customer reference, providing context for the shipment.",
    "5-0": "**Service**",
    "5-1": "Represents the type of shipping service used (for example, standard, express), influencing delivery speed and cost.",
    "6-0": "**Recipient**",
    "6-1": "Represents the name of the individual or entity designated to receive the shipment, important for ensuring accurate delivery.",
    "7-0": "**Destination**",
    "7-1": "Represents  final location where the shipment is being sent, needed for route planning and logistical coordination.",
    "8-0": "**Status**",
    "8-1": "Represents  the current state of the shipment (for example, **Confirmed**, **Label Printed**, and so on), providing timely updates to users.",
    "9-0": "**Packages**",
    "9-1": "Represents quantity of <<glossary:package>>s included in the shipment, vital for planning and inventory management.",
    "10-0": "**Last Modified**",
    "10-1": "Represents the date and time of the most recent update to the shipment's information, helping users track changes and ensure accuracy."
  },
  "cols": 2,
  "rows": 11,
  "align": [
    "center",
    "left"
  ]
}
[/block]


After viewing your shipments, you can now take necessary actions on your shipments as needed.