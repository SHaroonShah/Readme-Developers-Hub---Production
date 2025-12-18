---
title: Prohibited and Restricted Items
excerpt: >-
  Explore the regulations and compliance requirements for importing, exporting,
  and transporting goods, including prohibited and restricted items.
deprecated: false
hidden: false
icon: fad fa-not-equal
link:
  new_tab: false
metadata:
  title: ''
  description: ''
  robots: index
---
<Image align="center" className="border" border={true} src="https://files.readme.io/3e53aceb01b0e0ed75febefc59a27a61adb14eed84aa12e703de14ee0072c004-Prohibited_and_restricted_items.png" />

Hurricane provides your business with the information required to make a decision on whether goods can be imported or not, and what specific licences are required.

<Accordion title="Compliance API Overview" icon="info-circle">
  The compliance API provides a standalone interface for the end user to check if there are any restrictions or prohibitions on the <Glossary>product</Glossary>(s) being shipped on the three main areas:
</Accordion>

<Cards columns={1}>
  <Card title="Import" icon="arrow-down">
    Whether the product in question is able to be shipped into the destination country. There are products and commodities that cannot be shipped into certain countries without special documentation and some which are prohibited entirely. A good example is of alcohol-based perfumes into certain Muslim countries.
  </Card>
  <Card title="Export" icon="arrow-up">
    Whether the product in question is able to be shipped from the country of origin. The Convention on International Trade for Endangered Species of Flora and Fauna (CITES) details a number of commodities that cannot be shipped outside of their country of origin, such as rare hardwoods. Additionally, some hi-tech equipment now also requires additional documentation to be supplied in order for it to leave certain countries. An example of this is night vision goggles leaving USA.
  </Card>
  <Card title="Transportation" icon="truck">
    Whether the product in question can be shipped using the <Glossary>carriers</Glossary> that have been selected or are available. These can be subtler than the first two; however, a recent case in point concerns lithium-based batteries (both lithium ion and lithium polymer). If left switched on, it can cause excessive heat buildup, most notably recently with the Samsung Galaxy Tab 7. This has led to transportation restrictions around lithium batteries. So only a certain number per <Glossary>consignment</Glossary> can be shipped in the cargo hold of commercial passenger aircraft. Above this, the package must be shipped using a purely cargo method only.
  </Card>
</Cards>

> 📘 *Note*
>
> *For more information on how to use this API service, refer to the [Prohibited Items](https://docs.intersoftsapient.net/reference/post_v4-prohibiteditems) block of the **API References** section.*