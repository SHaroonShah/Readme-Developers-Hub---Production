---
title: Release shipment
excerpt: >-
  Releasing a shipment refers to the process of removing any restrictions or
  barriers that prevented it from being processed or shipped. It typically
  involves resolving any issues that cause the shipment hold, such as completing
  the required documentation, verifying payment, or addressing compliance
  concerns.
deprecated: false
hidden: false
icon: fad fa-right-long
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
Releasing a shipment from hold is crucial for maintaining operational efficiency, ensuring timey delivery, and upholding customer relationships.

In SAPIENT, you can anytime release the [held](https://docs.intersoftsapient.net/docs/held-shipments) <Glossary>shipments</Glossary>.

<Cards columns={2}>
  <Card title="UI Method" icon="fa-solid fa-desktop">
    Release held shipments directly through the SAPIENT user interface using the step-by-step process below.
  </Card>

  <Card title="API Method" icon="fa-solid fa-code">
    Use the SAPIENT API to programmatically release shipments. View the API references for detailed implementation.
  </Card>
</Cards>

## How to release shipment

<Tabs>
  <Tab title="Release via SAPIENT UI">
    <br />

    To release a shipment in SAPIENT, perform the steps as explained in the following procedure.

    <ToggleList>
      <ToggleListItem title={<strong>1. Access held shipments</strong>} icon="fa-rocket">
        <br />

        In the side navigation panel, select the **Shipment Processing** > **Held** option.

        <Image align="center" border={true} src="https://files.readme.io/c0796ec5b2d1123cc03bd22830f7520bddea1408599b62a0b00be63dff75e887-Held_option.png" alt="Accessing shipments" />

        ***
      </ToggleListItem>

      <br />

      <ToggleListItem title={<strong>2. Select shipments to release</strong>} icon="fa-rocket">
        <br />

        In the **Held Shipments** page that opens, select the checkboxes next to the shipments you want to release, and then select ![alt text](https://files.readme.io/ea4f0d57b9918ccc9192a3d230a9dbd24e3e5a33c864e0dd4e8c973181d78f46-Release_shipments_button.png).

        <Image align="center" border={true} src="https://files.readme.io/a64211ea7a7073f81971a21ff07e429fe56864cd50f4be911b9af62da763fe8d-Releasing_shipment.png" alt="Recalling shipment" />

        ***

        <br />
      </ToggleListItem>

      <br />

      <ToggleListItem title={<strong>3. Confirm your action </strong>} icon="fa-rocket">
        <br />

        In the confirmation dialog that appears, select **Yes**.

        <Image align="center" border={true} src="https://files.readme.io/6357a15bc67e4c76c3e37aca5da2842b7bdb395cf3c3ce8fa6e6bd16bba7a751-Confirming_shipment_release.png" width="350px" alt="Confirming shipment recalling" />

        <br />

        Once confirmed, the shipment(s) is removed from the **Held Shipments** list and goes back to its previous status and is included in the next manifest.

        ***
      </ToggleListItem>
    </ToggleList>

    <Callout icon="💡" theme="default">
      ### *Tip*

      *If you want to export the label for the held shipments, then in the**Tracking Number** column select ![](https://files.readme.io/3df26abe526e632f50567b6ad821d178d4193a2d068a9f584e3e6a2b547b4417-Cloud_icon.png). Follow the prompts of your computer and download it.*
    </Callout>
  </Tab>

  <Tab title="Release via API">
    To release shipment via our API, refer to the following endpoint

    <Cards>
      <Card title="Update Status" href="https://docs.intersoftsapient.net/reference/put_v4-shipments-status" icon="fa-solid fa-code">
        Complete API reference for shipment status updates including releasing
      </Card>
    </Cards>

    <br />

    To view a step-by-step process on how to release held shipments and manifest them via API, refer to the following API recipe:

    <Recipe />
  </Tab>
</Tabs>
