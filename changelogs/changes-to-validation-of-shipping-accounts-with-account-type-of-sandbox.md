---
title: Changes to validation of Shipping Accounts with Account Type of Sandbox
author: Intersoft
hidden: true
published_at: '2023-05-11T12:29:42.223Z'
type: improved
---
The following changes have been made to the validation of Shipping Accounts that have the Account Type set as Sandbox:

* For Royal Mail Sandbox shipping accounts, the Department Number sent in the createShipment request does not need to be a valid Department for the Royal Mail account
* It will now be possible for a shipping account to be changed from Production to Sandbox if Production shipments have been created for the account. When this is done, the Production shipments will still be available for manifesting in the Manifesting UI