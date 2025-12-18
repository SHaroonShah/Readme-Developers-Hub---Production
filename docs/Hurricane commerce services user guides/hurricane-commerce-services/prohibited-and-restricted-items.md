---
title: Prohibited and restricted items
excerpt: >-
  _Prohibited and restricted items_ are goods that are not allowed to be
  imported or exported according to specific regulations. Each country has its
  own list of prohibited items, which can include anything from certain
  chemicals to specific types of food or products that violate local laws.
deprecated: false
hidden: false
icon: fad fa-not-equal
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
<Image align="center" border={true} src="https://files.readme.io/3e53aceb01b0e0ed75febefc59a27a61adb14eed84aa12e703de14ee0072c004-Prohibited_and_restricted_items.png" className="border" />

Hurricane provides your business with the information required to make a decision on whether goods can be imported or not, and what specific licences are required.

The compliance API provides a standalone interface for the end user to check if there are any restrictions or prohibitions on the <Glossary>product</Glossary>(s) being shipped on the three main areas:

<Image align="center" border={false} width="500px" src="https://files.readme.io/835f9346589257843f9525927bce07d472ce27b2e464281c37c99995b48c67cf-1212.png" />

<Cards columns={1}>
  <Card title="Import" icon="fa-solid fa-arrow-down">
     Whether the product in question is able to be shipped into the destination country. There are products and commodities that cannot be shipped into certain countries without special documentation and some which are prohibited entirely. A good example is of alcohol-based perfumes into certain Muslim countries.
  </Card>

  <Card title="Export" icon="fa-solid fa-arrow-up">
     Whether the product in question is able to be shipped from the country of origin. The Convention on International Trade for Endangered Species of Flora and Fauna (CITES) details a number of commodities that cannot be shipped outside of their country of origin, such as rare hardwoods. Additionally, some hi-tech equipment now also requires additional documentation to be supplied in order for it to leave certain countries. An example of this is night vision goggles leaving USA.
  </Card>

  <Card title="Transportation" icon="fa-solid fa-truck">
     Whether the product in question can be shipped using the <Glossary>carriers</Glossary> that have been selected or are available. These can be subtler than the first two; however, a recent case in point concerns lithium-based batteries (both lithium ion and lithium polymer). If left switched on, it can cause excessive heat buildup, most notably recently with the Samsung Galaxy Tab 7. This has led to transportation restrictions around lithium batteries. So only a certain number per <Glossary>consignment</Glossary> can be shipped in the cargo hold of commercial passenger aircraft. Above this, the package must be shipped using a purely cargo method only.
  </Card>
</Cards>

> 📘 _Note_
>
> _For more information on how to use this API service, refer to the [Prohibited Items](https://docs.intersoftsapient.net/reference/post_v4-prohibiteditems) block of the **API References** section._
