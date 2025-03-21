---
title: Set up international arrival containers
excerpt: >-
  A _barcode range_ for an international arrival container is a specific set of
  numbers designated for tracking containers arriving into the UK from overseas.
  These barcodes are used to uniquely identify containers at various stages of
  the shipping and handling process, facilitating efficient tracking and
  management.
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
The barcode ranges functionality facilitates the <Glossary>data solution</Glossary> on behalf of customers who are shipping into the UK from abroad. This solution is dependent on the customer scanning a <Glossary>shipment</Glossary> into a <Glossary>container</Glossary> . When all the shipments for that container have been scanned, a summary barcode is produced.

This summary barcode, known as a WAND ID barcode is attached to the outside of the receptacle. As a result, an electronic data solution file is produced, in a predefined format and sent to Royal Mail, detailing the WAND ID and the individual shipment barcodes. This enables a link between the WAND ID used on a container and the tracking numbers of the shipments held within it.

IN SAPIENT, you can add a barcode range under the **International Arrival Containers** API service to capture the data required to populate the data solution file.

To add a barcode range for international arrival containers in SAPIENT, follow the steps as explained in the following procedure.

1. In the left navigation panel, select **Integrations**.

<Image align="center" alt="Accessing integrations" border={true} caption="Accessing integrations" src="https://files.readme.io/84039ea8d38560195f244c1aba1f5fdc49e22260967548a94b5ddc56e5c79c00-Accessing_Integrations_option.png" />

2. In the list of carrier integrations that appears, next to Royal Mail, select **LABELS**.

<Image align="center" alt="Accessing labels integration" border={true} caption="Accessing labels integration" src="https://files.readme.io/3d5109652b0b0cee5b6649c52dc92786f106840ba45e6ecea801be23f2b8d6af-Labels_option.png" />

3. On the page that opens, under the **Available Integrations** block, in the **LABELS** section, select **CONFIGURE**.

<Image align="center" alt="Configuring labels integration" border={true} caption="Configuring labels integration" src="https://files.readme.io/dc329170de3da55ba71a66858dc11d115904b5001362a12f87aea85d0e7656f4-Configure_labels_option.png" />

4. In the **Configure Royal Mail** page that opens, select the **International Arrivals Container Settings** tab. In the page that opens, enter your six-digit customer number provided to you by our onboarding team and then select ![alt text](https://files.readme.io/7c98764e6500bab5bbcb768bbff9aa47d0681116fc91a6a2921c0394178f7550-Save_changes_button.png).
5. Once you are added, select ![alt text](https://files.readme.io/d48a6a38086006b7b6e7e4edaaabed26a14571fe2fe075d2749bd142ac31f03f-Add_barcode_range_button.png).

<Image align="center" alt="Accessing option to add barcode range" border={true} caption="Accessing option to add barcode range" src="https://files.readme.io/b97eed8bcf06eb4bc0f3d303c0758e223459b710117e7e2464410003bd430bcb-Add_barcode_range_option.png" />

5. In the **Barcode Range Details** form that opens, enter the necessary information as explained in the following table.

<Image align="center" alt="Entering barcode range details" border={true} caption="Entering barcode range details" src="https://files.readme.io/f034c697c47c3c50bea13ef9821e4caec23a81ca1fc2252ab2457489d0c2a745-Barcode_range_details_form.png" />

<AsteridkForMandatoryElements />

|      Element     | Description                                                                                                                                                                                                                                                                                                                                    |
| :--------------: | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
|   **Prefix\***   | Enter a fixed set of characters to be added at the beginning of the barcode numbers. It often indicates the type of shipment or the service provider, helping to categorize items within the system.                                                                                                                                           |
| **Seed Start\*** | Enter the initial numbers in the barcode range. It marks the beginning of the numbering sequence for the barcodes to be generated, establishing where the sequence will commence.                                                                                                                                                              |
|  **Seed End\***  | Enter the final numbers in the barcode range. It denotes the endpoint of the numbering sequence, determining how many unique barcodes can be created within that range.                                                                                                                                                                        |
| **Total Number** | Represents the total count of unique barcodes that can be generated within the specified range, calculated as the difference between the seed end and seed start plus one (that is, Seed End - Seed Start + 1).                                                                                                                                |
|   **Calculate**  | Select ![alt text](https://files.readme.io/530aac60a4604cd28b9c5f84111d35151d47395157c95e3c0a1ef527b7fd4e02-Calculate_button.png) to compute the total number of barcodes based on the seed start and seed end fields. It validates the range and ensures consistency by recalculating the total whenever changes are made to the seed values. |

Once the relevant information is entered, select ![alt text](https://files.readme.io/79e0cb9c566226cd8b320dc3529f556e5d94e2faa0622645bd0bc2c572957cab-Add_barcode_range_button_2.png) to save and add the bar code. You can now use this bar code range in your [manifest shipments](https://docs.intersoftsapient.net/reference/post_v4-manifests-carriercode) request for international arrival containers. When the international arrival container is manifested, the data solution UK arrivals file is sent to Royal Mail via SFTP.

<Cards columns={4}>
  <Card title="ASCAN flow" href="https://docs.intersoftsapient.net/docs/internation-arrival-containers-ascan-flow#/" icon="fas fa-bezier-curve" target="_blank">
    Neque porro quisquam est qui dolorem ipsum quia
  </Card>

  <Card title="Internation Arrivals Containers API" href="https://docs.intersoftsapient.net/reference/post_v4-internationalarrivalscontainers-rm#/" icon="fa-solid fa-gear-complex-code">
    *Lorem ipsum dolor sit amet, consectetur adipiscing elit*
  </Card>

  <Card title="Third Card" icon="fa-star">
    > Ut enim ad minim veniam, quis nostrud ullamco
  </Card>

  <Card title="Fourth Card" icon="fa-question">
    **Excepteur sint occaecat cupidatat non proident**
  </Card>
</Cards>