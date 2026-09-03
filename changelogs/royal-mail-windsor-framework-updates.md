---
title: Royal Mail Windsor Framework updates
author: Laura Price
hidden: true
published_at: '2026-02-23T13:18:36.779Z'
type: improved
---
The following changes have been made for Royal Mail shipments sent from Great Britain to Northern Ireland (addresses with a GB country code and postcode beginning BT):

1. The shipment declaredValue must equal the sum of the item values within the shipment. The declaredValue cannot be less than or greater than the sum of the item values.
2. For B2B shipments where a pre-registration number with pre-registration type UKIMS is provided, previous logic that treated Item HS Code as optional has now been removed. Royal Mail’s standard reference data will now be used to determine whether Item HS Code is mandatory or optional. B2B shipments are validated against Ruleset K, which is documented in the <Anchor label="Royal Mail Validation Rules" target="_blank" href="https://docs.intersoftsapient.net/docs/royal-mail-validation-rules">Royal Mail Validation Rules</Anchor> guide.

<br />