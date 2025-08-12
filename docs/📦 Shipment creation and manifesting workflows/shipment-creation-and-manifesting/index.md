---
title: Shipment creation and manifesting
excerpt: >-
  Shipment creation and manifesting are key processes in logistics, particularly
  in the context of transporting goods. _Shipment creation_ refers to the
  process of preparing and documenting the details of a shipment before it is
  despatched to its destination, whereas _manifesting_ is the process of
  creating a detailed list (manifest) of all shipments being handed over to the
  carrier.
deprecated: false
hidden: false
icon: fad fa-cart-plus
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
The SAPIENT API has been designed to accommodate different methods of processing <Glossary>shipments</Glossary> , to fit in with the varied ways many businesses operate their despatching function. This section provides a high-level overview on the different methods available to manage when to print labels and how to manifest accurately at the end of each working day. 

> 📘 *Note*
>
> *For more detailed information, please contact the Intersoft Customer Operations team to arrange a consultation.*

## Use shipment actions in Create Shipment API

Shipment actions are specific operations that can be performed on a shipment during its lifecycle. These actions allow businesses to manage and control various aspects of the shipment process. The following are the most common available shipping actions: 

* [Process](https://docs.intersoftsapient.net/docs/create-shipment-with-action-process): an action that finalises the shipment creation and prepares the shipment for transportation. 

In SAPIENT, **Process** is the default setting. If this field is not populated in the **Create Shipment** request/by using **Process**, a label is returned in the **Create Shipment** response and the shipment is ready for manifesting immediately.

* [Create](https://docs.intersoftsapient.net/docs/create-shipments-with-action-create): an action that initiates a new shipment entry in the system. This action captures all the necessary details of the shipment to generate shipping documents and prepare for the actual shipping process. 
* [Allocate](https://docs.intersoftsapient.net/docs/create-shipments-with-action-allocate): an action that assigns resources (like items from inventory) to the shipment for fulfilment. This action ensures that the items intended for shipment are set aside and ready to be despatched.

The **Create** and **Allocate** actions do not return <Glossary>labels</Glossary> immediately, but instead rely on the customer calling the **Print Shipment** API. Using “Allocate”, the carrier tracking number is returned in the **Create Shipment** response for your reference. Using the **Create** action, the <Glossary>tracking number</Glossary> is not generated until the **Print Shipment** request is made.

Any of these actions can be used in conjunction with the the following options.

## Use shipment status in Update Shipment API

The *shipment status* indicates the current state or condition of a shipment within the shipment process. Each status reflects a specific phase in the shipment lifecycle, providing visibility to both shippers and recipients. The following are the available shipment statuses in SAPIENT: 

1. **Picked**: indicates that the items for the shipment have been successfully collected from the inventory and are ready for the next steps in the shipment process. 

The **Picked** status can be used if you want to print the labels in advance. To achieve this, simply create your shipments using the **Process** action—when picked and ready to despatch, update the status on the shipment to **Picked**. After, you can manifest all the picked shipments, ensuring the shipments that are yet to be processed are not manifested.

1. **Release**: indicates that the shipment has been authorised for despatch or has been cleared for shipment to the next destination.
2. **Cancel**: indicates that the shipment has been canceled and will not be processed any further.
3. **Hold**: indicates that the shipment is temporarily paused and is not progressing to the next phases of fulfillment or transport until the necessary requirements are fulfilled.

> 📘 *Note*
>
> *The “**Hold**” and “**Release**” statuses are available if a shipment needs to be delayed and only included in manifest production once it has been released.*

The shipment “**Status**” function can be used as a simple way to manage when shipments are ready to be dispatched.

## Using Containers

Using the shipment status can be adopted for an operation to manage a fluid picking and packing set up. Hence,  <Glossary>containerisation</Glossary> allows users to manage shipments based on any number of variables.

**Carrier Sortation**: for high volume users, your carrier may ask you to provide shipments pre-sorted based on service, destination or other factors. With containerisation, you can allocate shipments to a specific <Glossary>container</Glossary> and then manifest by container ID. The container ID could be a postcode sector or country code—or a specific <Glossary>carrier</Glossary> service.

**Managing Despatch Dates**: likewise, if you process pre-orders that need to be despatched on a specific date, a container ID could be set up for each date and shipments allocated based on requirements with the manifesting done by date, at container level.

> 📘 *Note*
>
> *A container can be created with any Container ID that suits the needs of the organisation.*

## Pre-allocate tracking number API

The <Glossary>pre-allocated tracking number</Glossary> API offers you the opportunity to request a pre-allocated Royal Mail tracking number for a destination and service. If your warehouse or eCommerce site operates in a way that you require a tracking number to be linked with your order, but you do not have the final details of your order yet, then consider using the [Pre Allocate Tracking Number](https://docs.intersoftsapient.net/reference/post_v4-shipments-preallocatetrackingnumber-rm) service. 

When requesting  pre-allocated tracking number, only a small amount of information is passed in the request body and a small amount of validation is done in the back-end to return a Royal Mail <Glossary>tracking number</Glossary> . The tracking number is issued without creating either the <Glossary>shipments</Glossary> or the <Glossary>labels</Glossary> . 

When you are ready to ship your order, simply call the Royal Mail [Create Shipment](https://docs.intersoftsapient.net/reference/post_v4-shipments-rm) API passing the pre-allocated tracking number that was returned in the **Pre Allocate Tracking Number** response in the **PreAllocatedBarcode** object of the **Create Shipment** request. The platform then creates the shipment and label with the tracking number you provided. 

> 🚧 *Important*
>
> *Currently, this service is only available for Royal Mail services that have a 1D Tracking Number generated—this includes shipments using untracked services with the Royal Mail Recorded Signed for enhancement.*