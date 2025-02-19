---
title: Add pre-registration number
excerpt: >-
  A pre-registration number is often required for certain shipments, especially
  when dealing with customs or compliance-related processes. This number serves
  as an identifier for businesses that engage in international shipping and may
  need to meet specific regulatory requirements before transporting goods across
  borders
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
Some countries operate a Tax Pre-Registration scheme, for example, VOEC in Norway, GST in Australia, and so on. If you are registered for a Tax Pre-Registration scheme for the destination country and are shipping under the scheme rules, then you must provide the <<glossary:Pre-registration number>> for the destination country.

> 🚧 _Important_
> 
> _The pre-registration number is only relevant for <<glossary:shipments>> with the <<glossary:DDU>> <<glossary:incoterms>>. If not provided in the **Create Shipment** API request and the shipment incoterms are set to DDU, then any pre-registration numbers that are set for your account in the **Customs Settings** GUI are used._

In SAPIENT, you can add the pre-registration number to ensure compliance with international shipping regulations and customs processes. This number facilitates smoother clearance of goods at customs, reducing delays in shipment and helps maintain accurate records of shipments for auditing and tracking purposes.

To add a pre-registration number in SAPIENT, follow the steps as explained in the following procedure.

1. In the left navigation panel, select **Customs Settings** > **Pre-Registration Numbers**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/52fba08b346b45d4888a1dc14a06bf395cc4b30bdd9eeec98113d4c2fa2e416f-Pre-registration_numbers_option.png",
        "",
        "Accessing pre-registration numbers"
      ],
      "align": "center",
      "border": true,
      "caption": "Accessing pre-registration numbers"
    }
  ]
}
[/block]


2. In the **Pre-Registration Numbers** page that opens, select ![alt text](https://files.readme.io/574f2d3dd4cce77a9cde0e299f8a2f591fab81c8c7b4b49266c81ed4528c661d-Add_pre-registration_number_button.png).

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/d7897eb60920589421496b60ad5a80cb6864a92a17cfb7f3f5aa143994d24e65-Add_pre-registration_number_option.png",
        "",
        "Accessing option to add pre-registration number"
      ],
      "align": "center",
      "caption": "Accessing option to add pre-registration number"
    }
  ]
}
[/block]


3. In the **Add Pre-Registration Number** form that opens, in the **SHIPPING ACCOUNT** block, from the dropdown menu, select the <<glossary:shipping account>> for which you want to add the pre-registration number.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/1eec0cd1bf0612547a50a5de7866c9467f0e0faaff330c61093b16e411869a0f-Shipping_account_block_2.png",
        "",
        "Selecting shipping account"
      ],
      "align": "center",
      "border": true,
      "caption": "Selecting shipping account"
    }
  ]
}
[/block]


4. After, in the **PRE-REGISTRATION NUMBER** block that appears, enter the necessary information as explained in the following table.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/e915ba8ed9b9e03c3d9a7662a7ce8fca175d3a707b9348ab7509b35df51fed36-Pre-registration_number_block.png",
        "",
        "Entering pre-registration number and its details"
      ],
      "align": "center",
      "border": true,
      "caption": "Entering pre-registration number and its details"
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
    "0-0": "**Shipping Location**",
    "0-1": "From the dropdown menu, select the <<glossary:shipping location>> for which you want to add the pre-registration number.  \n  \nYou can also select **All** if you want to add a pre-registration number for all the existing shipping accounts. ",
    "1-0": "**Country**",
    "1-1": "From the dropdown menu, select the specific destination country for which you want to add the pre-registration number.  \n  \nYou may select **All** if you want to include all the countries (that are, countries grouped by European Union or <<glossary:ROW>> categories). ",
    "2-0": "**Country Group**",
    "2-1": "From the dropdown menu, select the country group for which you want to add the pre-registration number.  \n  \n_Note: If you have selected a specific country in the **Country** field, then in this field, select **N/A**. Otherwise, select either **EuropeanUnion** or **RestOfTheWorld** options. In this case, the **Country** field value is set to **All**._",
    "3-0": "**Type\\***",
    "3-1": "From the dropdown menu, select any of the following types that you want to associated with your pre-registration number:  \n  \n• <<glossary:OSS>>  \n• <<glossary:IOSS>>  \n• <<glossary:GST>>  \n• **Other, please specify**: choose this option, only if the type you want to specify is other than the ones mentioned in this dropdown field.",
    "4-0": "**Other Type**",
    "4-1": "This field is only available if you have selected the **Other, please specify** option in the **Type** field.  \n  \nEnter the type that you want to associate with the pre-registration number you are adding.",
    "5-0": "**Pre-Registration Number\\***",
    "5-1": "Enter your pre-registration number",
    "6-0": "**Valid From\\***",
    "6-1": "From the date picker, select the date from which the pre-registration number you are adding is valid. "
  },
  "cols": 2,
  "rows": 7,
  "align": [
    "center",
    "left"
  ]
}
[/block]


5. After entering the relevant information, select  ![alt text](https://files.readme.io/5041628c1ebe60cd9a698ff4068b10ef8341649edfe2e513e460f7afddb93d08-Add_pre-registration_number_button_2.png). 

Once selected, the pre-registration number is added successfully and displays in the **Pre-Registration Numbers** list. You can now use this number in your [Create Shipment](https://docs.intersoftsapient.net/reference/post_v4-shipments-rm) request.

> 💡 _Tip_
> 
> If you want to remove the pre-registration number, then in the **Pre-Registration Numbers** list, next to the one you want to delete, select ![alt text](https://files.readme.io/0979c7211f5ae99308ba3f765bd083d41949895562626a4f0cc33acd80b30762-Trash_icon.png).
> 
> [block:image]{"images":[{"image":["https://files.readme.io/18854da926a99e35b6280bbb19445cac623a73a7f01d8cb9df4c99cd2a6fe6e9-Removing_item.png","","Deleting pre-registration number"],"align":"center","border":true,"caption":"Deleting pre-registration number"}]}[/block]