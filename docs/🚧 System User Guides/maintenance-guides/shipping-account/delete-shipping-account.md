---
title: Delete shipping account
excerpt: >-
  Deleting a shipping account provides a way to remove shipping accounts that
  are no longer needed, such as when a customer closes their account or when a
  business discontinues a partnership with a shipping provider.
deprecated: false
hidden: false
icon: fad fa-circle-trash
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
Deleting the <Glossary>shipping account</Glossary> that is no longer required is quite handy in certain situations, for example,  if an account was set up incorrectly or is causing issues, deleting it can clear up any confusion and prevent operational problem or removing obsolete data that could complicate integration processes with external APIs or systems.

<br />

<Tabs>
  <Tab title="Delete via SAPIENT UI">
    <br />

    To delete a shipping account in SAPIENT, perform the steps as explained in the following procedure.

    <ToggleList>
      <ToggleListItem title={<strong>1. Access the manifesting option</strong>} icon="fa-rocket">
        <br />

        In the side navigation panel, select the **Shipment Processing** > **Manifesting** option.

        <Image align="center" border={true} src="https://files.readme.io/43b41b65377780fd19531fd2378483c9b0c7d99c88b2c5242e584ef4225c5dae-Accessing_manifesting_option.png" alt="Accessing shipments" />

        ***
      </ToggleListItem>

      <br />

      <ToggleListItem title={<strong>2. Configure filters and sorting</strong>} icon="fa-rocket">
        <br />

        In the **Manifesting** page that opens, you can:

        * Sort the list either by <Glossary>carrier</Glossary> or <Glossary>shipping account</Glossary>
        * Change the <Glossary>shipping location</Glossary> by selecting the **Change Location** button

        <br />

        <Image align="center" border={true} src="https://files.readme.io/41603935fe204b0f21f146742408bd60584a5659ebb2a31c9302a475d93d24cf-sorting_and_changing_location.png" alt="Specifying filters" />
      </ToggleListItem>

      <br />

      <ToggleListItem title={<strong>3. Apply additional filters </strong>} icon="fa-rocket">
        <br />

        In the **Manifesting** page that opens, you can:

        * Sort the list either by <Glossary>carrier</Glossary> or <Glossary>shipping account</Glossary>
        * Change the <Glossary>shipping location</Glossary> by selecting the **Change Location** button

        <br />

        <Image align="center" border={true} src="https://files.readme.io/41603935fe204b0f21f146742408bd60584a5659ebb2a31c9302a475d93d24cf-sorting_and_changing_location.png" alt="Specifying filters" />

        ***
      </ToggleListItem>

      <br />

      <ToggleListItem title={<strong>4. Select shipments to hold </strong>} icon="fa-rocket">
        <br />

        Based on your requirements, select any of the following options:

        * **For bulk operations:**
          Next to the shipments that you want to hold, select ![alt text](https://files.readme.io/9a2d6ed673346e9c4c73e5a15a5dd8078483d6a780cf49d3f274cbf22c4df997-Hold_button.png).

        * **For individual shipments:**
          Next to the shipment, select ![alt text](https://files.readme.io/b9b3f904604324043bea000c1255950ee01f735b7e665909e3bbd409faeb2956-View_button.png).

        ***
      </ToggleListItem>

      <br />

      <ToggleListItem title={<strong>5. Confirm hold action</strong>} icon="fa-rocket">
        <br />

        On the page that opens, next to the shipment, select the checkbox and then click ![alt text](https://files.readme.io/1d487b18ddbdc249cef48fe35d465d2c89f5c7feb501f8cc797061ee607320cb-Hold_Shipments_button.png).

        <Image align="center" border={true} src="https://files.readme.io/3320e4d15decec9a248bb0a89c20e394b259c8c1368bd741773cd7814ed774c4-Hold_shipments_option.png" alt="Accessing option to cancel shipments" />

        ***
      </ToggleListItem>

      <br />

      <ToggleListItem title={<strong>6. Provide reason for hold</strong>} icon="fa-rocket">
        <br />

        In the confirmation dialog that appears, from the dropdown menu, select the reason for holding the shipment, and then click **Yes**.

        <Image align="center" border={true} src="https://files.readme.io/2ab6f56822de74b6346b1480d45c322673c372603a21ae06bb225425ba332f70-Conforming_shipment_hold.png" width="350px" alt="Confirming shipment cancellation" />

        <br />

        Once confirmed, the shipments are removed from the current list and is displayed in the list of held shipments. If needed, you can [release the held shipments](https://docs.intersoftsapient.net/docs/release-shipment) within the 28 days time frame and work with them accordingly.
      </ToggleListItem>
    </ToggleList>

    <Callout icon="💡" theme="default">
      ### *Tip*

      *You can access the held shipments directly from this page by selecting the**View Held Shipments** option or by accessing the **Shipment Processing** > **Held** option from the side navigation panel.*

      <Image align="center" border={true} src="https://files.readme.io/bc5120461fe99089d00c1c83f39a4e5e0706b8a62d25f2c39b697cb4377bf6b4-Accessing_held_shipmehts.png" alt="Accessing canceled shipments" />
    </Callout>
  </Tab>

  <Tab title="Hold via API">
    To hold shipment via our API, refer to the following endpoint

    <Cards>
      <Card title="Update Status" href="https://docs.intersoftsapient.net/reference/put_v4-shipments-status" icon="fa-solid fa-code">
        Complete API reference for shipment status updates including holding
      </Card>
    </Cards>
  </Tab>
</Tabs>

<br />

<br />

<br />

<Callout icon="💡" theme="default">
  ### _Tip_

  _You can delete the shipping account both via UI and the API. For more information on how to delete shipping accounts via API, refer to the [API References](https://docs.intersoftsapient.net/reference/delete_v4-shippingaccounts-carriercode-shippingaccountid) section._
</Callout>

To delete a shipping account in SAPIENT, follow the steps as explained in the following procedure.

1. On the **Home** page that opens, in the left navigation panel, select **Shipping Accounts**.

<Image align="center" alt="Accessing shipping accounts" border={true} caption="Accessing shipping accounts" src="https://files.readme.io/3e60281b3dfe72e1d825e37b48a9dbcb8a5446f083dc00aa30b8189f109e58dc-Shipping_account_option.png" />

3. On the **Shipping Accounts** page that opens, from the list of shipping accounts, select the account that you want to delete.
4. In the **View Shipping Account[account name]** page that opens, select ![](https://files.readme.io/af5c41de6009316deb4ab39f682b3be215f7a7673548911d06c333bc5ccf7606-Edit_shipping_account_button.png).

<Image align="center" alt="Selecting option to edit shipping account" border={true} caption="Selecting option to edit shipping account" src="https://files.readme.io/153a46ff1f4d9ffde3425fc25c9710c7b4a368c0f3f340a0f181b67b7b74a657-View_shipping_account_page.png" />

5. In the **Edit Shipping Account[account name]** form that opens, on the top right corner, select ![](https://files.readme.io/2b717367c6b8d33a03ad2eebc3a40edb38663cb47e41c7e3517289780460ef19-Delete_account_button.png).

<Image align="center" alt="Editing shipping account" border={true} caption="Deleting shipping account" src="https://files.readme.io/d0978d6da7df64866e6544071d90031fe5f91669b2cfc0eeef0fbd460c9a20b4-Deleting_shipping_account.png" />

6. In the confirmation dialog that appears, select **Yes** to confirm your action.

<Image align="center" alt="Confirming account deletion" border={true} caption="Confirming account deletion" src="https://files.readme.io/914ca92582b92600a9af9e9237ab6669e325795bab18d4de668c666d6d420606-Confirming_account_deletion.png" width="400px" />

Once confirmed, the shipping account is deleted successfully and no longer displays in the **Shipping Accounts** list.

## See also

* [Add shipping account](https://docs.intersoftsapient.net/docs/add-a-shipping-account)
