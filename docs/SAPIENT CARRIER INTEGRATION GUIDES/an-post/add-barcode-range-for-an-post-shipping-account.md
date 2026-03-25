---
title: Add barcode range to An Post shipping account
excerpt: >-
  A _barcode range_ is a specific set of numbers designated for tracking
  shipments. These barcodes are used to uniquely identify shipments at various
  stages of the shipping and handling process, facilitating efficient tracking
  and management.
deprecated: false
hidden: false
metadata:
  robots: index
---
The primary purpose of creating barcodes is to facilitate efficient tracking and management of shipments. Barcodes allow for the easy identification of items at various points in the shipping process, from dispatch to delivery. By assigning a unique barcode to each <Glossary>shipment</Glossary>, An Post can streamline its operations and improve accuracy in handling processes.

In SAPIENT, for an An Post <Glossary>shipping account</Glossary>, you can add a separate barcode number range per customer account and service.

To add a barcode range for an An Post shipping account in SAPIENT, follow the steps as explained in the following procedure.

<Accordion title="Procedure" icon="fa-list-ol">

1. In the left navigation panel, select **Integrations**.

<Image align="center" alt="Accessing integrations" border={true} caption="Accessing integrations" src="https://files.readme.io/84039ea8d38560195f244c1aba1f5fdc49e22260967548a94b5ddc56e5c79c00-Accessing_Integrations_option.png" />

2. In the list of carrier integrations that appears, next to An Post, select **LABELS**.

<Image align="center" alt="Accessing labels integration" border={true} caption="Accessing labels integration" src="https://files.readme.io/73206c9fcae539ce5f93c960a128ac24b243ce68ee47e2102c15b2f08b6cc098-Accessing_an_post_label_integration.png" />

3. On the page that opens, under the **Available Integrations** block, in the **LABELS** section, select **CONFIGURE**.

<Image align="center" alt="Configuring labels integration" border={true} caption="Configuring labels integration" src="https://files.readme.io/96f212ec23ed9c9033e295654543c4d4571a1189801f779bfbcfa2a9d2b20ed5-Configuring_an_post_labels_integration.png" />

4. In the **Configure ANPOST** page that opens, select the **Barcode Ranges** tab and click ![](https://files.readme.io/d48a6a38086006b7b6e7e4edaaabed26a14571fe2fe075d2749bd142ac31f03f-Add_barcode_range_button.png).

<Image align="center" alt="Accessing option to add barcode range" border={true} caption="Accessing option to add barcode range" src="https://files.readme.io/96e322d52aad201fb3c72d60c68ff6c2796ceb6b72665a463abae2e96b8f4082-Selecting_an_post_barcode_range_tab.png" />

5. In the **Barcode Range Details** form that opens, enter the necessary information as explained in the following table.

<Image align="center" alt="Entering barcode range details" border={true} caption="Entering barcode range details" src="https://files.readme.io/c796a68058d34fce826f5fd4af9b779690559fa07e009194c9c2bbcc443b842a-Adding_an_post_barcode_range.png" />
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
        **Shipping Account**\*
      </td>

      <td>
        From the dropdown menu, select the An Post shipping account for which you are adding the barcode range.
      </td>
    </tr>

    <tr>
      <td>
        **Service**
      </td>

      <td>
        Enter the 2-digit service code that you want to use with your barcode range.

        *`Note`: To learn more about the An Post services, refer to the<a href="https://docs.google.com/spreadsheets/d/1Jp7nTCtK-nhORTupG_5iPgJy_B9oQR7YABfj3rkV1m4/edit?usp=sharing" target="_blank" rel="noopener noreferrer">An Post services list</a>.*
      </td>
    </tr>

    <tr>
      <td>
        **Prefix**\*
      </td>

      <td>
        Enter a fixed set of characters to be added at the beginning of the barcode numbers.

        *`Note`: Make sure the prefix correspond to the selected service. To learn more about the services and their prefixes, refer to the<a href="https://docs.google.com/spreadsheets/d/1Jp7nTCtK-nhORTupG_5iPgJy_B9oQR7YABfj3rkV1m4/edit?usp=sharing" target="_blank" rel="noopener noreferrer">An Post services list</a>.*
      </td>
    </tr>

    <tr>
      <td>
        **Starting Value**\*
      </td>

      <td>
        Enter the initial numbers in the barcode range. It marks the beginning of the numbering sequence for the barcodes to be generated, establishing where the sequence will commence.
      </td>
    </tr>

    <tr>
      <td>
        **End Value**\*
      </td>

      <td>
        Enter the final numbers in the barcode range. It denotes the endpoint of the numbering sequence, determining how many unique barcodes can be created within that range.
      </td>
    </tr>

    <tr>
      <td>
        **Total Number**
      </td>

      <td>
        Represents the total count of unique barcodes that can be generated within the specified range.
      </td>
    </tr>

    <tr>
      <td>
        **Calculate**
      </td>

      <td>
        Select ![](https://files.readme.io/530aac60a4604cd28b9c5f84111d35151d47395157c95e3c0a1ef527b7fd4e02-Calculate_button.png) to compute the total number of barcodes based on the starting value and end value. It validates the range and ensures consistency by recalculating the total whenever changes are made to the values.
      </td>
    </tr>
  </tbody>
</Table>

Once the relevant information is entered, select ![](https://files.readme.io/e5a8c301d9e4f9f09e3a21633bae40e536aaff09f96776a43aeea8162ece2a4b-Add_range_button.png) to save and add the barcode range. You can now use this barcode range for your shipments.

</Accordion>