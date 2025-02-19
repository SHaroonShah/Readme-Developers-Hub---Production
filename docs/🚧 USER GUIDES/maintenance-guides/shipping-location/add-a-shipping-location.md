---
title: Add Shipping Location
excerpt: >-
  A _shipping location_ is a physical address designated area from which the
  goods are sent or despatched. It plays a crucial role in the logistics and
  shipping process.
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
The process of adding a <<glossary:shipping location>> helps in streamlining the order fulfillment process, enhance inventory oversight, aids in coordination, and contributes to customer satisfaction. Shipping locations are fundamental to ensuring that the products are despatched effectively and reach their destinations in a timely manner.

To add a new shipping location in SAPIENT, follow the instructions as described in the following procedure.

1. Log in to the SAPIENT platform using your credentials.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/c2af709d6dafdead99cae2dfd707cdd74065a776db2a6ad1c641d28c2705d229-Sapient_Login_window.png",
        "",
        ""
      ],
      "align": "center",
      "sizing": "500px",
      "border": true
    }
  ]
}
[/block]


2. On the **Home** page that opens, in the left navigation panel, select **Shipping Locations**. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/a84f50bafad4110e2244fa56d73b34787cf197d6a4e3de326ad287880d85e835-Shipping_locations_option.png",
        "",
        "Accessing shipping locations"
      ],
      "align": "center",
      "border": true,
      "caption": "Accessing shipping locations"
    }
  ]
}
[/block]


3. On the **Shipping Locations** page that appears, select ![alt text](https://files.readme.io/e50833cb14406497b4c50b5eb8c6997612af96e420fd9930bc45c1c883dd09a0-Add_shipping_location_button.png).

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/6e836d0e0573bdc15c4d746439001e41ccf2631c0e7bb1bc2f38149dee53e9e3-Selecting_add_shipping_location_button.png",
        "",
        "Selecting option to add shipping location"
      ],
      "align": "center",
      "border": true,
      "caption": "Selecting option to add shipping location"
    }
  ]
}
[/block]


4. On the **Add Shipping Location** form that opens, in the **LOCATION DETAILS** block, enter the necessary information as explained in the following table.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/5e6bebc209c1497103efb0288fd1a0d15ddc0bbb04d07e5d7bc4490f825c649b-Location_details_block.png",
        "",
        "Entering location details"
      ],
      "align": "center",
      "border": true,
      "caption": "Entering location details"
    }
  ]
}
[/block]


<AsteridkForMandatoryElements />

[block:parameters]
{
  "data": {
    "h-0": "Element",
    "h-1": "Description",
    "0-0": "**Name / Alias\\***",
    "0-1": "Enter the name of your location that you want to add.",
    "1-0": "**Set As Default Shipping Location**",
    "1-1": "Turn on this toggle to set the location you entered as default.  \n  \nIf you have previously set a <<glossary:default shipping location>>, then keeping this toggle off retains that location as the default one.  ",
    "2-0": "**Time Zone**",
    "2-1": "From the dropdown menu, select the timezone which adheres to the location you are adding. "
  },
  "cols": 2,
  "rows": 3,
  "align": [
    "center",
    "left"
  ]
}
[/block]


5. Now, in the **ADDRESS DETAILS** block, enter the necessary information as explained in the following table.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/3e977f9b76554494861e9900b8b9a42a8853cb4d2d4aa45c1042487dfbfd2380-Address_details_block.png",
        "",
        "Entering address details"
      ],
      "align": "center",
      "border": true,
      "caption": "Entering address details"
    }
  ]
}
[/block]


<AsteridkForMandatoryElements />

|       Element      | Description                                                                                                                |
| :----------------: | :------------------------------------------------------------------------------------------------------------------------- |
|    **Country\***   | Enter the name of the country where your location is based.                                                                |
|    **Address\***   | Enter the first line of address for your location.                                                                         |
|    **Address 2**   | Enter the second line of address for your location, if applicable.                                                         |
|    **Address 3**   | Enter the third line of address for your location, if applicable.                                                          |
| **Contact Number** | Enter the contact number that can be access at the location you are adding.                                                |
|     **Town\***     | Enter the name of the town where your location is based.                                                                   |
|     **County**     | Enter the name of the county where your location is based.                                                                 |
|   **Postcode\***   | Enter the exact post code of the location you are adding.                                                                  |
|   **What3Words**   | Enter the  <<glossary:What3words>> for your location to be able to get identified within the resolution of about 3 meters. |

6. After entering all the relevant information, select ![alt text](https://files.readme.io/656f8ada261afe731847fa985571a318b7e27a15af1b7bb917149489b6f974ef-Add_shipping_location_button_2.png).

Once done, a new shipping location is created successfully and appears in the **Shipping Locations** table. You can now manage it as per your business needs. 

> 📘 _Note_
> 
> _Shipping locations can be added and managed via API. To learn more on how to add a shipping locations via API, refer to the [API References](https://docs.intersoftsapient.net/reference/post_v4-shippinglocations) section._