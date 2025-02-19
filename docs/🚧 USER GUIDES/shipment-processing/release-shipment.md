---
title: Release shipment
excerpt: >-
  Releasing a shipment refers to the process of removing any restrictions or
  barriers that prevented it from being processed or shipped. It typically
  involves resolving any issues that cause the shipment hold, such as completing
  the required documentation, verifying payment, or addressing compliance
  concerns.
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
Releasing a shipment from hold is crucial for maintaining operational efficiency, ensuring timey delivery, and upholding customer relationships.

In SAPIENT, you can anytime release the [held](https://docs.intersoftsapient.net/docs/held-shipments)<<glossary:shipments>>  .

> 💡 _Tip_
> 
> _You can release the shipments both via UI and the API. For more information on how to release shipments via API, refer to the [API References](https://docs.intersoftsapient.net/reference/put_v4-shipments-status) section._

To release a shipment in SAPIENT, follow the steps as explained in the following procedure.

1. In the side navigation panel, select the **Shipment Processing** > **Held** option.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/c0796ec5b2d1123cc03bd22830f7520bddea1408599b62a0b00be63dff75e887-Held_option.png",
        "",
        "Accessing shipments"
      ],
      "align": "center",
      "border": true,
      "caption": "Accessing held shipments"
    }
  ]
}
[/block]


2. In the **Held Shipments** page that opens, select the checkboxes next to the shipments you want to release, and then select ![alt text](https://files.readme.io/ea4f0d57b9918ccc9192a3d230a9dbd24e3e5a33c864e0dd4e8c973181d78f46-Release_shipments_button.png). 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/a64211ea7a7073f81971a21ff07e429fe56864cd50f4be911b9af62da763fe8d-Releasing_shipment.png",
        "",
        "Recalling shipment"
      ],
      "align": "center",
      "border": true,
      "caption": "Releasing shipments"
    }
  ]
}
[/block]


3. In the confirmation dialog that appears, select **Yes**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/6357a15bc67e4c76c3e37aca5da2842b7bdb395cf3c3ce8fa6e6bd16bba7a751-Confirming_shipment_release.png",
        "",
        "Confirming shipment recalling"
      ],
      "align": "center",
      "sizing": "350px",
      "border": true,
      "caption": "Confirming shipment release"
    }
  ]
}
[/block]


3. Once confirmed, the shipment(s) is removed from the **Held Shipments** list and goes back to its previous status and is included in the next manifest.

> 💡 _Tip_
> 
> _If you want to export the label for the held shipments, then in the **Tracking Number** column select ![alt text](https://files.readme.io/3df26abe526e632f50567b6ad821d178d4193a2d068a9f584e3e6a2b547b4417-Cloud_icon.png). Follow the prompts of your computer and download it. _