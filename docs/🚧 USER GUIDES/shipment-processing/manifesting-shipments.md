---
title: Manifest shipment
excerpt: >-
  Learn how to manifest shipments in SAPIENT through the UI, including filtering
  options, step-by-step procedures, and best practices for efficient shipment
  processing.
deprecated: false
hidden: false
icon: fad fa-cart-flatbed-empty
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
In this stage, shipments are being prepared for processing into a shipping manifest, which is a document listing all shipments to be sent together. This process involves gathering details about each shipment, allowing users to finalise the manifest and generate shipping labels for efficient despatch.

In SAPIENT, you can <Glossary>manifest</Glossary> the <Glossary>shipment</Glossary> in several ways:

<Cards columns="2">
  <Card title="Container-based manifesting" href="https://docs.intersoftsapient.net/docs/manifest-shipments-in-a-container" icon="fa-solid fa-container-storage">
    Manifest shipments grouped within a specific container
  </Card>

  <Card title="Status-based manifesting" href="https://docs.intersoftsapient.net/docs/manifest-shipments-by-picked-status" icon="fa-solid fa-check-circle">
    Manifest shipments filtered by their Picked status
  </Card>
</Cards>

You can also manifest shipments by:

- Shipping location
- Shipping account
- Service code

<Callout icon="💡" theme="default">
  ### _Tip_

  _You can manifest shipments both via UI and API._
</Callout>

## How to manifest shipment

<Tabs>
  <Tab title="Manifest via SAPIENT UI">
    

    To manifest a shipment in SAPIENT, perform the steps as explained in the following procedure.

    <ToggleList>
      <ToggleListItem title={<strong>1. Access the manifesting option</strong>} icon="fa-rocket">
        <br />

        In the side navigation panel, select the **Shipment Processing** > **Manifesting** option.

        <Image align="center" border={true} src="https://files.readme.io/43b41b65377780fd19531fd2378483c9b0c7d99c88b2c5242e584ef4225c5dae-Accessing_manifesting_option.png" alt="Accessing shipments" />

        ***
      </ToggleListItem>

      <br />

      <ToggleListItem title={<strong>2. Configure filters and sorting</strong>} icon="fa-rocket">
        <br />

        In the **Manifesting** page that opens, you can:

        * Sort the list either by <Glossary>carrier</Glossary> or <Glossary>shipping account</Glossary>
        * Change the <Glossary>shipping location</Glossary> by selecting the **Change Location** button

        <br />

        <Image align="center" border={true} src="https://files.readme.io/41603935fe204b0f21f146742408bd60584a5659ebb2a31c9302a475d93d24cf-sorting_and_changing_location.png" alt="Specifying filters" />
      </ToggleListItem>

      <br />

      <ToggleListItem title={<strong>3. Apply additional filters </strong>} icon="fa-rocket">
        <br />

        In the **Manifesting** page that opens, you can sort the list either of the following ways:

        * *By status*: Filter by shipment status
        * *By service*: Filter by carrier service codes

        <br />

        <Image align="center" border={true} src="https://files.readme.io/41603935fe204b0f21f146742408bd60584a5659ebb2a31c9302a475d93d24cf-sorting_and_changing_location.png" alt="Specifying filters" />

        ***
      </ToggleListItem>

      <br />

      <ToggleListItem title={<strong>4. Initiate manifesting </strong>} icon="fa-rocket">
        <br />

        Next to your desired shipment, select the manifest button: ![Manifest button](https://files.readme.io/fcb77ce4360ada3f172a0dccfceec28b483d6f4aa3e2a6a467929cf803686efe-Manifest_button.png)

                <Image align="center" border={true} src="https://files.readme.io/417b398230fd2d49d159b9cc0cffa33e38496a2e5649b8fe2ec36d0a3078ce4a-Manifest_option.png" alt="Manifesting shipment" />).

        ***
      </ToggleListItem>

      <br />

      <ToggleListItem title={<strong>5. Confirm the manifest</strong>} icon="fa-rocket">
        <br />

        Review the confirmation dialog carefully and select **Yes** if everything is correct.

        <Image align="center" border={true} src="https://files.readme.io/2b517ebeb7b8975acf72b7691c2d98aa3fd26d639e5ae366fdb98d5c5ae9d80e-Confirming_manifest.png" width="350px" />

        ***
      </ToggleListItem>

      <br />

      <ToggleListItem title={<strong>6. Monitor progress</strong>} icon="fa-rocket">
        <br />

        After confirming, you are directed to the **Manifest Processing Page** to track your manifest progress.

        <Image align="center" border={true} src="https://files.readme.io/94ad18f86e7c082888deddcd6fd000efdf60439d19d1779d552b579fe3f219d1-Manifest_processing_page.png" alt="Processing manifest" />

        <br />

        ***
      </ToggleListItem>

      <br />

      <ToggleListItem title={<strong>7. View manifest details</strong>} icon="fa-rocket">
        <br />

        Once processing is complete, expand the **Manifest/s processed** section using the view button: ![View manifests button](https://files.readme.io/b912251130f1a55af9a87de2cd47d96fa27576b740d7f5e4c4100d08470606d9-View_manifests_button.png)

        <Image align="center" border={true} src="https://files.readme.io/a160eccb1432a48bba9e1295800375eb7307516e9c2fbcbb7d5f386f98648443-Manifest_details.png" alt="Viewing manifest details" />

        <br />

        You have now successfully manifested your shipments.

        <Callout icon="💡" theme="default">
          ### **Tip**

          *If needed, you can export your manifest file by selecting the**Download as PDF** icon ![PDF icon](https://files.readme.io/e12fc39d80fd5eb7931db6e1db22df354422aa16bbc2c675f70c85c4a788431c-PDF_icon.png) in the **Manifest Number** column.*

          <Image align="center" border={true} src="https://files.readme.io/bc5120461fe99089d00c1c83f39a4e5e0706b8a62d25f2c39b697cb4377bf6b4-Accessing_held_shipmehts.png" alt="Accessing canceled shipments" />
        </Callout>
      </ToggleListItem>
    </ToggleList>
  </Tab>

  <Tab title="Manifest via API">
    

    To manifest shipments via our API, refer to the following endpoint

    <Cards>
      <Card title="Manifest Shipments" href="https://docs.intersoftsapient.net/docs/manifesting-shipments" icon="fa-solid fa-code">
        Complete API reference for manifesting shipments via our API
      </Card>
    </Cards>

    ### API recipe guide
  
    <Recipe slug="release-and-manifest-held-shipments" title="Manifest picked shipments" />

  </Tab>
</Tabs>

<br />
