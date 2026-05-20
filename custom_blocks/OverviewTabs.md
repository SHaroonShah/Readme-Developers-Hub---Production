---
name: OverviewTabs
---
<Tabs>
  <Tab title="Key Features">
    <Cards columns={2}>
      <Card title="Shipping Origins" icon="fa-map-marker-alt">
        ThThe integration supports shipping from locations in Great Britain (GB) only.
      </Card>

      <Card title="Shipping Destinations" icon="fa-solid fa-globe">
        Users can send shipments to Great Britain (GB), Europe, and the Rest of the World (<Glossary>ROW</Glossary>).
      </Card>

      <Card title="Service Type" icon="fa-solid fa-shipping-fast">
        The integration is focused on outbound shipping.
      </Card>

      <Card title="Incoterms Support" icon="fa-solid fa-file-contract">
        The integration supports <Glossary>DAP</Glossary> and <Glossary>DDP</Glossary> incoterms.
      </Card>

      <Card title="Label Formats" icon="fa-solid fa-tag">
        The integration supports labels in the <Glossary>PDF</Glossary> format.
      </Card>
    </Cards>

    <br />
  </Tab>

  <Tab title="Additional Features">
    * **Consignment services**: Consignment services are supported, and DPD UK allows a maximum of 99 packages per consignment.

    > 📘 *Note*
    >
    > *Please bear in mind that not all services offer consignment options.*

    * **Carrier-Specific Fields**: The **CarrierSpecifics** object in the **Create Shipment** request contains the following field:

      * **DeliveryInstructions**: To provide any additional instructions to the carrier regarding the delivery of the shipment
  </Tab>

  <Tab title="Service Enhancements">
    <Cards columns={2}>
      <Card title="Proof of Identity" icon="fa-solid fa-id-card">
        Requires the receiver to present valid identification at the point of delivery.
      </Card>

      <Card title="Proof of Age" icon="fa-solid fa-calendar-circle-user">
        Ensures the recipient meets a minimum age requirement, like for age-restricted goods.
      </Card>

      <Card title="Pin Required" icon="fa-solid fa-location-pin-lock">
        A secure PIN is sent to the receiver, which must be provided upon delivery.
      </Card>

      <Card title="Pin Required & Proof of Age" icon="fa-solid fa-location-pin-lock">
        Requires PIN and age verification at the point of delivery for added security.
      </Card>
    </Cards>

    <br />

    <Callout icon="💡" theme="default">
      ### *Tip*

      *For more information on the service enhancements and carrier services, refer to the following endpoints:*

      * *[Create Shipment](https://docs.intersoftsapient.net/reference/post_v4-shipments-dpduk)*
      * *[Get Carrier Services](https://docs.intersoftsapient.net/reference/get_v4-carriers-carriercode-services)*
    </Callout>
  </Tab>
</Tabs>
