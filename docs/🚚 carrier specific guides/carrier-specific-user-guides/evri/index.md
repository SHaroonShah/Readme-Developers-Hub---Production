---
title: EVRi
excerpt: >-
  _EVRi_ is a logistics and parcel delivery service provider that operates
  primarily in the UK. EVRi offers a wide range of delivery options, including
  standard, next-day, and scheduled deliveries, catering to both business and
  residential customers.
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
      slug: shipping-account-setup-3
      title: Evri shipping account setup
---
<Image align="center" border={false} width="140px" src="https://files.readme.io/49cf864b835a4e2de7c4ebfd3cea85e552a3a27790c9dd755e39162cdb71c63e-image.png" />

***

The EVRi integration into the SAPIENT platform enhances our shipping capabilities by enabling users to seamlessly manage their shipments through Evri's robust delivery network. Customers can now access Evri's comprehensive suite of services, including real-time tracking, flexible delivery options, and efficient returns management, all within the familiar SAPIENT interface. This enhancement aims to streamline the shipping process, improve operational efficiency, and provide a better overall experience for our users.

## Key features

This integration provides the following key features:

**Ship from destinations**: The integration supports shipping from locations in Great Britain (GB) only.

* **Ship To Destinations**: Users can send <Glossary>shipments</Glossary> to Great Britain (GB), Europe, and the <Glossary>ROW</Glossary> (Rest of the World).
* **Label formats**: The EVRi's label integration support labels in the <Glossary>PDF</Glossary> and <Glossary>PNG</Glossary> formats.
* **Incoterms**: This integration only supports <Glossary>DDU</Glossary>.
* **Service Type**: The integration is focused on outbound and Returns shipping services.

> 📘 _Note_
>
> _QR code generation is supported for the returns shipments._

## Enhancements

The following are the key enhancements provided by the EVRi integration:

* Service enhancements: These services include the following:
  * **Signed**: Requires a signature upon delivery.
  * **SMS**: Requires a contact number to receive delivery updates via SMS.

## Additional features

The EVRi integration provides the following additional features:

* **Single package**: All services in this integration support only single-package services. Which means, only one package can be sent per request.

## Integration types

This integrations supports the following integration types on SAPIENT:

**Label**: Enables delivery routing request to be used for outbound services, and collection routing request for the returns services.

**Tracking**: Enables data files to be sent via SFTP.

***

In this section, learn how to:

* [Add an EVRi shipping account](https://docs.intersoftsapient.net/docs/shipping-account-setup-3)
* [Add an EVRi tracking account](https://docs.intersoftsapient.net/docs/tracking-account-setup)
* [Add a child client department to parent shipping account](https://docs.intersoftsapient.net/docs/client-id-and-child-clinet-id-management-1#/)

<br />
