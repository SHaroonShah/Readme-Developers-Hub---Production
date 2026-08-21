---
title: FedEx
excerpt: >-
  FedEx is a global leader in logistics and delivery services, renowned for its
  reliable express shipping and comprehensive transportation solutions. It
  offers a range of shipping options tailored for various international markets,
  making it an essential partner for businesses seeking to optimise their
  shipping operations.
deprecated: false
hidden: false
icon: fad fa-truck-fast
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---

<Image src="https://files.readme.io/094a6ea764d7d28798166aaaafe13e3fbe491279d79b1fd691766a419eb13352-FedEx_white_banner.png" align="center" width="900px" />


***

The FedEx-SAPIENT integration aims to enhance operational efficiency and provide users with tailored shipping options. By leveraging FedEx's extensive capabilities, businesses can ensure a streamlined shipping process that meets diverse logistical needs. This integration represents a significant step towards optimising shipping functions within SAPIENT.

## Overview

<Tabs>
  <Tab title="Key Features">
    <Cards columns="2">
      <Card title="Shipping Origins" icon="fa-map-marker-alt">
        The integration supports shipping from locations in Great Britain (GB) and Europe.
      </Card>

      <Card title="Shipping Destinations" icon="fa-solid fa-globe">
        Users can send <Glossary>shipments</Glossary> to Great Britain (GB), Europe, and Rest of the World (<Glossary>ROW</Glossary>).
      </Card>

      <Card title="Service Type" icon="fa-solid fa-shipping-fast">
        The integration is focused on outbound shipping only.
      </Card>

      <Card title="Incoterms Support" icon="fa-solid fa-file-contract">
        The integration supports <Glossary>DDU</Glossary>, <Glossary>DDP</Glossary>, and <Glossary>DAP</Glossary>.
      </Card>
    </Cards>
  </Tab>

  <Tab title="Additional Features">
    <Cards>
      <Card title="Multipiece Shipments" icon="fa-solid fa-boxes-stacked">
        Support for multipiece shipments is included in the integration.
      </Card>

      <Card title="Package Types" icon="fa-solid fa-box">
        FedEx offers its own distinct <Glossary>package type</Glossary>s.

        > _For more information on the carrier package types, use the<Anchor target="_blank" href="https://docs.intersoftsapient.net/reference/get_v4-carriers-carriercode-services-servicecode-packagetypes#/">Get Carrier Service Package Types</Anchor> endpoint._
      </Card>

      <Card title="Electronic Trade Document (ETD)" icon="fa-solid fa-file-invoice">
        Supports electronic trade documents, such as <Glossary>commercial invoice</Glossary>, <Glossary>proforma invoice</Glossary>, and in some cases, other specific documents, while configuring the FedEx <Glossary>shipping account</Glossary>. This solution allows you to create and send your trade documents electronically when shipping internationally.
      </Card>
    </Cards>

    <Callout icon="📘" theme="default">
      ### _Note_

      _For more information on Electronic Trade Document configuration, refer to the<Anchor target="_blank" href="https://docs.intersoftsapient.net/docs/add-fedex-shipping-account">Add FedEx shipping account</Anchor> section._
    </Callout>
  </Tab>

  <Tab title="Service Enhancements">
    The following are the key service enhancements provided by the FedEx integration:

    - **Saturday Delivery**: Enables package delivery on Saturdays for added convenience.
    - **Declared Values**: Applies a surcharge if the requested declared value of the shipment exceeds the liability stated in FedEx's terms and conditions for the selected service. The _declared value_ of a package represents the maximum liability in connection with the shipment of the package, including, but not limited to, any loss, damage, delay, or missed delivery relating to that shipment. As the shipper, it’s your responsibility to prove any actual damages. Exposure to and risk of any loss in excess of your declared value is assumed by you.
    - **Adult Signature**: Obtains a signature from any person of legal age at the delivery address, subject to the provision of a valid ID. If no one qualified to sign is available, an attempt will be made to redeliver the package on another date. Legal age varies depending on the destination country/territory and is governed by local legal age of an adult, not the legal age to purchase specific products.
    - **Direct Signature**: Obtains a signature from someone at the delivery address only. If no one is available to sign, a redelivery attempt of the package will be made on another date.
    - **Indirect Signature**: Obtains a signature from someone at the delivery address, from a neighbour, or from a building manager. If no one is available to sign, the package will be delivered on another date.
    - **No Signature Required**: Allows delivery without obtaining a signature if no one is available to sign. The package will be kept in a safe place.
    - **Email Notifications**: Sends notifications on delivery, estimated delivery, exceptions, shipment status, and tender.

    <Callout icon="💡" theme="default">
      ### _Tip_

      _For more information on the service enhancements and carrier services, refer to the API References section._
    </Callout>
  </Tab>

  <Tab title="Carrier Services">
    The following key services are provided by the FedEx integration.

    | Service Name                              | Description                                                                                                                                                                                         |
    | :---------------------------------------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
    | **FedEx® Economy**                        | This service provides cost-effective delivery for non-urgent shipments, typically delivered within a few working days with full tracking and reliable transit times.                                |
    | **FedEx® First**                          | This service provides early-morning, next-working-day delivery for urgent shipments, ensuring arrival at the start of the business day with time-definite delivery.                                 |
    | **FedEx® International Connect Plus**     | This service provides fast, cost-effective international e-commerce delivery with day-definite transit times, customs clearance, full tracking, and delivery management across global destinations. |
    | **FedEx International Economy®**          | This service provides cost-effective international delivery for less urgent shipments, typically completed within 2–5 business days with full tracking and customs clearance.                       |
    | **FedEx International First®**            | This service provides early-morning international delivery to selected destinations, offering time-definite delivery as early as 8:00–10:00 AM for urgent shipments.                                |
    | **FedEx International Priority®**         | This service provides fast international delivery within 1–3 business days, offering reliable, end-of-day delivery with tracking and customs-cleared processing.                                    |
    | **FedEx International Priority® Express** | This service provides expedited international delivery with time-definite arrival, typically by mid-morning or noon within 1–3 business days, including tracking and customs clearance.             |
    | **FedEx® Priority Express**               | This service provides time-definite, next-working-day delivery for urgent shipments, ensuring early delivery with full tracking and high-priority handling across the network.                      |
    | **FedEx® Priority**                       | This service provides fast, reliable delivery for time-sensitive shipments with delivery typically within 1–5 working days, including tracking and priority handling.                               |
    | **FedEx® Regional Economy**               | This service provides cost-effective, day-definite delivery within regions such as Europe, using road transport for less time-sensitive shipments with full tracking and customs support.           |

    <Callout icon="💡" theme="default">
      ### _Tip_

      _For the most up-to-date carrier services, use the [Get Carrier Services](https://docs.intersoftsapient.net/reference/get_v4-carriers-carriercode-services) endpoint._
    </Callout>
  </Tab>
</Tabs>

***

## API Services

<Tabs>
  <Tab title="Core Services">
    <Accordion title="Create Shipment">
      The integration for creating shipments to reflect FedEx as a primary carrier and allowing users to create shipments using the Create Shipment endpoint.
    </Accordion>

    <Accordion title="Manifest Shipment">
      Enables customers to retrieve information about shipment manifests created by the system and track when shipments have been successfully manifested with the carrier. For customers who need real‑time updates, we strongly recommend using the INTERSOFT [Manifest Webhook](https://docs.intersoftsapient.net/v4.04/docs/manifest-webhook), which provides updates on manifest requests, allowing you to track the progress and status of shipments prepared for carrier collection and delivery.
    </Accordion>

    <Accordion title="Cancel Shipment">
      The integration to cancel any unwanted shipments, to ensures that cancellations are fully registered with FedEx, helping prevent customers from being mistakenly charged for cancelled shipments.
    </Accordion>

    <Callout icon="🚧" theme="warning">
      ### _Important_

      _FedEx will not charge customers for transportation costs. However, customs clearance fees may still apply if a package is not cancelled and scanned by FedEx._
    </Callout>
  </Tab>

  <Tab title="Other Services">
    <Accordion title="Print Label">
      Generate and return the label for a DHL Germany shipment in the supported label formats. This endpoint must be utilised when the label is not generated in the DHL Germany Create Shipment request.

      <Callout icon="📘" theme="info">
        ### _Note_

        _This endpoint changes the status of the shipment to label printed. This endpoint should be called at the time of actual printing or label creation, depending on how your business operates. Shipments must be updated to label printed status prior to manifesting._
      </Callout>
    </Accordion>

    <Accordion title="Tracking">
      Enables customers to receive tracking updates through their integration with the SAPIENT tracking webhook.
    </Accordion>
  </Tab>
</Tabs>

***

## Getting Started

<Tabs>
  <Tab title="Account Setup">
    <Cards>
      <Card title="Add FedEx Shipping Account" href="https://docs.intersoftsapient.net/docs/add-fedex-shipping-account" icon="fa-solid fa-truck" target="_blank">
        Set up your FedEx shipping account to start creating shipments.
      </Card>

      <Card title="Add FedEx Tracking Account" href="https://docs.intersoftsapient.net/docs/add-fedex-tracking-account" icon="fa-solid fa-search-location" target="_blank">
        Configure tracking for your FedEx shipments.
      </Card>
    </Cards>
  </Tab>

  <Tab title="API References">
    <Cards columns="2">
      <Card title="SAPIENT FedEx API" href="https://docs.intersoftsapient.net/reference/get_v4-shippingaccounts-fedex" icon="fa-solid fa-code" target="_blank">
        Explore the FedEx API endpoints.
      </Card>
    </Cards>
  </Tab>
</Tabs>

<Banner isInline={true} message="Ready to integrate?" color="#ffb600" textColor="#ffffff" fontSize="20px" fontWeight="bold" width="120px" />

<Cards>
  <Card title="Activate this integration" href="https://docs.intersoftsapient.net/docs/integration-activation#/" icon="fa-solid fa-circle-play fa-beat" target="_blank">
    Connect with FedEx and manage your shipping operations from a single platform.
  </Card>
</Cards>
