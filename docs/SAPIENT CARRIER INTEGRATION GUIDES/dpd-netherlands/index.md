---
title: DPD Netherlands (NL)
excerpt: >-
  DPD Netherlands (NL) is the branch of DPD operating in the Netherlands and is
  part of Geopost group.
deprecated: false
hidden: false
icon: fad fa-truck-fast
metadata:
  robots: index
---
<Image align="center" width="900px" src="https://files.readme.io/67505883534542d666a2fed1d64893c848534290da3ac931e7c09fce390c7fa5-DPD_NL_banner_white.png" />

***

<br />

DPD NL ship domestically and internationally, and approximately 60% of their outbound volume is cross-border.

The integration of DPD NL into the SAPIENT platform is a significant step in enhancing shipping capabilities. This section discusses the in-scope features of this integration and the services this carrier offers

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
    <Cards columns={2}>
      <Card title="Consignment services" icon="fa-solid fa-boxes-stacked">
        Consignment services are supported, and DPD UK allows a maximum of 99 packages per consignment.

        > *Please bear in mind that not all services offer consignment options.*
      </Card>

      <Card title="Carrier-Specific Fields" icon="fa-solid fa-list-check">
        The **CarrierSpecifics** object in the **Create Shipment** request includes **DeliveryInstructions** for providing additional delivery instructions to the carrier.
      </Card>
    </Cards>
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

***

## API Services

The following API services are provided by the DPD NL integration:

* **Create shipment**: The integration for creating shipments to reflect DPD NL as a primary carrier and allowing users to create shipments using the Create Shipment that returns the label in base64 encoded format.
* **Manifest webhook**: Keep track of shipments and their statuses by to receiving real-time updates or notifications whenever specific events occur in the system (such as shipping updates, status changes, and so on) via the SAPIENT Manifest Webhook feature.
* **Tracking**: Enables data files to be sent via SFTP and received through the SAPIENT tracking webhook.

<br />
