---
title: Set up a barcode range for International Arrival Containers
excerpt: >-
  A barcode range is a set of numbers used to identify and track International
  Arrival Containers arriving in the UK. Each container is assigned a unique
  barcode number from this range.
deprecated: false
hidden: false
icon: fad fa-barcode-scan
metadata:
  robots: index
---
<br />

The barcode range is used as part of the <Glossary>Data Solution</Glossary> for shipments being imported into the UK.<br />Shipments must be allocated to an International Arrival Container. When all shipments have been allocated and the container is manifested, a container barcode is generated.

The container barcode, known as the WAND ID barcode, is attached to the outside of the container. <br />A Data Solution file is then generated and sent to Royal Mail. The file contains the WAND ID and the individual shipment barcodes, allowing Royal Mail to identify the container and the shipments allocated to it.

In SAPIENT, set up a barcode range under the International Arrival Containers (A-Scan) service. The barcode range provides the container barcode numbers required for the Data Solution file.

## How to set up a barcode range for International Arrival Containers

Follow the steps below to set up a barcode range in SAPIENT.

<ToggleList>
  <ToggleListItem title="1. Open the Integrations page" icon="fa-solid fa-1">

    <br />

    In the left navigation panel, select **Integrations**.

    <Image align="center" border={true} src="https://files.readme.io/84039ea8d38560195f244c1aba1f5fdc49e22260967548a94b5ddc56e5c79c00-Accessing_Integrations_option.png" caption="Opening the Integrations page" />

    ***
  </ToggleListItem>

  <br />

  <ToggleListItem title="2. Select the Labels integration" icon="fa-solid fa-2">

    <br />

    In the Royal Mail section, select **LABELS**.

    <Image align="center" border={true} src="https://files.readme.io/3d5109652b0b0cee5b6649c52dc92786f106840ba45e6ecea801be23f2b8d6af-Labels_option.png" caption="Selecting the Royal Mail Labels integration" />

    ***
  </ToggleListItem>

  <br />

  <ToggleListItem title="3.: Configure the Labels integration" icon="fa-solid fa-3">

    <br />

    Under **Available Integrations**, in the **LABELS** section, select **CONFIGURE**.

    <Image align="center" border={true} src="https://files.readme.io/dc329170de3da55ba71a66858dc11d115904b5001362a12f87aea85d0e7656f4-Configure_labels_option.png" caption="Configuring the Labels integration" />

    ***
  </ToggleListItem>

  <br />

  <ToggleListItem title="4. Enter your Customer Number" icon="fa-solid fa-4">

    <br />

    On the **Configure Royal Mail** page, select the **International Arrivals Container Settings** tab. Enter the six-digit Customer Number provided by the Intersoft Onboarding team, then select ![](https://files.readme.io/7c98764e6500bab5bbcb768bbff9aa47d0681116fc91a6a2921c0394178f7550-Save_changes_button.png).

    ***
  </ToggleListItem>

  <br />

  <ToggleListItem title="5. Add a barcode range" icon="fa-solid fa-5">

    <br />

   Select ![](https://files.readme.io/d48a6a38086006b7b6e7e4edaaabed26a14571fe2fe075d2749bd142ac31f03f-Add_barcode_range_button.png).

    <Image align="center" border={true} src="https://files.readme.io/b97eed8bcf06eb4bc0f3d303c0758e223459b710117e7e2464410003bd430bcb-Add_barcode_range_option.png" caption="Adding a barcode range" />

    ***
  </ToggleListItem>

  <br />

  <ToggleListItem title="6. Enter  barcode range details" icon="fa-solid fa-6">

    <br />

    In the **Barcode Range Details** form, enter the required information as explained in the table below.

    <Image align="center" border={true} src="https://files.readme.io/f034c697c47c3c50bea13ef9821e4caec23a81ca1fc2252ab2457489d0c2a745-Barcode_range_details_form.png" caption="Entering barcode range details" />
    <br />

    <AsteridkForMandatoryElements />

    |      Element     | Description                                                                                                                                                                                                                                                                                                                            |
    | :--------------: | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
    |   **Prefix**\*   | Enter the prefix for the barcode range. The prefix is added at the beginning of each container barcode number.                                                                                                                              |
    | **Seed Start**\* | Enter the first number in the barcode range.                                                                                                                                      |
    |  **Seed End**\*  | Enter the last number in the barcode range.                                                                                                                                            |
    | **Total Number** | Shows the total number of barcodes available in the range. This is calculated as: Seed End - Seed Start + 1.                                                                                                                     |
    |   **Calculate**  | Select  ![](https://files.readme.io/530aac60a4604cd28b9c5f84111d35151d47395157c95e3c0a1ef527b7fd4e02-Calculate_button.png) to check the barcode range and calculate the Total Number. |

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

<Cards>
  <Card title="A-Scan Flow" href="https://docs.intersoftsapient.net/docs/internation-arrival-containers-ascan-flow#/" icon="fa-solid fa-barcode-read" target="_blank">
    Learn how the **International Arrivals Containers** process works and get to know the entire journey of the UK arrival containers on the fly.
  </Card>

  <Card title="International Arrivals Containers API" href="https://docs.intersoftsapient.net/reference/post_v4-internationalarrivalscontainers-rm#/" icon="fa-solid fa-gear-complex-code" target="_blank">
    Create and name (with and ID or alias) a new international arrivals container to be used for manifesting a specific group of shipments.
  </Card>
</Cards>

<Cards columns="2">
  <Card title="A-scan FAQs" href="https://docs.intersoftsapient.net/docs/a-scan-faqs#/" icon="fa-solid fa-messages-question">
    Frequently asked questions regarding the International Arrivals Container API.
  </Card>
</Cards>