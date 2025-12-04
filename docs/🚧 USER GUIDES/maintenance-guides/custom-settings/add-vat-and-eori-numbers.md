---
title: Add VAT and EORI number
excerpt: >-
  Learn how to add Value Added Tax (VAT) and Economic Operators Registration and
  Identification (EORI) numbers in SAPIENT for seamless cross-border trading and
  customs compliance.
deprecated: false
hidden: false
icon: fad fa-square-plus
link:
  new_tab: false
metadata:
  title: ''
  description: >-
    _Value Added Tax (VAT)_ numbers are essential for businesses engaged in
    trading goods and services across different countries, particularly in the
    European Union. It allows businesses to charge or reclaim VAT on sales and
    purchases. On the other hand, The _Economic Operators Registration and
    Identification (EORI)_ number is necessary for businesses involved in
    customs activities within the EU. It is used to identify traders in customs
    systems.
  robots: index
---
The VAT number ensures proper tax handling and compliance during cross-border transactions and the EORI number expedites customs clearance and reduces the risk of delays or complications at the border, ensuring smooth movement of goods.

Both numbers facilitate proper documentation and record-keeping, enhancing compliance with local and international regulations.

To add the VAT and EORI numbers in SAPIENT, follow the steps as explained in the following procedure.

1. In the left navigation panel, select **Customs Settings** > **VAT and EORI Numbers**.

<Image alt="Accessing VAT/EORI numbers" align="center" border={true} src="https://files.readme.io/d2f5fc850cb7428b8d4fe11242188b656639184480dd01c0e9eebe3cd144f15b-VAT_and_EORI_Numbers_option.png">
  Accessing VAT/EORI numbers
</Image>

2. In the **VAT and EORI Numbers** page that opens, select ![alt text](https://files.readme.io/cfc581cdc313b6976001d824d376acaf887d052bb884f729d8a58d5d1577f166-Add_VAT-EORI_number_button.png).

<Image alt="Accessing option to add VAT/EORI number" align="center" border={true} src="https://files.readme.io/97201a3c79a244f53d8d8772dbe7b397a5b6332c1d568a93ecdcad4fc97aa783-Add_vat_and_eori_numbers_option.png">
  Accessing option to add VAT/EORI number
</Image>

3. In the **Add VAT/EORI Number** form that opens, in the **SHIPPING ACCOUNT** block, from the dropdown menu, select the <Glossary>shipping account</Glossary> for which you want to add the VAT/EORI number.

<Image alt="Selecting shipping account  " align="center" border={true} src="https://files.readme.io/4a14d44448f074b3ef3ae91182eb8f8cee848e50bb9da74ad642b26627ae7259-Shipping_account_block_3.png">
  Selecting shipping account  
</Image>

4. After, in the **VAT/EORI NUMBER** block that appears, enter the necessary information as explained in the following table.
5. <Image alt="Entering VAT/EORI number and its details" align="center" border={true} src="https://files.readme.io/7c7d4e9ebcc049fcd2bd43fac3ce92d73d2f654b832d368199aeb91eb9e830e5-VAT-EORI_Number_block.png">
     Entering VAT/EORI number and its details
   </Image>

<AsteridkForMandatoryElements />

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
        From the dropdown menu, select the <Glossary>shipping location</Glossary> for which you want to add the VAT/EORI number.  

        You can also select **All** if you want to add the VAT/EORI number for all the existing shipping accounts. 
      </td>
    </tr>

    <tr>
      <td style={{ textAlign: "center" }}>
        **Country**
      </td>

      <td style={{ textAlign: "left" }}>
        From the dropdown menu, select the specific destination country for which you want to add the VAT/EORI number.  

        You may select **All** if you want to include all the countries (that are, countries grouped by European Union or <Glossary>ROW</Glossary> categories). 
      </td>
    </tr>

    <tr>
      <td style={{ textAlign: "center" }}>
        **Country Group**
      </td>

      <td style={{ textAlign: "left" }}>
        From the dropdown menu, select the country group for which you want to add the VAT/EORI number.  

        *Note: If you have selected a specific country in the**Country** field, then in this field, select **N/A**. Otherwise, select either **EuropeanUnion** or **RestOfTheWorld** options. In this case, the **Country** field value is set to **All**.*
      </td>
    </tr>

    <tr>
      <td style={{ textAlign: "center" }}>
        **Type\***
      </td>

      <td style={{ textAlign: "left" }}>
        From the dropdown menu, select any of the following types that you want to associate with your VAT/EORI number:  

        • **VAT**\
        • **EORI**
      </td>
    </tr>

    <tr>
      <td style={{ textAlign: "center" }}>
        **VAT/EORI Number**
      </td>

      <td style={{ textAlign: "left" }}>
        Enter your VAT/EORI number based on the selection you have made in the **Type** field.
      </td>
    </tr>

    <tr>
      <td style={{ textAlign: "center" }}>
        **Valid From\***
      </td>

      <td style={{ textAlign: "left" }}>
        From the date picker, select the date from which the VAT/EORI number you are adding is valid. 
      </td>
    </tr>
  </tbody>
</Table>

5. After entering the relevant information, select  ![alt text](https://files.readme.io/c741f8846981e5dbf335f391f4138a7fa3d215a56a14b681ad4fc6ae90bc7dec-Add_VAT-EORI_number_button_2.png). 

Once selected, the VAT/EORI added successfully and displays in the **VAT and EORI Numbers** list. Now, if the user does not send the shipper VAT or EORI in the **Create Shipment** request, and the shipment incoterms are <Glossary>DDU</Glossary> , and a VAT or EORI number exists for the destination country or country group in the UI, then the VAT or EORI setup in the UI will be used for the shipment.

> 💡 *Tip*
>
> If you want to remove the VAT/EORI, then in the **VAT and EORI Numbers** list, next to the one you want to delete, select ![alt text](https://files.readme.io/0979c7211f5ae99308ba3f765bd083d41949895562626a4f0cc33acd80b30762-Trash_icon.png).
>
> <Image alt="Deleting pre-registration number" align="center" border={true} src="https://files.readme.io/18854da926a99e35b6280bbb19445cac623a73a7f01d8cb9df4c99cd2a6fe6e9-Removing_item.png">
>   Deleting VAT/EORI number
> </Image>