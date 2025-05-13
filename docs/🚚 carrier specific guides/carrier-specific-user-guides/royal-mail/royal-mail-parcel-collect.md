---
title: Use collection service
excerpt: >-
  _Collection_ is a process/service that manages the collection of return
  shipments from customers. This includes tracking items being returned,
  ensuring that they are sent back to the appropriate location, and managing any
  associated logistics and financial aspects, such as refunds or adjustments to
  inventory.
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
The collections service integration automates the return process, reducing manual work and potential errors associated with managing returns and tracking items.

The Royal Mail collection allows the system to default the dimensions and format based on the weight of the shipment, applying the maximum dimensions specified on our website for each format:

* Shipments weighing 750g or under will be classified as Large Letters.
* Shipments weighing between 751g and 2kg will be classified as Small Parcels.
* Shipments weighing over 2kg up to 20kg will be classified as Medium Parcels.

> 🚧 *Important*
>
> *Before using this feature, make sure to enable the**Collect** integration via the [integration activation](https://docs.intersoftsapient.net/docs/integration-activation) page.*

If you want to enable your customers to have their returns collected from their homes, you can create a Royal Mail shipment using one of Royal Mail's return services <Glossary>TSN Tracked Returns 24</Glossary> or <Glossary>TSS Tracked Returns 48</Glossary>. Please ensure to meet [all the requirements](https://docs.intersoftsapient.net/docs/royal-mail-returns) when creating a returns shipment. You can then request a Royal Mail collection for the <Glossary>shipment</Glossary>.

> 🚧 *Important*
>
> *Royal Mail does not have the**Test** environment for Collection service. Therefore, it can only be developed against the **Production** environment. This means that you need to book an actual collection and then cancel it before the date of the collection.*

You can either allow SAPIENT to default the collection to the first available collection date or allow your customer to their preferred collection date, usually up to 5 days in advance. You can also specify if you want the <Glossary>labels</Glossary> to be brought by Royal Mail when collecting the shipment or printed by your customer.

> 📘 *Note*
>
> *The return shipment must be created using the[Create Shipment](https://docs.intersoftsapient.net/reference/post_v4-shipments-rm) request.*

By default, the labels are not brought by Royal Mail. If you need this enhancement, you must specify it by setting the **BringMyLabel** parameter to **True**. The return shipments and collections do not require manifesting.

<Image align="center" alt="Workflow for creating shipments using collection service" border={false} caption="Workflow for creating shipments using collection service" src="https://files.readme.io/23d766f112ee59190e6487da2b979ae6ab2368a441d69ab8f6c8463360b56f94-Collection_service_flow.png" />

> 📘 *Note*
>
> *The name displayed on the Parcel Collect notification sent to the end consumer is driven by the name set up on the<Glossary>Online Business Account </Glossary> (OBA) account. Therefore, If you wish to change the name on your account, contact your Royal Mail account handler as you cannot simply change the name just for Parcel Collect.*