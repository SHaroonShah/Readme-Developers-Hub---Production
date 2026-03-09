---
title: 2026 release notes
excerpt: This section includes the archived release notes published in the year 2026.
deprecated: false
hidden: true
icon: fad fa-notes
metadata:
  robots: index
---
<Accordion title="January release notes" icon="fa-solid fa-document">
  ## DPD UK integration 
The DPD UK integration has been added to the SAPIENT system. This integration expands our shipping options, allowing our customers to utilise DPD UK for their shipping needs, improving overall service flexibility and efficiency.

With this addition, the following information has been added to the swagger documentation:

* **New API endpoints**. A new DPD UK block has been added to our carrier-specific APIs. This block includes the following API endpoints:
  * **Shipping Account**
    * **Get Accounts**: Retrieve a list of DPD UK shipping accounts.
    * **Add Account**: Add a new DPD UK shipping account.
    * **Get Account**: Retrieve details of a specific DPD UK shipping account.
    * **Update Account**: Update details of an existing DPD UK shipping account.
    * **Link Locations**: Link shipping locations to the DPD UK shipping accounts.
    * **Get Associated Locations**: Retrieve locations linked to the DPD UK shipping account.
    * **Get Associated Location**: Fetch details for a specific associated location.
  * **Shipments**
    * **Create Shipment**: Create a new DPD UK shipment request.
    * **Print Label**: Generate a label for the DPD UK shipment. This is only valid if the shipment is created with the action other than **Process**.

> 📘 _Note_
>
> _The [Get Carrier](https://docs.intersoftsapient.net/reference/get_v4-carriers-carriercode) and [Get Carrier Services](https://docs.intersoftsapient.net/reference/get_v4-carriers-carriercode-services) endpoints in our **SAPIENT CORE API** block can also be utilised to look for the carrier and its available services._

<br />
</Accordion>

<br />