---
title: DX Freight sign-off
excerpt: >-
  Complete the DX Freight sign-off steps so your shipping account is ready to
  create shipments.
deprecated: false
hidden: false
icon: far fa-clipboard-check
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
Once you have created the DX Freight <Glossary>shipping account</Glossary>, make sure you have the correct information before you start using it to ship with DX Freight.

<Callout icon="💡" theme="default">
  ### _Tip_

  _The DX Freight integration is pre-approved, but you must have the required information beforehand to ship with DX Freight._
</Callout>

In order to ship with DX Express, consider the following:

1. The **Carrier Account Number**, **Origin Service Center (Depot)**, and **Password** have been provided to you by the DX Freight's sales team.
2. Set up the shipping account with the <Glossary>account type</Glossary> set to **Production**.

> 🚧 _Important_
>
> _If you are using the**Production** account type for testing your shipments, you will be billed accordingly as DX Express bills on manifesting rather than scanning. To avoid that, it is advised to please cancel those shipments. Be mindful that the shipments can only be cancelled if the shipment date is today or within the next 28 days. Consignments with a past shipment date cannot be cancelled._

3. Once the account has been created with the correct information, the status of your shipping account is set to **'Enabled'**. You can check the account status by viewing the shipping account or via the [Get Account](https://api.test.intersoftsapient.net/docs/v4-DX/api/index.html#tag/Shipping-Accounts/paths/~1v4~1shippingAccounts~1DX~1%7BshippingAccountId%7D/get) API.
4. Although, the Intersoft DX Freight integration is approved by the <Glossary>carrier</Glossary>, it is recommended to create a few test labels with services you will be using and share the <Glossary>labels</Glossary> with the carrier for review to avoid any discrepancies.
5. It is also recommended to run the end to end test to ensure that the integration was set up correctly by sending out a test parcel. If tracking has been enabled for the carrier, then you should also receive the tracking events via the <Glossary>tracking webhook</Glossary>.

***

### See also

<Cards columns={3}>
  <Card title="Add Shipping Account" href="https://docs.intersoftsapient.net/docs/add-dx-freight-shipping-account" icon="fa-solid fa-truck">
    Access the step-by-step guide on how to set up DX Freight shipping account on SAPIENT.
  </Card>

  <Card title="Add Tracking Account" href="https://docs.intersoftsapient.net/docs/add-dx-freight-tracking-account#/" icon="fa-solid fa-search-location">
    Access the step-by-step guide on how to set up DX Freight tracking account on SAPIENT.
  </Card>

  <Card title="API References" href="https://docs.intersoftsapient.net/reference/get_v4-shippingaccounts-dxf" icon="fa-solid fa-code">
    Explore the DX Freight API endpoints for a seamless shipping experience.
  </Card>
</Cards>

<br />
