---
title: Shipping Accounts
excerpt: >-
  A shipping account is where you assign your carrier credentials and link them
  to the relevant shipping location(s). This guide shows how to create and
  manage shipping account(s).
deprecated: false
hidden: true
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
**Shipping Accounts**

- The accounts you hold directly with a carrier and want to use for creating shipments in Sapient. The Shipping Accounts will have to be registered in Sapient. Each Shipping Account will have an alias assigned by you and a global unique identifier assigned by the system. Both values can be used to identify a Shipping Account where ShippingAccountId is required.  
  To be able to use a Shipping Account to create shipments from one of your shipping locations, the shipping account and shipping locations must be linked. Some carriers require specific details before they will validate the link.  
  For Royal Mail, these are your RM OBA Account Number, the Posting Location Code that has been assigned by Royal Mail and an OBA Access Code that has either been given to you by Royal Mail or it will be generated automatically by the system. You won’t be able to use the Shipping Account and Shipping Location to create shipments before the Royal Mail OBA team validates the details.  
  If you have multiple Shipping Accounts with one carrier and want to use them in Sapient, you will need to add them.  
  You can link multiple Shipping Locations with a Shipping Account and one Shipping Location with multiple Shipping Accounts.

**Account Type**

- Sandbox and Production. When a Shipping Account is set as Sandbox it can only be used to create test shipments. The Shipping Account still needs to be linked to a Shipping Location and approved by the carrier before it can be used for shipments.