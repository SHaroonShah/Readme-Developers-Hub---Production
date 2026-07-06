---
title: Add VAT and EORI number
excerpt: >-
  _Value Added Tax (VAT)_ numbers are essential for businesses engaged in
  trading goods and services across different countries, particularly in the
  European Union. It allows businesses to charge or reclaim VAT on sales and
  purchases. On the other hand, The _Economic Operators Registration and
  Identification (EORI)_ number is necessary for businesses involved in customs
  activities within the EU. It is used to identify traders in customs systems.
deprecated: false
hidden: false
icon: fad fa-square-plus
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
## Understanding VAT and EORI numbers

<Cards columns={2}>
  <Card title="VAT Number" icon="fa-solid fa-calculator">
    **Value Added Tax (VAT)** numbers are essential for businesses engaged in trading goods and services across different countries, particularly in the European Union. It allows businesses to charge or reclaim VAT on sales and purchases.
  </Card>

  <Card title="EORI Number" icon="fa-solid shipping-fast">
    **Economic Operators Registration and Identification (EORI)** number is necessary for businesses involved in customs activities within the EU. It is used to identify traders in customs systems.
  </Card>
</Cards>

***

## Benefits

<Columns layout="auto">
  <Column>
    **VAT Number:**

    * Ensures proper tax handling during cross-border transactions
    * Enables VAT compliance with local and international regulations
    * Facilitates proper documentation and record-keeping
  </Column>

  <Column>
    **EORI Number:**

    * Expedites customs clearance processes
    * Reduces risk of delays or complications at borders
    * Ensures smooth movement of goods across EU boundaries
  </Column>
</Columns>

***

## How to add VAT and EORI Numbers

To add the VAT and EORI numbers in SAPIENT, perform the steps as explained in the following procedure.

<ToggleList>
  <ToggleListItem title={<strong>1. Access VAT and EORI settings</strong>} icon="fa-rocket">
    <br />

    In the left navigation panel, select **Customs Settings** > **VAT and EORI Numbers**.

    <Image align="center" border={true} src="https://files.readme.io/d2f5fc850cb7428b8d4fe11242188b656639184480dd01c0e9eebe3cd144f15b-VAT_and_EORI_Numbers_option.png" alt="Accessing VAT/EORI numbers" />

    ***
  </ToggleListItem>

  <br />

  <ToggleListItem title={<strong>2. Access option to add VAT and EORI Number</strong>} icon="fa-rocket">
    <br />

    In the **VAT and EORI Numbers** page that opens, select ![alt text](https://files.readme.io/cfc581cdc313b6976001d824d376acaf887d052bb884f729d8a58d5d1577f166-Add_VAT-EORI_number_button.png).

    <Image align="center" border={true} src="https://files.readme.io/97201a3c79a244f53d8d8772dbe7b397a5b6332c1d568a93ecdcad4fc97aa783-Add_vat_and_eori_numbers_option.png" alt="Accessing option to add VAT/EORI number" />

    ***
  </ToggleListItem>

  <br />

  <ToggleListItem title={<strong>3. Select shipping account </strong>} icon="fa-rocket">
    <br />

    In the **Add VAT/EORI Number** form that opens, in the **SHIPPING ACCOUNT** block, from the dropdown menu, select the <Glossary>shipping account</Glossary> for which you want to add the VAT/EORI number.

    <Image align="center" border={true} src="https://files.readme.io/4a14d44448f074b3ef3ae91182eb8f8cee848e50bb9da74ad642b26627ae7259-Shipping_account_block_3.png" alt="Selecting shipping account" />

    ***
  </ToggleListItem>

  <br />

  <ToggleListItem title={<strong>4. Enter VAT/EORI details </strong>} icon="fa-rocket">
    <br />

    In the **VAT/EORI NUMBER** block that appears, enter the necessary information as detailed in the configuration table below.

    <Image align="center" border={true} src="https://files.readme.io/7c7d4e9ebcc049fcd2bd43fac3ce92d73d2f654b832d368199aeb91eb9e830e5-VAT-EORI_Number_block.png" alt="Entering VAT/EORI number and its details" />

    <br />

    <AsteridkForMandatoryElements />

    <Table align={["center","left"]}>
      <thead>
        <tr>
          <th>
            Element
          </th>

          <th>
            Description
          </th>
        </tr>
      </thead>

      <tbody>
        <tr>
          <td>
            **Shipping Location**
          </td>

          <td>
            From the dropdown menu, select the <Glossary>shipping location</Glossary> for which you want to add the VAT/EORI number.
            You can also select **All** if you want to add the VAT/EORI number for all the existing shipping accounts.
          </td>
        </tr>

        <tr>
          <td>
            **Country**
          </td>

          <td>
            From the dropdown menu, select the specific destination country for which you want to add the VAT/EORI number.
            You may select **All** if you want to include all the countries (that are, countries grouped by European Union or <Glossary>ROW</Glossary> categories).
          </td>
        </tr>

        <tr>
          <td>
            **Country Group**
          </td>

          <td>
            From the dropdown menu, select the country group for which you want to add the VAT/EORI number.
            *Note: If you have selected a specific country in the**Country** field, then in this field, select **N/A**. Otherwise, select either **EuropeanUnion** or **RestOfTheWorld** options. In this case, the **Country** field value is set to **All**.*
          </td>
        </tr>

        <tr>
          <td>
            **Type**\*
          </td>

          <td>
            From the dropdown menu, select any of the following types that you want to associate with your VAT/EORI number:
            • **VAT**
            • **EORI**
          </td>
        </tr>

        <tr>
          <td>
            **VAT/EORI Number**
          </td>

          <td>
            Enter your VAT/EORI number based on the selection you have made in the **Type** field.
          </td>
        </tr>

        <tr>
          <td>
            **Valid From**\*
          </td>

          <td>
            From the date picker, select the date from which the VAT/EORI number you are adding is valid.
          </td>
        </tr>
      </tbody>
    </Table>

    ***
  </ToggleListItem>

  <br />

  <ToggleListItem title={<strong>5. Save the configuration </strong>} icon="fa-rocket">
    <br />

    After entering the relevant information, select ![](https://files.readme.io/c741f8846981e5dbf335f391f4138a7fa3d215a56a14b681ad4fc6ae90bc7dec-Add_VAT-EORI_number_button_2.png).

    Once selected, the VAT/EORI is added successfully and displays in the **VAT and EORI Numbers** list. Now, if the user does not send the shipper VAT or EORI in the **Create Shipment** request, and the shipment incoterms are <Glossary>DDU</Glossary>, and a VAT or EORI number exists for the destination country or country group in the UI, then the VAT or EORI setup in the UI will be used for the shipment.

    <Callout icon="💡" theme="default">
      ### *Tip*

      *If you want to remove the VAT and EORI number, then in the**VAT and EORI Numbers** list, next to the one you want to delete, select  ![alt text](https://files.readme.io/0979c7211f5ae99308ba3f765bd083d41949895562626a4f0cc33acd80b30762-Trash_icon.png).*

      <Image align="center" border={true} src="https://files.readme.io/18854da926a99e35b6280bbb19445cac623a73a7f01d8cb9df4c99cd2a6fe6e9-Removing_item.png" alt="Deleting VAT/EORI number" />
    </Callout>
  </ToggleListItem>
</ToggleList>