---
title: Configure Hurricane commerce service
excerpt: >-
  _Hurricane_ is a UK-based technology company that specialises in cross-border
  e-commerce solutions. With the rise of online shopping, cross-border
  e-commerce has become a crucial part of the retail industry.
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
There are some significant challenges faced by the retailers, including the accurate calculation of duties, taxes, and fees associated with shipping goods internationally.This is where Hurricane commerce cervices comes in. The company has developed a suite of tools that help retailers and postal operators comply with international regulations and requirements related to cross-border e-commerce.

In SAPIENT, you can configure the Hurricane commerce services, to eliminate your cross-border challenges and streamline your international <<glossary:shipment>> process.

To configure the Hurricane commerce service, follow the instructions as provided in the following procedure.

1. Log in to the SAPIENT platform using your credentials. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/9d01c43822f6ea8e09f2dcc827a191c1d319511fdbf63e40e4a779b72ec3c46d-Sapient_Login_window.png",
        "",
        "Logging into SAPIENT"
      ],
      "align": "center",
      "sizing": "500px",
      "border": true,
      "caption": "Logging into SAPIENT"
    }
  ]
}
[/block]


2. On the **Home** page that opens, in the left navigation panel, select **Integrations**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/9edbbe0f060a9821348b7a077aae6171ab9fde12fd7b6d2ffdbe5d215b463f3a-Sapient_home_page.png",
        "",
        "Accessing integrations"
      ],
      "align": "center",
      "border": true,
      "caption": "Accessing integrations"
    }
  ]
}
[/block]


> 🚧 _Important_
> 
> _Before you configure the Hurricane service, please note that this is a chargeable service, you will be invoiced directly and any associated usage fees will be applied going forwards. Only approved personnel from your company should be given permission to access these pages and activate this service._

3. On the **Integrations** page that opens, in the **Hurricane** block, select **CUSTOMS** .

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/6ab95a5c1c86ae354fef99d35a7bc44c455705c6ff7e56217a30a01f58b9a29a-Accessing_hurricane_customs_service.png",
        "",
        "Accessing hurricane service"
      ],
      "align": "center",
      "border": true,
      "caption": "Accessing hurricane service"
    }
  ]
}
[/block]


4. On the page that opens, view the services and features provided by Hurricane in their respective blocks, and if you wish to proceed, select **CONFIGURE**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/9617de8bf0d49838392c05d0184155859865df5391536e1b03685863fe928ef9-Selection_option_to_configure_HS.png",
        "",
        "Selecting option to configure hurricane service"
      ],
      "align": "center",
      "border": true,
      "caption": "Selecting option to configure hurricane service"
    }
  ]
}
[/block]


5. On the **Configure Hurricane** page that opens, next to each available service, turn on the toggle for the service that you wish to configure. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/3aaa4e5db150ef6800d6595f71b05fa7c207d4ac67d041c4180af7a4bb3b1e6e-Selecting_hurricane_service.png",
        "",
        "Selecting hurricane services"
      ],
      "align": "center",
      "border": true,
      "caption": "Selecting Hurricane services"
    }
  ]
}
[/block]


6. If you wish to select the **Enable Prohibited Items check on shipment creation** or **Enable Denied Parties check on shipment creation** options, then a **DENIED PARTIES AND PROHIBITED ITEMS COUNTRIES [CONTER]** table is displayed with the following columns.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/034f4680d679a260821c6edc87a787cbb97887a401cb96e3ceb7904a811b6b1d-Configuring_hurricane_services.png",
        "",
        "Configuring hurricane services"
      ],
      "align": "center",
      "border": true,
      "caption": "Configuring Hurricane services"
    }
  ]
}
[/block]


[block:parameters]
{
  "data": {
    "h-0": "Column",
    "h-1": "Description",
    "0-0": "**Country Name**",
    "0-1": "Represents the name of the country for which the service is being configured.",
    "1-0": "**Alpha-2 Code**",
    "1-1": "Represents the country code (initials) of the country for which the service is being configured.",
    "2-0": "**Require Check for Denied Parties**",
    "2-1": "Represents whether the service needs to check for <<glossary:denied parties>> for this country. Typical values are **Yes** and **No**.",
    "3-0": "**Denied Party Score**",
    "3-1": "Represents the threshold value above which the country is identified as denied.  \n  \n_Note: this value is set to 75 by default. You cannot change this value._",
    "4-0": "**Require Check for Prohibited Items**",
    "4-1": "Represents whether the service needs to check for prohibited items. Typical values are **Yes** and **No**.",
    "5-0": "**Last Modified**",
    "5-1": "Represents the exact date, time, and the name of the user who last modified the information provided in the table.",
    "6-0": "Actions",
    "6-1": "Select **View** to open a new screen, where you can manage the Hurricane services for that country. Additionally, from that page, you can also delete the country, if applicable."
  },
  "cols": 2,
  "rows": 7,
  "align": [
    "center",
    "left"
  ]
}
[/block]


> 💡 _Tip_
> 
> _You can also add a new country to the list by selecting the **Add Country** button and configure the desired hurricane services for it on the fly_.