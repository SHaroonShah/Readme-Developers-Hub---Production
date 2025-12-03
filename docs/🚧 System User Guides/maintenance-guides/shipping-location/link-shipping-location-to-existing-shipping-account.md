---
title: Link shipping location to existing shipping account
excerpt: >-
  A _shipping location_ is a physical address designated area from which the
  goods are sent or despatched. It plays a crucial role in the logistics and
  shipping process.
deprecated: false
hidden: false
icon: fad fa-link
metadata:
  robots: index
---
In SAPIENT, you can link on or more shipping locations to your carrier's existing <Glossary>shipping account</Glossary>. This setup enhances operational efficiency, supports scalability, and ensures compliance, making it easier to manage shipments from various origins under one system.

## How to link shipping location to an existing shipping account

<Tabs>
  <Tab title="Link via SAPIENT UI">
    <br />

    To link a shipping location to an existing shippinh account in SAPIENT, perform the steps as explained in the following procedure.

    <ToggleList>
      <ToggleListItem title={<strong>1. Access the shipping locations page</strong>} icon="fa-rocket">
        <br />

        In the left navigation panel, select **Shipping Locations**.

        <Image align="center" border={true} src="https://files.readme.io/a84f50bafad4110e2244fa56d73b34787cf197d6a4e3de326ad287880d85e835-Shipping_locations_option.png" alt="Accessing shipping locations" />

        ***
      </ToggleListItem>

      <br />

      <ToggleListItem title={<strong>2. Select location to link</strong>} icon="fa-rocket">
        <br />

        On the **Shipping Locations** page that appears, select the shipping location that you want to link to an existing shipping account and on the **View Shipping Location\[location name]** form that opens, in the ASSOCIATED SHIPPING ACCOUNTS block, select ![](https://files.readme.io/80cdc77d8bb03dab8b51d717f073576dae0699b7acc8a964c6f2cf74bcd27556-Link_existing_shipping_account_button.png).

        <Image align="center" border={true} src="https://files.readme.io/0caad28a80311077a940bff28ebd29c2ceadd655c014741d090bcb5c51f5cbc5-Linking_shipping_account.png" alt="Selecting option to add shipping location" />

        ***
      </ToggleListItem>

      <br />

      <ToggleListItem title={<strong>3. Configure shipping account details </strong>} icon="fa-rocket">
        <br />

        On the **Link Shipping Account** form that opens, update the necessary information as expalined in the following table.

        <Image align="center" border={true} src="https://files.readme.io/3de31c22fb2c5ee0f5257c680dbd966f3059acb17241abb26012ed820a9dc1f6-Entering_shipping_account_details.png" alt="Entering location details" />

        <br />

        <AsteridkForMandatoryElements />

        <br />

        <Columns layout="auto">
          <Column>

            |         Element        | Description                                                                                           |
            | :--------------------: | :---------------------------------------------------------------------------------------------------- |
            |      **Carrier**\*     | From the dropdown menu, select the needed carrier.                                                    |
            | **Shipping Account**\* | From the dropdown menu, select the shipping account to which you want to link this shipping location. |
          </Column>
        </Columns>

        > 📘 **Note**
        >
        > If you have selected Royal Mail as your carrier option, then an additional **CARRIER DETAILS** block is displayed. To learn more on how to fill this block, refer to the <Anchor label="Add Royal Mail shipping account" target="_blank" href="https://docs.intersoftsapient.net/docs/shipping-account-requirements#/">Add Royal Mail shipping account</Anchor> section.

        ***
      </ToggleListItem>

      <br />

      <ToggleListItem title={<strong>4. Save changes </strong>} icon="fa-rocket">
        <br />

        After entering all the relevant information, select ![](https://files.readme.io/7f3338ad6d04eed0cfe60a5831902bd726f21988472aa810308695f020fe5b89-Link_shipping_account_button.png).

        Once done, the shipping location is successfully linked to your shipping account.

        ***
      </ToggleListItem>
    </ToggleList>
  </Tab>

  <Tab title="Link via API">
    <br />

    To link a shipping location to an existing shipping account via our API, refer to the following endpoint:

    <Cards>
      <Card title="Link Locations" href="https://docs.intersoftsapient.net/v4.02_Coding/reference/post_v4-shippingaccounts-rm-shippingaccountid-linklocations#/" icon="fa-solid fa-code">
        Complete API reference for linking shipping locations to an exsiting shipping account
      </Card>
    </Cards>
  </Tab>
</Tabs>

To link a shipping location to your carrier shipping account in SAPIENT, follow the steps as explained in the following procedure.

1. In the left navigation panel, select **Shipping Locations**.

<Image align="center" alt="Accessing shipping locations" border={true} caption="Accessing shipping locations" src="https://files.readme.io/a84f50bafad4110e2244fa56d73b34787cf197d6a4e3de326ad287880d85e835-Shipping_locations_option.png" />

2. On the **Shipping Locations** page that appears, select the shipping location that you want to link to an existing shipping account and on the **View Shipping Location[location name]** form that opens, in the ASSOCIATED SHIPPING ACCOUNTS block, select ![](https://files.readme.io/80cdc77d8bb03dab8b51d717f073576dae0699b7acc8a964c6f2cf74bcd27556-Link_existing_shipping_account_button.png).

<Image align="center" alt="Selecting option to add shipping location" border={true} caption="Selecting option to link existing shipping account" src="https://files.readme.io/0caad28a80311077a940bff28ebd29c2ceadd655c014741d090bcb5c51f5cbc5-Linking_shipping_account.png" />

3. On the **Link Shipping Account** form that opens, update the necessary information as explained in the following table.

<Image align="center" alt="Entering location details" border={true} caption="Entering shipping account details" src="https://files.readme.io/3de31c22fb2c5ee0f5257c680dbd966f3059acb17241abb26012ed820a9dc1f6-Entering_shipping_account_details.png" />

<AsteridkForMandatoryElements />

|        Element        | Description                                                                                           |
| :-------------------: | :---------------------------------------------------------------------------------------------------- |
|      **Carrier***     | From the dropdown menu, select the needed carrier.                                                    |
| **Shipping Account*** | From the dropdown menu, select the shipping account to which you want to link this shipping location. |

> 📘 _Note_
>
> _If you have selected Royal Mail as your carrier option, then an additional**CARRIER DETAILS** block is displayed. To learn more on how to fill this block, refer to the <Anchor label="Add Royal Mail shipping account" target="_blank" href="https://docs.intersoftsapient.net/docs/shipping-account-requirements#/">Add Royal Mail shipping account</Anchor> section._

4. After entering all the relevant information, select ![](https://files.readme.io/7f3338ad6d04eed0cfe60a5831902bd726f21988472aa810308695f020fe5b89-Link_shipping_account_button.png).

Once done, the shipping location is successfully linked to your shipping account.

<Callout icon="💡" theme="default">
  ### _Tip_

  _You can also link the shipping locations to your carrier's shipping account via the<Anchor label="Link Locations" target="_blank" href="https://docs.intersoftsapient.net/reference/post_v4-shippingaccounts-rm-shippingaccountid-linklocations#/">Link Locations</Anchor> API endpoint._
</Callout>

<br />
