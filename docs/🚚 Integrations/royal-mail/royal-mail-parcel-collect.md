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
icon: fad fa-cart-flatbed-suitcase
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
The collections service integration automates the return process, reducing manual work and potential errors associated with managing returns and tracking items.

## Weight classifications

The Royal Mail collection allows the system to default the dimensions and format based on the weight of the shipment, applying the maximum dimensions specified on our website for each format:

| Weight range            | Classification |
| ----------------------- | -------------- |
| **750g or under**       | Large Letters  |
| **751g – 2kg**          | Small Parcels  |
| **Over 2kg up to 20kg** | Medium Parcels |

<Callout icon="🚧" theme="warning">
  ### _Important_

  _Before using this feature, make sure to enable the&#x20;_**_Collect_**_&#x20;integration via the [integration activation](https://docs.intersoftsapient.net/docs/integration-activation) page._
</Callout>

## Create a return shipment

<Callout icon="📘" theme="info">
  ### _Note_

  _The return shipment must be created using the [Create Shipment](https://docs.intersoftsapient.net/reference/post_v4-shipments-rm) request._
</Callout>

If you want to enable your customers to have their returns collected from their homes, create a Royal Mail shipment using the Royal Mail's return services. Ensure you meet [all the requirements](https://docs.intersoftsapient.net/docs/royal-mail-returns) when creating a returns shipment. You can then request a Royal Mail collection for the <Glossary>shipment</Glossary>.

<Callout icon="🚧" theme="warn">
  ### _Important_

  _Royal Mail does not have the&#x20;_**_Test_**_&#x20;environment for Collection service. It can only be developed against the&#x20;_**_Production_**_&#x20;environment. This means that you need to book an actual collection and then cancel it before the date of the collection._
</Callout>

## Configure collection options

You can either allow SAPIENT to default the collection to the first available collection date or allow your customer to select their preferred collection date, usually up to 5 days in advance. You can also specify if you want the <Glossary>labels</Glossary> to be brought by Royal Mail when collecting the shipment or printed by your customer.

<Accordion title="BringMyLabel parameter" icon="fa-tag">
  By default, the labels are not brought by Royal Mail. If you need this enhancement, set the **BringMyLabel** parameter to **True**. The return shipments and collections do not require manifesting.
</Accordion>


<Image src="https://files.readme.io/23d766f112ee59190e6487da2b979ae6ab2368a441d69ab8f6c8463360b56f94-Collection_service_flow.png" alt="Workflow for creating shipments using collection service" align="center" caption="Workflow for creating shipments using collection service" />


<Callout icon="📘" theme="info">
  ### _Note_

  _The name displayed on the Parcel Collect notification sent to the end consumer is driven by the name set up on the <Glossary>Online Business Account</Glossary> (OBA) account. If you wish to change the name on your account, contact your Royal Mail account handler as you cannot change the name for Parcel Collect alone._
</Callout>

***

### See also

<Cards>
  <Card title="Create Shipment API" href="https://docs.intersoftsapient.net/reference/post_v4-shipments-rm" icon="fa-plus" target="_blank">
    Generate return labels for your packages.
  </Card>

  <Card title="Return requirements" href="https://docs.intersoftsapient.net/docs/royal-mail-returns" icon="fa-rotate-left" target="_blank">
    View all requirements for creating a returns shipment.
  </Card>

  <Card title="Integration activation" href="https://docs.intersoftsapient.net/docs/integration-activation" icon="fa-toggle-on" target="_blank">
    Enable the Collect integration for your account.
  </Card>
</Cards>
