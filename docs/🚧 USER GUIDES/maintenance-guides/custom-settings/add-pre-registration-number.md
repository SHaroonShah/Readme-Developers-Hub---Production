---
title: Add pre-registration number
excerpt: >-
  Learn how to add pre-registration numbers in SAPIENT for international
  shipping compliance. Required for DDU shipments with tax schemes like VOEC,
  GST, OSS, and IOSS.
deprecated: false
hidden: false
icon: fad fa-square-plus
link:
  new_tab: false
metadata:
  title: ''
  description: ''
  robots: index
---
## Overview

Some countries operate a Tax Pre-Registration scheme, for example, VOEC in Norway, GST in Australia, and so on. If you are registered for a Tax Pre-Registration scheme for the destination country and are shipping under the scheme rules, then you must provide the <Glossary>Pre-registration number</Glossary> for the destination country.

<Cards columns={2}>
  <Card title="Important Note" icon="exclamation-triangle">
    The pre-registration number is only relevant for <Glossary>shipments</Glossary> with the <Glossary>DDU</Glossary> <Glossary>incoterms</Glossary>. If not provided in the **Create Shipment** API request and the shipment incoterms are set to DDU, then any pre-registration numbers that are set for your account in the **Customs Settings** GUI are used.
  </Card>
  
  <Card title="Benefits" icon="check-circle">
    Adding pre-registration numbers ensures compliance with international shipping regulations, facilitates smoother customs clearance, reduces delays, and helps maintain accurate records for auditing and tracking purposes.
  </Card>
</Cards>

## Step-by-Step Procedure

Follow these steps to add a pre-registration number in SAPIENT:

<Accordion title="Step 1: Access Pre-Registration Numbers" icon="arrow-right">

In the left navigation panel, select **Customs Settings** > **Pre-Registration Numbers**.

<Image alt="Accessing pre-registration numbers" align="center" border={true} src="https://files.readme.io/52fba08b346b45d4888a1dc14a06bf395cc4b30bdd9eeec98113d4c2fa2e416f-Pre-registration_numbers_option.png">
  Accessing pre-registration numbers
</Image>

</Accordion>

<Accordion title="Step 2: Start Adding New Number" icon="plus">

