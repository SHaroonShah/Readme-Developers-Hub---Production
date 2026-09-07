---
name: KeyFeatures_Template
---
<Tabs>
  <Tab title="Key Features">
    <Cards>
      <Card title="Shipping Origins" icon="fa-map-marker-alt">
        The integration supports shipping from locations in Great Britain (GB) mainland only (England, Wales, and Scotlabd).
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

      <Card title="Incoterms Support">
        The integration only supports <Glossary>DDU</Glossary> incoterm.
      </Card>
    </Cards>
  </Tab>

  <Tab title="Additional Features">
    <Cards>
      <Card title="Labelled B2C" icon="fa-solid fa-tag">
        Generates and returns a label to be attached to the parcel for a B2C business transaction type deliveries.
      </Card>

      <Card title="Labelless Returns Using QR Codes" icon="fa-solid fa-qrcode">
        Generates a QR code for a return shipment which eliminates the need for printing shipping labels. This feature enhances the return process and makes it more environmentally friendly.
      </Card>
    </Cards>
  </Tab>

  <Tab title="Service Enhancements">
    <Callout icon="📘" theme="info">
      ### _Note_

      _There are no service enhancements for this integration._
    </Callout>
  </Tab>

  <Tab title="Carrier Services">
    The following key services are provided by the InPost integration.

    | Service Name          | Description                                                                                                                                                                                                                                                                    |
    | :-------------------- | :----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
    | **Labelled B2C**      | This service provides business-to-consumer parcel delivery using a printed shipping label, where the sender generates and attaches the label before drop-off at an InPost locker or shop.                                                                                      |
    | **Labelless Returns** | This service provides a label-free returns solution using a QR code, allowing customers to drop off parcels at the desired <Glossary>PUDO</Glossary> location, such as lockers or shops without printing labels, with tracking and labelling handled by InPost during transit. |

    <Callout icon="💡" theme="default">
      ### _Tip_

      _For the most up-to-date carrier services, use the&#x20;_[Get Carrier Services](https://docs.intersoftsapient.net/reference/get_v4-carriers-carriercode-services)_&#x20;endpoint._
    </Callout>
  </Tab>
</Tabs>
