---
title: Add barcode range to An Post shipping account
excerpt: >-
  A _barcode range_ is a specific set of numbers designated for tracking
  shipments. These barcodes are used to uniquely identify shipments at various
  stages of the shipping and handling process, facilitating efficient tracking
  and management.
deprecated: false
hidden: false
icon: fad fa-barcode-read
metadata:
  robots: index
---
The primary purpose of creating barcodes is to facilitate efficient tracking and management of shipments. Barcodes allow for the easy identification of items at various points in the shipping process, from dispatch to delivery. By assigning a unique barcode to each <Glossary>shipment</Glossary>, An Post can streamline its operations and improve accuracy in handling processes.

In SAPIENT, for an An Post <Glossary>shipping account</Glossary>, you can add a separate barcode number range per customer account and service.

## How to add barcode ranges to An Post shipping account

To add barcode ranges to An Post shipping account in SAPIENT, follow the steps as explained in the following procedure.

<ToggleList>
  <ToggleListItem title="1. Select the Integrations page">
    In the left navigation panel, select **Integrations**.

    <Image align="center" border={true} src="https://files.readme.io/84039ea8d38560195f244c1aba1f5fdc49e22260967548a94b5ddc56e5c79c00-Accessing_Integrations_option.png" caption="Integrations option in the navigation panel" />

    ***
  </ToggleListItem>

  <br />

  <ToggleListItem title="2. Select the LABELS integration for An Post">
    In the list of carrier integrations that appears, next to An Post, select **LABELS**.

    <Image align="center" border={true} src="https://files.readme.io/73206c9fcae539ce5f93c960a128ac24b243ce68ee47e2102c15b2f08b6cc098-Accessing_an_post_label_integration.png" caption="An Post LABELS integration" />

    ***
  </ToggleListItem>

  <br />

  <ToggleListItem title="3. Configure the LABELS integration">
    On the page that opens, under the **Available Integrations** block, in the **LABELS** section, select **CONFIGURE**.

    <Image align="center" border={true} src="https://files.readme.io/96f212ec23ed9c9033e295654543c4d4571a1189801f779bfbcfa2a9d2b20ed5-Configuring_an_post_labels_integration.png" caption="Configure option for the An Post LABELS integration" />

    ***
  </ToggleListItem>

  <br />

  <ToggleListItem title="4. Add a barcode range">
    In the **Configure ANPOST** page that opens, select the **Barcode Ranges** tab and click <Image src="https://files.readme.io/d48a6a38086006b7b6e7e4edaaabed26a14571fe2fe075d2749bd142ac31f03f-Add_barcode_range_button.png" caption="Add barcode range button" />.

    <Image align="center" border={true} src="https://files.readme.io/96e322d52aad201fb3c72d60c68ff6c2796ceb6b72665a463abae2e96b8f4082-Selecting_an_post_barcode_range_tab.png" caption="Barcode Ranges tab and add barcode range option" />

    ***
  </ToggleListItem>

  <br />

  <ToggleListItem title="5. Enter barcode range details">
    In the **Barcode Range Details** form that opens, enter the necessary information as explained in the following table.

    <Image align="center" border={true} src="https://files.readme.io/c796a68058d34fce826f5fd4af9b779690559fa07e009194c9c2bbcc443b842a-Adding_an_post_barcode_range.png" caption="Barcode Range Details form" />

    <br />

    <AsteridkForMandatoryElements />

    |         Element        | Description                                                                                                                                                                                                                                                                                                                                                                                                             |
    | :--------------------: | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
    | **Shipping Account**\* | From the dropdown menu, select the An Post shipping account for which you are adding the barcode range.                                                                                                                                                                                                                                                                                                                 |
    |       **Service**      | Enter the 2-digit service code that you want to use with your barcode range.<br /><br />*`Note`: To learn more about the An Post services, refer to the<a href="https://docs.google.com/spreadsheets/d/1Jp7nTCtK-nhORTupG_5iPgJy_B9oQR7YABfj3rkV1m4/edit?usp=sharing" target="_blank" rel="noopener noreferrer">An Post services list</a>.*                                                                             |
    |      **Prefix**\*      | Enter a fixed set of characters to be added at the beginning of the barcode numbers.<br /><br />*`Note`: Make sure the prefix correspond to the selected service. To learn more about the services and their prefixes, refer to the<a href="https://docs.google.com/spreadsheets/d/1Jp7nTCtK-nhORTupG_5iPgJy_B9oQR7YABfj3rkV1m4/edit?usp=sharing" target="_blank" rel="noopener noreferrer">An Post services list</a>.* |
    |  **Starting Value**\*  | Enter the initial numbers in the barcode range. It marks the beginning of the numbering sequence for the barcodes to be generated, establishing where the sequence will commence.                                                                                                                                                                                                                                       |
    |     **End Value**\*    | Enter the final numbers in the barcode range. It denotes the endpoint of the numbering sequence, determining how many unique barcodes can be created within that range.                                                                                                                                                                                                                                                 |
    |    **Total Number**    | Represents the total count of unique barcodes that can be generated within the specified range.                                                                                                                                                                                                                                                                                                                         |
    |      **Calculate**     | Select <Image src="https://files.readme.io/530aac60a4604cd28b9c5f84111d35151d47395157c95e3c0a1ef527b7fd4e02-Calculate_button.png" caption="Calculate button" /> to compute the total number of barcodes based on the starting value and end value. It validates the range and ensures consistency by recalculating the total whenever changes are made to the values.                                                                                         |

    ***
  </ToggleListItem>

  <br />

  <ToggleListItem title="6. Save and add the barcode range">
    Once the relevant information is entered, select <Image src="https://files.readme.io/e5a8c301d9e4f9f09e3a21633bae40e536aaff09f96776a43aeea8162ece2a4b-Add_range_button.png" caption="Add range button" /> to save and add the barcode range.

    You can now use this barcode range for your shipments.
  </ToggleListItem>
</ToggleList>

***

### See also

<Cards columns="2">
  <Card title="Add Shipping Account" href="https://docs.intersoftsapient.net/docs/add-an-post-shipping-account" icon="fa-solid fa-truck">
    Access the step-by-step guide on how to set up An Post shipping account on SAPIENT.
  </Card>
</Cards>