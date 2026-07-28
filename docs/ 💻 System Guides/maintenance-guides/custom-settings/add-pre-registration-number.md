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
icon: fad fa-square-plus
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
Some countries operate a Tax Pre-Registration scheme, for example, VOEC in Norway, GST in Australia, and so on. If you are registered for a Tax Pre-Registration scheme for the destination country and are shipping under the scheme rules, then you must provide the <Glossary>Pre-registration number</Glossary> for the destination country.

<Callout icon="🚧" theme="warn">
  ### _Important_

  _The pre-registration number is only relevant for <Glossary>shipments</Glossary> with the <Glossary>DDU</Glossary> <Glossary>incoterms</Glossary>. If not provided in the&#x20;_**_Create Shipment_**_&#x20;API request and the shipment incoterms are set to DDU, then any pre-registration numbers that are set for your account in the&#x20;_**_Customs Settings_**_&#x20;GUI are used._
</Callout>

In SAPIENT, you can add the pre-registration number to ensure compliance with international shipping regulations and customs processes. This number facilitates smoother clearance of goods at customs, reducing delays in shipment and helps maintain accurate records of shipments for auditing and tracking purposes.

## How to add pre-registration number

To add a pre-registration number via the SAPIENT UI, perform the steps as explained in the following procedure.

<ToggleList>
  <ToggleListItem title={<strong>1. Access Pre-registration numbers</strong>} icon="fa-rocket">
    <br />

    In the left navigation panel, select **Customs Settings** > **Pre-Registration Numbers**.

    <Image align="center" border={true} src="https://files.readme.io/52fba08b346b45d4888a1dc14a06bf395cc4b30bdd9eeec98113d4c2fa2e416f-Pre-registration_numbers_option.png" caption="Accessing pre-registration numbers" />

    ***
  </ToggleListItem>

  <br />

  <ToggleListItem title={<strong>2. Start adding new number</strong>} icon="fa-rocket">
    <br />

    In the **Pre-Registration Numbers** page that opens, select ![](https://files.readme.io/574f2d3dd4cce77a9cde0e299f8a2f591fab81c8c7b4b49266c81ed4528c661d-Add_pre-registration_number_button.png).

    <Image align="center" src="https://files.readme.io/d7897eb60920589421496b60ad5a80cb6864a92a17cfb7f3f5aa143994d24e65-Add_pre-registration_number_option.png" caption="Accessing option to add pre-registration number" />

    ***
  </ToggleListItem>

  <br />

  <ToggleListItem title={<strong>3. Select shipping account </strong>} icon="fa-rocket">
    <br />

    In the **Add Pre-Registration Number** form that opens, in the **SHIPPING ACCOUNT** block, from the dropdown menu, select the <Glossary>shipping account</Glossary> for which you want to add the pre-registration number.

    <Image align="center" border={true} src="https://files.readme.io/1eec0cd1bf0612547a50a5de7866c9467f0e0faaff330c61093b16e411869a0f-Shipping_account_block_2.png" caption="Selecting shipping account" />

    ***
  </ToggleListItem>

  <br />

  <ToggleListItem title={<strong>4. Enter pre-regitsration details </strong>} icon="fa-rocket">
    <br />

    After selecting the shipping account, in the **PRE-REGISTRATION NUMBER** block that appears, enter the necessary information as explained in the following table.

    <Image align="center" border={true} src="https://files.readme.io/e915ba8ed9b9e03c3d9a7662a7ce8fca175d3a707b9348ab7509b35df51fed36-Pre-registration_number_block.png" caption="Entering pre-registration number and its details" />

    <br />

    <AsteridkForMandatoryElements />

    <table>
      <thead>
        <tr>
          <th align="center">Element</th>
          <th align="left">Description</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td align="center"><strong>Shipping Location</strong></td>
          <td align="left">From the dropdown menu, select the <Glossary>shipping location</Glossary> for which you want to add the pre-registration number.<br /><br />You can also select <strong>All</strong> if you want to add a pre-registration number for all the existing shipping accounts.</td>
        </tr>
        <tr>
          <td align="center"><strong>Country</strong></td>
          <td align="left">From the dropdown menu, select the specific destination country for which you want to add the pre-registration number.<br /><br />You may select <strong>All</strong> if you want to include all the countries (that are, countries grouped by European Union or <Glossary>ROW</Glossary> categories).</td>
        </tr>
        <tr>
          <td align="center"><strong>Country Group</strong></td>
          <td align="left">From the dropdown menu, select the country group for which you want to add the pre-registration number.<br /><br /><em><code>Note</code></em>: If you have selected a specific country in the <strong>Country</strong> field, then in this field, select <strong>N/A</strong>. Otherwise, select either <strong>EuropeanUnion</strong> or <strong>RestOfTheWorld</strong> options. In this case, the <strong>Country</strong> field value is set to <strong>All</strong>.</td>
        </tr>
        <tr>
          <td align="center"><strong>Type</strong>&#42;</td>
          <td align="left">From the dropdown menu, select any of the following types that you want to associated with your pre-registration number:<br /><br /><ul><li><Glossary>OSS</Glossary></li><li><Glossary>IOSS</Glossary></li><li><Glossary>GST</Glossary></li><li><strong>Other, please specify</strong>: choose this option only if the type you want to specify is other than the ones mentioned in this dropdown field.</li></ul></td>
        </tr>
        <tr>
          <td align="center"><strong>Other Type</strong></td>
          <td align="left">This field is only available if you have selected the <strong>Other, please specify</strong> option in the <strong>Type</strong> field.<br /><br />Enter the type that you want to associate with the pre-registration number you are adding.</td>
        </tr>
        <tr>
          <td align="center"><strong>Pre-Registration Number</strong>&#42;</td>
          <td align="left">Enter your pre-registration number.</td>
        </tr>
        <tr>
          <td align="center"><strong>Valid From</strong>&#42;</td>
          <td align="left">From the date picker, select the date from which the pre-registration number you are adding is valid.</td>
        </tr>
      </tbody>
    </table>

    ***
  </ToggleListItem>

  <br />

  <ToggleListItem title={<strong>5. Save the configuration </strong>} icon="fa-rocket">
    <br />

    After entering the relevant information, select ![]("https://files.readme.io/5041628c1ebe60cd9a698ff4068b10ef8341649edfe2e513e460f7afddb93d08-Add_pre-registration_number_button_2.png).

    Once selected, the pre-registration number is added successfully and displays in the **Pre-Registration Numbers** list. You can now use this number in your [Create Shipment](https://docs.intersoftsapient.net/reference/post_v4-shipments-rm) request.

    <Callout icon="💡" theme="default">
      ### *Tip*

      *If you want to remove the pre-registration number, then in the **Pre-Registration Numbers** list, next to the number you want to delete, select the following icon.*

      <Image align="center" src="https://files.readme.io/0979c7211f5ae99308ba3f765bd083d41949895562626a4f0cc33acd80b30762-Trash_icon.png" caption="Delete pre-registration number icon" />

      <Image align="center" border={true} src="https://files.readme.io/18854da926a99e35b6280bbb19445cac623a73a7f01d8cb9df4c99cd2a6fe6e9-Removing_item.png" caption="Deleting pre-registration number" />
    </Callout>
  </ToggleListItem>
</ToggleList>

<br />
