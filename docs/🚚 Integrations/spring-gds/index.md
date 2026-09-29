---
title: Spring GDS
excerpt: >-
  Spring Global Delivery Solutions (GDS) is a carrier aggregator providing
  international mail and parcel services through a network of final mile
  delivery partners.
deprecated: false
hidden: false
icon: fad fa-truck-fast
link:
  new_tab: false
metadata:
  robots: index
---
Spring GDS supports outbound international shipments from Great Britain and the European Union, with services determined by your enabled shipping account and carrier service matrix.

<Tabs>
  <Tab title="Key Features">
    <Cards>
      <Card title="Shipping Origins" icon="fa-map-marker-alt">
        The integration supports shipping from Great Britain (GB) and the European Union (EU).
      </Card>

      <Card title="Shipping Destinations" icon="fa-solid fa-globe">
        You can send shipments to Great Britain (GB), Europe (EU), and the Rest of the World (ROW).
      </Card>

      <Card title="Service Type" icon="fa-solid fa-shipping-fast">
        The integration supports outbound shipping only.
      </Card>

      <Card title="Incoterms Support" icon="fa-solid fa-file-contract">
        The integration supports Delivered Duty Unpaid (DDU) and Delivered Duty Paid (DDP) incoterms.
      </Card>

      <Card title="Label Formats" icon="fa-solid fa-tag">
        The integration supports labels in PDF, PNG, and ZPL at 200 or 300 dots per inch (dpi).
      </Card>
    </Cards>

    <Callout icon="📘" theme="info">
      ### _Note_

      _Shipping destinations are determined by the services enabled on your shipping account and the carrier service matrix._
    </Callout>
  </Tab>

  <Tab title="Additional Features">
    <Cards>
      <Card title="Single-package Services" icon="fa-solid fa-box">
        Spring GDS supports single-package services only. Consignment services are not supported.
      </Card>

      <Card title="Carrier-specific Fields" icon="fa-solid fa-sliders">
        You can provide optional carrier-specific fields in the Carrier Specifics block of the Create Shipment request.
      </Card>
    </Cards>

    <Callout icon="🚧" theme="warn">
      ### _Important_

      _Before you use the carrier-specific fields, be aware of the following:_

      - _Carrier-specific fields apply only to Spring Clear. They default to `false` when omitted and do not cause shipment-validation failures._
      - _You cannot configure Spring Clear at shipping-account level or through a SAPIENT user interface setting. Its availability depends on your agreement and setup with Spring GDS._
      - _When Spring Clear is configured, set the incoterm to DDP in the Create Shipment request to trigger it._
      - _Use `PreferentialOriginTag` to indicate goods that qualify for reduced or zero-duty rates under an applicable international trade agreement. You are responsible for determining eligibility and meeting compliance obligations._
      - _Use `BondedGoods` to indicate goods that remain under customs supervision because customs duties have not yet been paid._
    </Callout>
  </Tab>

  <Tab title="Service Enhancements">
    <Callout icon="📘" theme="info">
      ### _Note_

      _There are no service enhancements for this integration._
    </Callout>
  </Tab>

  <Tab title="Carrier Services">
    The following key services are provided by the Spring GDS integration.

    | Service name | Description |
    | :--- | :--- |
    | **Create shipment** | Creates a shipment with Spring GDS as the primary carrier and returns the label in Base64-encoded format. |
    | **Tracking** | Provides tracking updates through the SAPIENT tracking webhook. |
    | **Manifest shipment** | Retrieves information about manifests created by the system and confirms when shipments have been manifested with the carrier. |

    <Callout icon="💡" theme="default">
      ### _Tip_

      _For the most up-to-date carrier services, use the&#x20;_[Get Carrier Services](https://docs.intersoftsapient.net/reference/get_v4-carriers-carriercode-services)_&#x20;endpoint._
    </Callout>
  </Tab>
</Tabs>

***

## API services

<Tabs>
  <Tab title="Core Services">
    <Accordion title="Create Shipment">
      Create a shipment with Spring GDS as the primary carrier. The Create Shipment service returns the shipment label in Base64-encoded format.
    </Accordion>

    <Accordion title="Tracking">
      Receive tracking updates for Spring GDS shipments through your SAPIENT tracking webhook integration.
    </Accordion>

    <Accordion title="Manifest shipment">
      Retrieve information about shipment manifests created by the system and check when shipments have been successfully manifested with Spring GDS. For real-time updates, use the [Manifest Webhook](https://docs.intersoftsapient.net/v4.04/docs/manifest-webhook) to monitor manifest requests and the status of shipments prepared for carrier collection and delivery.
    </Accordion>
  </Tab>
</Tabs>

***

## Getting Started

<Tabs>
  <Tab title="Account Setup">
    <Cards>
      <Card title="Add Spring GDS Shipping Account" href="https://docs.intersoftsapient.net/docs/add-spring-gds-shipping-account" icon="fa-solid fa-truck" target="_blank">
        Set up your Spring GDS shipping account before creating shipments.
      </Card>
    </Cards>
  </Tab>

  <Tab title="API References">
    <Cards>
      <Card title="Get Carrier Services" href="https://docs.intersoftsapient.net/reference/get_v4-carriers-carriercode-services" icon="fa-solid fa-code" target="_blank">
        Retrieve the services available for a carrier.
      </Card>
    </Cards>
  </Tab>
</Tabs>