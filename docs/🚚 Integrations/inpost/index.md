---
title: InPost
excerpt: >-
  InPost is a Polish public logistics limited company with courier, package
  delivery and express mail service. The company specialises in parcel locker
  service operated in Poland, Italy, United Kingdom, France, Benelux, Spain, and
  Portugal.
deprecated: false
hidden: false
icon: fad fa-truck-fast
metadata:
  robots: index
---

<Image src="https://files.readme.io/75762ee66dc10880c8cfd75e2d683174396ef3ed0fd727fd959f2eb44e013de6-InPost_white_banner.png" align="center" width="900px" />


***

InPost provides a convenient, eco-friendly parcel delivery service through a network of 24/7 automated lockers and partnered shops in the UK. You can drop off or pick up parcels at these locations anytime, offering flexibility and ease for both senders and recipients.

This integration offers several key features that streamline the shipping process. This article summarises the in-scope features of the integration and provides detailed explanations of the associated process flows.

<Tabs>
  <Tab title="Key Features">
    <Cards columns={2}>
      <Card title="Shipping Origins" icon="fa-map-marker-alt">
        ThThe integration supports shipping from locations in Great Britain (GB) mainland only (England, Wales, and Scotlabd).
      </Card>

      <Card title="Shipping Destinations" icon="fa-solid fa-globe">
        Users can send shipments to Great Britain (GB) mainland only.
      </Card>

      <Card title="Service Type" icon="fa-solid fa-shipping-fast">
        The integration is focused on outbound and inbound shipping.
      </Card>

      <Card title="Label Formats" icon="fa-solid fa-tag">
        The integration supports labels in the <Glossary>PDF</Glossary> format.
      </Card>
    </Cards>

    <br />
  </Tab>

  <Tab title="Additional Features">
    <Cards column={1}>
      <Card title="Labelled B2C" icon="fa-solid fa-tag">
        Generates and returns a label to be attached to the parcel for a B2C business transaction type deliveries.
      </Card>

      <Card title="Labelless Returns Using QR Codes" icon="fa-solid fa-qrcode">
        Generates a QR code for a return shipment which eliminates the need for printing shipping labels. This feature enhances the return process and makes it more environmentally friendly.
      </Card>
    </Cards>
  </Tab>

  <Tab title="Service Enhancements">
    > 📘 *Note*
    >
    > *There are no service enhancements for this integration.*
  </Tab>

  <Tab title="Carrier Services">
    The following key services are provided by the InPost integration.

    | Service Name          | Description                                                                                                                                                                                                                                                                    |
    | :-------------------- | :----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
    | **Labelled B2C**      | This service provides business-to-consumer parcel delivery using a printed shipping label, where the sender generates and attaches the label before drop-off at an InPost locker or shop.                                                                                      |
    | **Labelless Returns** | This service provides a label-free returns solution using a QR code, allowing customers to drop off parcels at the desired <Glossary>PUDO</Glossary> location, such as lockers or shops without printing labels, with tracking and labelling handled by InPost during transit. |

    <br />

    <Callout icon="💡" theme="default">
      ### *Tip*

      *For the most up-to-date carrier services, use the [Get Carrier Services](https://docs.intersoftsapient.net/reference/get_v4-carriers-carriercode-services) endpoint.*
    </Callout>
  </Tab>
</Tabs>

***

## API services

<Tabs>
  <Tab title="Core Services">
    <Accordion title="Create Shipment">
      The integration for creating shipments to reflect EVRi as a primary carrier and allowing users to create shipments using the **Create Shipment** endpoint.
    </Accordion>

    <br />

    <Accordion title="Manifest shipment">
      Enable customers to retrieve information about shipment manifests created by the system and track when shipments have been successfully manifested with the carrier. For customers who need real‑time updates, we strongly recommend using the INTERSOFT [Manifest Webhook](https://docs.intersoftsapient.net/docs/manifest-webhook) to keep track of shipments and their statuses by to receiving real-time updates or notifications whenever specific events occur in the system (such as shipping updates, status changes, and so on).

      > 📘 *Note*
      >
      > *If any created shipments have not been manifested, it is advised to cancel them to avoid unwanted labels.*
    </Accordion>

    <br />

    <Accordion title="Get PUDO locations">
      Enable customers to users to access essential shipping options for both sending and returning packages seamlessly via the [Get PUDO Locations endpoint](https://docs.intersoftsapient.net/reference/get_v4-pudolocations-carriercode-countrycode-postcode).
    </Accordion>
  </Tab>

  <Tab title="Other Services">
    <Accordion title="Print Label">
      Generate and return the label for an InPost shipment in the PDF format. This endpoint must be utilised when the label is not generated in the InPost Create Shipment request.

      > 📘 *Note*
      >
      > *This endpoint changes the status of the shipment to label printed. This endpoint should be called at the time of actual printing or label creation, depending on how your business operates. Shipments must be updated to label printed status prior to manifesting.*
    </Accordion>
    <br />
    <Accordion title="Tracking">
      This integration allows customers to monitor their shipments in real-time, providing transparency and peace of mind. Users can access detailed tracking information, including, real-time updates, tracking numbers, and delivery notifications.
    </Accordion>
  </Tab>
</Tabs>

***

## Getting Started

<Tabs>
  <Tab title="Account Setup">
    <Cards columns={3}>
      <Card title="Add InPost Shipping Account" icon="fa-solid fa-truck" href="https://docs.intersoftsapient.net/docs/add-inpost-shipping-account">
        Set up your InPost shipping account to start creating shipments.
      </Card>

      <Card title="Add InPost Tracking Account" icon="fa-solid fa-search-location" href="https://docs.intersoftsapient.net/docs/add-inpost-tracking-account">
        Configure tracking for your InPost shipments.
      </Card>

      <Card title="Use Inpost PUDO service" icon="fa-solid fa-search-location" href="https://docs.intersoftsapient.net/docs/pudo-integration">
        Utilise the SAPIENT Pick Up and Drop Off (PUDO) service to use a convenient out of home option to collect or return InPost parcels at designated locations.
      </Card>
    </Cards>
  </Tab>

  <Tab title="API References">
    <Cards columns={2}>
      <Card title="SAPIENT InPost API" icon="fa-solid fa-code" href="https://docs.intersoftsapient.net/reference/get_v4-shippingaccounts-inpost">
        Explore the InPost API endpoints for a seamless shipping experience.
      </Card>

      <Card title="Get PUDO Locations" icon="fa-solid fa-code" href="https://docs.intersoftsapient.net/reference/get_v4-shippingaccounts-inpost">
        Explore the SAPIENT's core PUDO Locations endpoint to reetrieve a list of Pick-Up and Drop-Off (PUDO) locations associated with InPost.
      </Card>
    </Cards>
  </Tab>

  <Tab title="Sign-Off">
    <Cards>
      <Card title="Inpost Sign-off Process" href="https://docs.intersoftsapient.net/docs/inpost-sign-off" icon="fa-solid fa-file-signature">
        Complete all the necessary steps before using InPost for creating shipments on SAPIENT.
      </Card>
    </Cards>
  </Tab>
</Tabs>

<Banner isInline={true} message="Ready to integrate?" color="#ffb600" textColor="#ffffff" fontSize="20px" fontWeight="bold" width="120px" />

<Cards columns={0}>
  <Card title="Activate this integration" href="https://docs.intersoftsapient.net/docs/integration-activation#/" icon="fa-solid fa-circle-play fa-beat" target="_blank">
    Seamlessly connect with InPost and manage your shipping operations from a single platform.
  </Card>
</Cards>

<br />
