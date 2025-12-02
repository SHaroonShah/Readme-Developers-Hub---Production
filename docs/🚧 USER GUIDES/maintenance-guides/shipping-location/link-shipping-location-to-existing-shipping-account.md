---
title: Link shipping location to existing shipping account
excerpt: >-
  Learn how to link shipping locations to existing carrier shipping accounts in
  SAPIENT to enhance operational efficiency and streamline logistics management.
deprecated: false
hidden: false
icon: fad fa-link
link:
  new_tab: false
metadata:
  robots: index
---
## Overview

In SAPIENT, you can link one or more shipping locations to your carrier's existing <Glossary>shipping account</Glossary>. This setup enhances operational efficiency, supports scalability, and ensures compliance, making it easier to manage shipments from various origins under one system.

<Cards columns={2}>
  <Card title="Shipping Location" icon="map-marker-alt">
    A physical address designated area from which goods are sent or dispatched, playing a crucial role in the logistics and shipping process.
  </Card>
  <Card title="Shipping Account" icon="credit-card">
    Your carrier's existing account that can be linked to multiple shipping locations for centralized management.
  </Card>
</Cards>

## Linking Process

Follow these steps to link a shipping location to your carrier shipping account in SAPIENT:

<Accordion title="Step-by-Step Procedure" icon="list-ol">

### Step 1: Access Shipping Locations
In the left navigation panel, select **Shipping Locations**.

<Image align="center" alt="Accessing shipping locations" border={true} caption="Accessing shipping locations" src="https://files.readme.io/a84f50bafad4110e2244fa56d73b34787cf197d6a4e3de326ad287880d85e835-Shipping_locations_option.png" />

### Step 2: Select Location to Link
On the **Shipping Locations** page that appears, select the shipping location that you want to link to an existing shipping account. On the **View Shipping Location [location name]** form that opens, in the ASSOCIATED SHIPPING ACCOUNTS block, select ![](https://files.readme.io/80cdc77d8bb03dab8b51d717f073576dae0699b7acc8a964c6f2cf74bcd27556-Link_existing_shipping_account_button.png).

<Image align="center" alt="Selecting option to add shipping location" border={true} caption="Selecting option to link existing shipping account" src="https://files.readme.io/0caad28a80311077a940bff28ebd29c2ceadd655c014741d090bcb5c51f5cbc5-Linking_shipping_account.png" />

### Step 3: Enter Shipping Account Details
On the **Link Shipping Account** form that opens, update the necessary information as outlined below.

<Image align="center" alt="Entering location details" border={true} caption="Entering shipping account details" src="https://files.readme.io/3de31c22fb2c5ee0f5257c680dbd966f3059acb17241abb26012ed820a9dc1f6-Entering_shipping_account_details.png" />

</Accordion>

## Form Fields Reference

<Columns layout="auto">
  <Column>

<AsteridkForMandatoryElements />

|         Element        | Description                                                                                           |
| :--------------------: | :---------------------------------------------------------------------------------------------------- |
|      **Carrier**\*     | From the dropdown menu, select the needed carrier.                                                    |
| **Shipping Account**\* | From the dropdown menu, select the shipping account to which you want to link this shipping location. |

  </Column>
  <Column>

> 📘 **Royal Mail Special Requirements**
>
> If you have selected Royal Mail as your carrier option, then an additional **CARRIER DETAILS** block is displayed. To learn more on how to fill this block, refer to the <Anchor label="Add Royal Mail shipping account" target="_blank" href="https://docs.intersoftsapient.net/docs/shipping-account-requirements#/">Add Royal Mail shipping account</Anchor> section.

  </Column>
</Columns>

## Complete the Linking

After entering all the relevant information, select ![](https://files.readme.io/7f3338ad6d04eed0cfe60a5831902bd726f21988472aa810308695f020fe5b89-Link_shipping_account_button.png).

Once done, the shipping location is successfully linked to your shipping account.

<Callout icon="💡" theme="default">
  ### *Alternative Method*

  *You can also link the shipping locations to your carrier's shipping account via the <Anchor label="Link Locations" target="_blank" href="https://docs.intersoftsapient.net/reference/post_v4-shippingaccounts-rm-shippingaccountid-linklocations#/">Link Locations</Anchor> API endpoint.*
</Callout>