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

Prior to going live on SAPIENT, first provide a <Glossary>bearer token</Glossary> and make sure, as a minimum, to have the following API calls developed:

* [Create Shipment](https://docs.intersoftsapient.net/reference/post_v4-shipments-rm): to generate the delivery <Glossary>labels</Glossary> for your packages.
* [Update Status to Cancel](https://docs.intersoftsapient.net/reference/put_v4-shipments-status): to cancel/void a current shipping label. This can only be used before a <Glossary>shipment</Glossary> has been confirmed by being manifested.
* International Arrivals Containers (A-scan) API calls - **relevant to Freight 2 Post customers only.  It is mandatory to use by Freight 2 Post customers.**\
  API calls related to this are:
  * [Add Container ](https://docs.intersoftsapient.net/reference/post_v4-internationalarrivalscontainers-rm): to create and name (with an ID or alias) a new International Arrivals Container to be used for manifesting a specific group of shipments.
  * [Get Containers](https://docs.intersoftsapient.net/reference/get_v4-internationalarrivalscontainers-rm): to get a list of all International Arrivals Containers set up on the system.
  * [Update Container](https://docs.intersoftsapient.net/reference/put_v4-internationalarrivalscontainers-rm-update-containerid): to update details of the International Arrivals Container.
  * [Add / Remove Shipments](https://docs.intersoftsapient.net/reference/put_v4-internationalarrivalscontainers-rm-containerid): to allocate shipments to a container or remove them from it before the container will be manifested.
  * [Delete Container](https://docs.intersoftsapient.net/reference/delete_v4-internationalarrivalscontainers-rm-containerid): to delete a specific container.
  * [Get Container ](https://docs.intersoftsapient.net/reference/get_v4-internationalarrivalscontainers-rm-containerid): to get details for a specific container.
* [Manifest Shipments](https://docs.intersoftsapient.net/reference/post_v4-manifests-carriercode): to closeout shipments, which produces the collection <Glossary>manifest</Glossary> (Royal Mail Sales Order Summary) to be handed over to the driver and triggers electronic <Glossary>pre-advice</Glossary> and billing data to be sent to the <Glossary>carrier</Glossary>. This must be done before your <Glossary>shipment</Glossary> enters Royal Mail network.  Not doing it may result in multiple issues such as delays, missing tracking, lack of notifications for your end consumers, surcharges, and others.

> 📘 *Note*
>
> *At INTERSOFT, we have developed a dedicated API endpoint for servers based in China.  To access this, kindly change your domain from***.net** to **.cn** for all the relevant endpoints you will be using.
>
> *For example, when creating a new shipment replace the[https://api.intersoftsapient.net/v4/shipments/rm](https://api.intersoftsapient.net/v4/shipments/rm) URL with [https://api.intersoftsapient.cn/v4/shipments/rm](https://api.intersoftsapient.net/v4/shipments/rm).*
>
> *As a back-up, please develop\*\* .net\*\* as well.*

## See also

* [Authentication](https://docs.intersoftsapient.net/docs/authentication)