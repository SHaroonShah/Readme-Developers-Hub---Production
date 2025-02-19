---
title: Tracking Webhook Solution
excerpt: ''
deprecated: false
hidden: true
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
***

add tracking flow here

***

**Royal Mail tracking**

* Allows for a 30-day policy to keep tracking a shipment
* Almost real-time updates - **COMING SOON!**
* Trackable products:
  * Tracked Standard, Tracked High Volume, Tracked Returns
  * Special Delivery
  * International Tracked and Signed, International Tracked, International Signed
* NOTE: no historical updates will be pushed

***

Allows to send up to 1000 tracking numbers in one /v4trackings request

Retry logic to keep updates for 72h if the webhook connection on your end is not available before we expire them

<br />

<br />

or more information on how to set this up,For these shipments, the tracking number must be provided to Intersoft via the POST/v4/trackings API. **Please Note this is a chargeable endpoint.**
