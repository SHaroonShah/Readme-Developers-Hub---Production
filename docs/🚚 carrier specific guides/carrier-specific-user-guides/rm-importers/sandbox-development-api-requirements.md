---
title: API development requirements for Sandbox
excerpt: >-
  The development of some basic API calls is a process of creating and testing
  essential API functions that are fundamental to the operation of a software
  application. These initial API calls are typically recommended to handle core
  functionalities that the software can rely on once it is fully operational.
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
Intersoft API is a fully RESTful service implemented using JSON messaging. You, as the customer are responsible for sending JSON messages and for maintaining the capability of receiving JSON messages in the format described in this section.

Prior to going live on SAPIENT, first provide a <<glossary:bearer token>> and make sure, as a minimum, to have the following API calls developed:

- [Create Shipment](https://docs.intersoftsapient.net/reference/post_v4-shipments-rm): to generate the delivery <<glossary:labels>> for your packages.
- [Update Status](https://docs.intersoftsapient.net/reference/put_v4-shipments-status): to cancel/void a current shipping label. This can only be used before a <<glossary:shipment>> has been confirmed by being manifested.
- International Arrivals Containers (A-scan) API calls - **relevant to Freight 2 Post customers only.  It is mandatory to use by Freight 2 Post customers.**  
  API calls related to this are: 
  - [Add Container ](https://docs.intersoftsapient.net/reference/post_v4-internationalarrivalscontainers-rm): to create and name (with and ID or alias) a new international arrivals container to be used for manifesting a specific group of shipments. 
  - [Get Containers](https://docs.intersoftsapient.net/reference/get_v4-internationalarrivalscontainers-rm): to get a list of all international arrivals containers set up on the system.
  - [Update Container](https://docs.intersoftsapient.net/reference/put_v4-internationalarrivalscontainers-rm-update-containerid): to update details of the International Arrivals container.
  - [Add / Remove Shipments](https://docs.intersoftsapient.net/reference/put_v4-internationalarrivalscontainers-rm-containerid): to allocate shipments to a container or remove them from it before the container will be manifested.
  - [Delete Container](https://docs.intersoftsapient.net/reference/delete_v4-internationalarrivalscontainers-rm-containerid): to delete a specific container.
  - [Get Container ](https://docs.intersoftsapient.net/reference/get_v4-internationalarrivalscontainers-rm-containerid): to get details for a specific container.
- [Manifest Shipments](https://docs.intersoftsapient.net/reference/post_v4-manifests-carriercode): to closeout shipments, which produces the collection <<glossary:manifest>> to be handed over to the driver and triggers electronic <<glossary:pre-advice>> and billing data to be sent to the <<glossary:carrier>>. This must be done before your <<glossary:shipment>> enter Royal Mail network.  Not doing it may result in multiple issues such as delays, missing tracking, lack of notifications for your end consumers, surcharges, and others.

> 📘 _Note_
> 
> _At INTERSOFT, we have developed a dedicated API endpoint for servers based in China.  To access this domain, kindly change your domain from **.net** to **.cn** for all the relevant endpoints you will be using._ 
> 
> _For example, when creating a new shipment replace the <https://api.intersoftsapient.net/v4/shipments/rm> URL with [https://api.intersoftsapient.cn/v4/shipments/rm](https://api.intersoftsapient.net/v4/shipments/rm). _
> 
> _As a back-up, please develop **.net** as well._

## See also

- [Authentication](https://docs.intersoftsapient.net/docs/authentication)