In the **Pre-Registration Numbers** page that opens, select ![alt text](https://files.readme.io/574f2d3dd4cce77a9cde0e299f8a2f591fab81c8c7b4b49266c81ed4528c661d-Add_pre-registration_number_button.png).

<Image alt="Accessing option to add pre-registration number" align="center" src="https://files.readme.io/d7897eb60920589421496b60ad5a80cb6864a92a17cfb7f3f5aa143994d24e65-Add_pre-registration_number_option.png">
  Accessing option to add pre-registration number
</Image>

</Accordion>

<Accordion title="Step 3: Select Shipping Account" icon="building">

In the **Add Pre-Registration Number** form that opens, in the **SHIPPING ACCOUNT** block, from the dropdown menu, select the <Glossary>shipping account</Glossary> for which you want to add the pre-registration number.

<Image alt="Selecting shipping account" align="center" border={true} src="https://files.readme.io/1eec0cd1bf0612547a50a5de7866c9467f0e0faaff330c61093b16e411869a0f-Shipping_account_block_2.png">
  Selecting shipping account
</Image>

</Accordion>

<Accordion title="Step 4: Enter Pre-Registration Details" icon="edit">

After selecting the shipping account, in the **PRE-REGISTRATION NUMBER** block that appears, enter the necessary information.

<Image alt="Entering pre-registration number and its details" align="center" border={true} src="https://files.readme.io/e915ba8ed9b9e03c3d9a7662a7ce8fca175d3a707b9348ab7509b35df51fed36-Pre-registration_number_block.png">
  Entering pre-registration number and its details
</Image>

<AsteridkForMandatoryElements />

</Accordion>

<Accordion title="Field Reference Guide" icon="info-circle">

<Table align={["center","left"]}>
  <thead>
    <tr>
      <th style={{ textAlign: "center" }}>
        Element
      </th>

      <th style={{ textAlign: "left" }}>
        Description
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td style={{ textAlign: "center" }}>
        **Shipping Location**
      </td>

      <td style={{ textAlign: "left" }}>
        From the dropdown menu, select the <Glossary>shipping location</Glossary> for which you want to add the pre-registration number.  

        You can also select **All** if you want to add a pre-registration number for all the existing shipping accounts. 
      </td>
    </tr>

    <tr>
      <td style={{ textAlign: "center" }}>
        **Country**
      </td>

      <td style={{ textAlign: "left" }}>
        From the dropdown menu, select the specific destination country for which you want to add the pre-registration number.  

        You may select **All** if you want to include all the countries (that are, countries grouped by European Union or <Glossary>ROW</Glossary> categories). 
      </td>
    </tr>

    <tr>
      <td style={{ textAlign: "center" }}>
        **Country Group**
      </td>

      <td style={{ textAlign: "left" }}>
        From the dropdown menu, select the country group for which you want to add the pre-registration number.  

        *Note: If you have selected a specific country in the**Country** field, then in this field, select **N/A**. Otherwise, select either **EuropeanUnion** or **RestOfTheWorld** options. In this case, the **Country** field value is set to **All**.*
      </td>
    </tr>

    <tr>
      <td style={{ textAlign: "center" }}>
        **Type\***
      </td>

      <td style={{ textAlign: "left" }}>
        From the dropdown menu, select any of the following types that you want to associated with your pre-registration number:  

        • <Glossary>OSS</Glossary>\
        • <Glossary>IOSS</Glossary>\
        • <Glossary>GST</Glossary>\
        • **Other, please specify**: choose this option, only if the type you want to specify is other than the ones mentioned in this dropdown field.
      </td>
    </tr>

    <tr>
      <td style={{ textAlign: "center" }}>
        **Other Type**
      </td>

      <td style={{ textAlign: "left" }}>
        This field is only available if you have selected the **Other, please specify** option in the **Type** field.  

        Enter the type that you want to associate with the pre-registration number you are adding.
      </td>
    </tr>

    <tr>
      <td style={{ textAlign: "center" }}>
        **Pre-Registration Number\***
      </td>

      <td style={{ textAlign: "left" }}>
        Enter your pre-registration number
      </td>
    </tr>

    <tr>
      <td style={{ textAlign: "center" }}>
        **Valid From\***
      </td>

      <td style={{ textAlign: "left" }}>
        From the date picker, select the date from which the pre-registration number you are adding is valid. 
      </td>
    </tr>
  </tbody>
</Table>

</Accordion>

<Accordion title="Step 5: Save Your Configuration" icon="save">

After entering the relevant information, select ![alt text](https://files.readme.io/5041628c1ebe60cd9a698ff4068b10ef8341649edfe2e513e460f7afddb93d08-Add_pre-registration_number_button_2.png). 

Once selected, the pre-registration number is added successfully and displays in the **Pre-Registration Numbers** list. You can now use this number in your [Create Shipment](https://docs.intersoftsapient.net/reference/post_v4-shipments-rm) request.

</Accordion>

## Managing Pre-Registration Numbers

<Cards columns={1}>
  <Card title="Deleting Pre-Registration Numbers" icon="trash">
    If you want to remove a pre-registration number, then in the **Pre-Registration Numbers** list, next to the one you want to delete, select ![alt text](https://files.readme.io/0979c7211f5ae99308ba3f765bd083d41949895562626a4f0cc33acd80b30762-Trash_icon.png).

    <Image alt="Deleting pre-registration number" align="center" border={true} src="https://files.readme.io/18854da926a99e35b6280bbb19445cac623a73a7f01d8cb9df4c99cd2a6fe6e9-Removing_item.png">
      Deleting pre-registration number
    </Image>
  </Card>
</Cards>