---
title: YODEL
excerpt: >-
  _YODEL_ is a prominent logistics and parcel delivery service provider based in
  the UK., specialising in delivery parcels for ecommerce businesses and
  individual customers. YODEL offers a broad range of delivery options,
  including next-day delivery, standard service, and same-day delivery for
  certain locations.
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
  pages:
    - type: basic
      slug: shipping-account-setup-1
      title: Yodel shipping account setup
---
<Image align="center" width="120px" src="https://files.readme.io/6bb2b97788b8ae71adbb45e1d2c1d8095e6ea532a364aafbf784365c823c24ba-image.png" />

***

YODEL, is fully integrated into the Intersoft SAPIENT platform. This integration allows businesses to seamlessly access YODEL’s delivery network through SAPIENT’s unified API, enabling the following key features:

* **Ship from destinations**: The integration supports shipping from locations in Great Britain (GB) only.
* **Ship To Destinations**: Users can send <Glossary>shipments</Glossary> to Great Britain (GB), Europe, and the <Glossary>ROW</Glossary> (Rest of the World).

> 📘 _**Note**_
>
> _Shipments to Northern Ireland (NI) and Channel Islands are treated as international._

* **Service Type**: The integration is focused on outbound shipping.
* **Label formats**: <Glossary>PDF</Glossary> and <Glossary>PNG</Glossary>.

## Additional features

The YODEL integration provides the following additional features:

* **Consignment services**: Supports consignment services. Maximum number of packages supported depends on the service. Some services allow multiple packages, and some do not ; the maximum number of packages is stored against the service.

> 📘 _Note_
>
> _Multi-package requests are not supported for single-package services._

* **Incoterms**: The integration supports <Glossary>DDU</Glossary> (Delivered Duty Unpaid) incoterm only.

## Integration types

**Label**: This integration is In-house, which means that the label is generated within the SAPIENT system without calling the carrier API.

**Tracking**: Enables data files to be sent via SFTP.

In this section, learn how to do the following: 

* [Add a YODEL shipping account](https://docs.intersoftsapient.net/docs/shipping-account-setup-1)
* [Add a YODEL tracking account](https://docs.intersoftsapient.net/docs/tracking)
* Add a barcode range to YODEL shipping account
