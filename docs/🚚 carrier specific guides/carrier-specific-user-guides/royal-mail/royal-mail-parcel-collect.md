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

> 🚧 _Important_
> 
> _Before using this feature, make sure to enable the **'Collect'** integration via the [integration activation](https://docs.intersoftsapient.net/docs/integration-activation) page._

If you want to enable your customers to have their returns collected from their homes, you can create a Royal Mail shipment using one of Royal Mail's return services <<glossary:TSN Tracked Returns 24>> or <<glossary:TSS Tracked Returns 48>>. Please ensure to meet [all the requirements](https://docs.intersoftsapient.net/docs/royal-mail-returns) when creating a returns shipment. You can then request a Royal Mail collection for the <<glossary:shipment>>. 

> 🚧 _Important_
> 
> _Royal Mail does not have the **Test** environment for Collection service. Therefore, it can only be developed against the **Production** environment. This means that you need to book an actual collection and then cancel it before the date of the collection._

You can either allow SAPIENT to default the collection to the first available collection date or allow your customer to their preferred collection date, usually up to 5 days in advance. You can also specify if you want the <<glossary:labels>> to be brought by Royal Mail when collecting the shipment or printed by your customer.

> 📘 _Note_
> 
> _The return shipment must be created using the [CreateShipment](https://docs.intersoftsapient.net/reference/post_v4-shipments-rm) request._

By default, the labels are not brought by Royal Mail. If you need this enhancement, you must specify it by setting the **BringMyLabel** parameter to **True**. The return shipments and collections do not require manifesting.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/23d766f112ee59190e6487da2b979ae6ab2368a441d69ab8f6c8463360b56f94-Collection_service_flow.png",
        "",
        "Workflow for creating shipments using collection service"
      ],
      "align": "center",
      "caption": "Workflow for creating shipments using collection service"
    }
  ]
}
[/block]


> 📘 _Note_
> 
> _The name displayed on the Parcel Collect notification sent to the end consumer is driven by the name set up on the <<glossary:Online Business Account>> (OBA) account. Therefore, If you wish to change the name on your account, contact your Royal Mail account handler as you cannot simply change the name just for Parcel Collect._