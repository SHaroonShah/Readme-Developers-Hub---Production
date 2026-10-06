---
title: Royal Mail export validation updates
author: Syed Haroon Shah
hidden: false
published_at: '2026-10-06T09:34:04.502Z'
type: improved
---
To support Royal Mail customs requirements, shipments using commercial customs services can no longer be created when the **ReasonForExport&#x20;**&#x66;ield in the Create Shipment request is set to **Gift**.

<Callout icon="🚧" theme="warn">
  ### _Important_

  _If a shipment is submitted using the Royal Mail commercial customs service with Reason for Export as Gift, the shipment will fail validation and an error will be returned._

  > _For more information, refer to the Royal Mail&#x20;_<Anchor target="_blank" href="https://docs.intersoftsapient.net/reference/post_v4-shipments-rm">_Create Shipment_</Anchor>_&#x20;endpoint._
</Callout>