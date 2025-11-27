---
title: Cancel shipment
excerpt: >-
  A shipment can be set to *Cancelled* when it has been officially stopped and
  is not going to be delivered. Cancellations may occur for various reasons,
  including customer requests or logistical issues.
deprecated: false
hidden: false
icon: fad fa-nfc-slash
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
In SAPIENT, you can cancel the <Glossary>shipments</Glossary> to ensure that resources can be reallocated and allow users to manage customer expectations. The shipment can be canceled if it has been confirmed by being manifested.

<Cards columns="2">
  <Card title="UI Cancellation" icon="mouse-pointer">
    Cancel shipments directly through the SAPIENT interface with step-by-step guidance
  </Card>

  <Card title="API Cancellation" icon="code">
    cancel shipments using our REST API endpoint
  </Card>
</Cards>

## How to cancel shipments

<Tabs>
  <Tab title="Via SAPIENT UI">
    Follow these steps to cancel shipments through the SAPIENT UI:

    <ToggleList>
      <ToggleListItem title={<strong>1. Access the manifesting option</strong>} icon="fa-rocket">
        <br />

        In the side navigation panel, select **Shipment Processing** > **Manifesting**.

        <Image align="center" border={true} src="https://files.readme.io/43b41b65377780fd19531fd2378483c9b0c7d99c88b2c5242e584ef4225c5dae-Accessing_manifesting_option.png" alt="Accessing shipments" />

        ***
      </ToggleListItem>

      <br />

      <ToggleListItem title={<strong>2. Configure filters and sorting</strong>} icon="fa-rocket">
        <br />

        In the **Manifesting** page that opens, you can perform the following actions and filter the tabe data as per your needs:

        * Sort the list by <Glossary>carrier</Glossary> or <Glossary>shipping account</Glossary>
        * Change the <Glossary>shipping location</Glossary> by selecting **Change Location**

        <br />

        <Image align="center" border={true} src="https://files.readme.io/41603935fe204b0f21f146742408bd60584a5659ebb2a31c9302a475d93d24cf-sorting_and_changing_location.png" alt="Specifying filters" />
      </ToggleListItem>

      <br />

      <ToggleListItem title={<strong>3. Apply additional filters </strong>} icon="fa-rocket">
        <br />

        Filter the table data using:

        * **Narrow by Status**: Filter by shipment status
        * **Narrow by Service**: Filter by carrier service codes

        <br />

        <Image align="center" border={true} src="https://files.readme.io/4f3b0dfcf1502b52e1c71c7448e95814a0afee4d9d9b865ba27082f2acbde5ed-Narrowing_manifesting.png" alt="Viewing shipments" />

        ***
      </ToggleListItem>

      <br />

      <ToggleListItem title={<strong>4. Select and cancel shipments </strong>} icon="fa-rocket">
        <br />

        Next to the shipment you want to cancel, select ![alt text](https://files.readme.io/ade8694f40f0b89e1cfab543051a5b77f7a307552c22b1c0105f7f2439dd065e-View_button.png). On the page that opens, select the checkbox next to the shipment, and then click ![alt text](https://files.readme.io/ce57b2272ffff135c3c09d4b532c2cbff21b8ffeaaacb4bb668edcbd00c2e67c-Cancel_shipments_button.png).

        <br />

        <Image align="center" border={true} src="https://files.readme.io/1b5ebf0996d78e8b255de85c8da7e377d6f19524f9899bc8155d4b48f34ea0d0-Canceling_shipments.png" alt="Accessing option to cancel shipments" />

        ***
      </ToggleListItem>

      <br />

      <ToggleListItem title={<strong>5. Confirm cancellation</strong>} icon="fa-rocket">
        <br />

        In the confirmation dialog that opens, enter the reason for canceling the shipment and select **Yes** to confirm.

        <br />

        <Image align="center" border={true} src="https://files.readme.io/add229243a38970d994d96735c0f6ad74a1ca4404fa57475b6c9fc2a85b038ad-Confirming_shipment_cancellation.png" width="350px" alt="Confirming shipment cancellation" />
      </ToggleListItem>
    </ToggleList>

    <Callout icon="💡" theme="default">
      ### *Tip*

      *You can access the canceled shipments directly from this page by selecting the**View Cancelled Shipments** option or by accessing the **Shipment Processing** > **Cancelled** option from the side navigation panel.*

      <Image align="center" border={true} src="https://files.readme.io/98bb78638eb05e979777dfd34b1a13605cab5520fa6017f7a980a02fc38a0602-Canceled_shipments_option.png" alt="Accessing canceled shipments" />
    </Callout>
  </Tab>

  <Tab title="Via API">
    To cancel shipment via our API, refer to the following endpoint:

    <Cards>
      <Card title="Update Status" href="https://docs.intersoftsapient.net/reference/put_v4-shipments-status" icon="fa-solid fa-code">
        Complete API reference for shipment status updates including cancellation
      </Card>
    </Cards>

    ***

    ### API recipe guide

    To view a step-by-step process on how to cancel shipments via API, refer to the following API recipe:

    <Recipe />
  </Tab>
</Tabs>

<br />

<br />

<br />

<br />

<br />
