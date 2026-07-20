---
title: Set up barcode range for International Arrival Containers
excerpt: >-
  A _barcode range_ for an International Arrival Container is a specific set of
  numbers designated for tracking containers arriving into the UK from overseas.
  These barcodes are used to uniquely identify containers at various stages of
  the shipping and handling process, facilitating efficient tracking and
  management.
deprecated: false
hidden: false
icon: fad fa-barcode-scan
metadata:
  robots: index
---
<br />

The barcode ranges functionality facilitates the <Glossary>Data Solution</Glossary> on behalf of customers who are shipping into the UK from abroad. This solution is dependent on the customer allocating a <Glossary>shipment</Glossary> into a <Glossary>container</Glossary> . When all the shipments for that container have been allocated and a container manifested, a summary barcode is produced.

This summary barcode, known as a WAND ID barcode is attached to the outside of the receptacle. As a result, an electronic Data Solution file is produced, in a predefined format and sent to Royal Mail, detailing the WAND ID and the individual shipment barcodes. It allows Royal Mail to process more efficiently shipments arriving in the UK.

In SAPIENT, you can add a barcode range under the **International Arrival Containers** API service to capture the data required to populate the Data Solution file.

## How to set up barcode range for International Arrival Containers

To add a barcode range for International Arrival Containers in SAPIENT, perform the steps as explained in the following procedure.

<ToggleList>
  <ToggleListItem title="1. Select Integrations page" icon="fa-solid fa-1">

    <br />

    In the left navigation panel, select **Integrations**.

    <Image align="center" border={true} src="https://files.readme.io/84039ea8d38560195f244c1aba1f5fdc49e22260967548a94b5ddc56e5c79c00-Accessing_Integrations_option.png" alt="Accessing integrations" />

    ***
  </ToggleListItem>

  <br />

  <ToggleListItem title="2. Select the Labels integration" icon="fa-solid fa-2">

    <br />

    In the list of carrier integrations that appears, next to Royal Mail, select **LABELS**.

    <Image align="center" border={true} src="https://files.readme.io/3d5109652b0b0cee5b6649c52dc92786f106840ba45e6ecea801be23f2b8d6af-Labels_option.png" alt="Accessing labels integration" />

    ***
  </ToggleListItem>

  <br />

  <ToggleListItem title="3.: Configure Labels integration" icon="fa-solid fa-3">

    <br />

    On the page that opens, under the **Available Integrations** block, in the **LABELS** section, select **CONFIGURE**.

    <Image align="center" border={true} src="https://files.readme.io/dc329170de3da55ba71a66858dc11d115904b5001362a12f87aea85d0e7656f4-Configure_labels_option.png" alt="Configuring labels integration" />

    ***
  </ToggleListItem>

  <br />

  <ToggleListItem title="4. Enter customer number and save" icon="fa-solid fa-4">

    <br />

    In the **Configure Royal Mail** page that opens, select the **International Arrivals Container Settings** tab. In the page that opens, enter your six-digit customer number provided to you by our onboarding team and then select ![](https://files.readme.io/7c98764e6500bab5bbcb768bbff9aa47d0681116fc91a6a2921c0394178f7550-Save_changes_button.png).

    ***
  </ToggleListItem>

  <br />

  <ToggleListItem title="5. Add barcode range" icon="fa-solid fa-5">

    <br />

    Once you are added, select ![](https://files.readme.io/d48a6a38086006b7b6e7e4edaaabed26a14571fe2fe075d2749bd142ac31f03f-Add_barcode_range_button.png).

    <Image align="center" border={true} src="https://files.readme.io/b97eed8bcf06eb4bc0f3d303c0758e223459b710117e7e2464410003bd430bcb-Add_barcode_range_option.png" alt="Accessing option to add barcode range" />

    ***
  </ToggleListItem>

  <br />

  <ToggleListItem title="6. Enter  barcode range details" icon="fa-solid fa-6">

    <br />

    In the **Barcode Range Details** form that opens, enter the necessary information as explained in the following table.

    <Image align="center" border={true} src="https://files.readme.io/f034c697c47c3c50bea13ef9821e4caec23a81ca1fc2252ab2457489d0c2a745-Barcode_range_details_form.png" alt="Entering barcode range details" />
    <br />

    <AsteridkForMandatoryElements />

    |      Element     | Description                                                                                                                                                                                                                                                                                                                            |
    | :--------------: | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
    |   **Prefix**\*   | Enter a fixed set of characters to be added at the beginning of the barcode numbers. It often indicates the type of shipment or the service provider, helping to categorize items within the system.                                                                                                                                   |
    | **Seed Start**\* | Enter the initial numbers in the barcode range. It marks the beginning of the numbering sequence for the barcodes to be generated, establishing where the sequence will commence.                                                                                                                                                      |
    |  **Seed End**\*  | Enter the final numbers in the barcode range. It denotes the endpoint of the numbering sequence, determining how many unique barcodes can be created within that range.                                                                                                                                                                |
    | **Total Number** | Represents the total count of unique barcodes that can be generated within the specified range, calculated as the difference between the seed end and seed start plus one (that is, Seed End - Seed Start + 1).                                                                                                                        |
    |   **Calculate**  | Select ![](https://files.readme.io/530aac60a4604cd28b9c5f84111d35151d47395157c95e3c0a1ef527b7fd4e02-Calculate_button.png) to compute the total number of barcodes based on the seed start and seed end fields. It validates the range and ensures consistency by recalculating the total whenever changes are made to the seed values. |

    <br />

    Once the relevant information is entered, select ![](https://files.readme.io/79e0cb9c566226cd8b320dc3529f556e5d94e2faa0622645bd0bc2c572957cab-Add_barcode_range_button_2.png) to save and add the barcode. You can now use this barcode range in your [manifest shipments](https://docs.intersoftsapient.net/reference/post_v4-manifests-carriercode) request for International Arrival Containers. When the international arrival container is manifested, the Data Solution file is sent to Royal Mail via SFTP.
  </ToggleListItem>
</ToggleList>

<Callout icon="💡" theme="default">
  ### _Tip_

  _For development and testing purposes the Customer Number can be filled with dummy details. The Barcode Range used for testing purposes should be AC40000001 to AC49999999. Production details will be provided to you when your account is switched onto production._
</Callout>

***

### See also

<Cards columns={2}>
  <Card title="ASCAN flow" href="https://docs.intersoftsapient.net/docs/internation-arrival-containers-ascan-flow#/" icon="fa-solid fa-barcode-read" target="_blank">
    Learn how the **International Arrivals Containers** process works and get to know the entire journey of the UK arrival containers on the fly.
  </Card>

  <Card title="International Arrivals Containers API" href="https://docs.intersoftsapient.net/reference/post_v4-internationalarrivalscontainers-rm#/" icon="fa-solid fa-gear-complex-code">
    Create and name (with and ID or alias) a new international arrivals container to be used for manifesting a specific group of shipments.
  </Card>
</Cards>

<Cards columns={2}>
  <Card title="A-scan FAQs" href="https://docs.intersoftsapient.net/docs/a-scan-faqs#/" icon="fa-solid fa-messages-question">
    Frequently asked questions regarding the International Arrivals Container API.
  </Card>
</Cards>

<br />
