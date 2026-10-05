---
title: DTP shipment validation
author: Syed Haroon Shah
hidden: true
published_at: '2026-10-05T14:18:45.322Z'
---
A new <Glossary>DTP</Glossary>-specific validation has been added for Royal Mail international export shipments. This enhancement enables DTP shipments to be validated against dedicated rules, helping ensure the correct services, destinations, and shipment information are used. This change improves validation accuracy and supports Royal Mail's evolving requirements for commercial export services.

The DTP value can be specified in the **Create Shipment** > **CarrierSpecifics** > **TermsOfDelivery** field.

<Callout icon="🚧" theme="warn">
  ### _Important_

  _Populate the&#x20;_**_TermsOfDelivery_**_&#x20;field to&#x20;_**_DTP_**_&#x20;only when the&#x20;_**_Incoterms_**_&#x20;field is set to&#x20;_<Glossary>DDP</Glossary>_. For more information, refer to the Royal Mail&#x20;_[_Create Shipment_](https://docs.proshipping.net/reference/post_v4-shipments-rm)_&#x20;endpoint._
</Callout>