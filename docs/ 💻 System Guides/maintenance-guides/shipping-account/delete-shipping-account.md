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

## How to delete shipping account

<Tabs>
  <Tab title="Delete via SAPIENT UI">
    To delete a shipping account in SAPIENT, perform the steps as explained in the following procedure.

    <ToggleList>
      <ToggleListItem title={<strong>1. Access the shipping accounts page</strong>} icon="fa-rocket">
        <br />

        On the **Home** page that opens, in the left navigation panel, select **Shipping Accounts**.

        <Image align="center" border={true} src="https://files.readme.io/3e60281b3dfe72e1d825e37b48a9dbcb8a5446f083dc00aa30b8189f109e58dc-Shipping_account_option.png" caption="Accessing shipping accounts" />

        ***
      </ToggleListItem>

      <br />

      <ToggleListItem title={<strong>2. Select the shipping account to edit</strong>} icon="fa-rocket">
        <br />

        On the **Shipping Accounts** page that opens, from the list of shipping accounts, select the account that you want to delete.

        ***
      </ToggleListItem>

      <br />

      <ToggleListItem title={<strong>3. View shipping account details </strong>} icon="fa-rocket">
        <br />

        In the **View Shipping Account\[account name]** page that opens, select ![alt text](https://files.readme.io/af5c41de6009316deb4ab39f682b3be215f7a7673548911d06c333bc5ccf7606-Edit_shipping_account_button.png).

        <Image align="center" border={true} src="https://files.readme.io/d81e673f87f261d6b098f8e062f8580297676b82eabd667fbb8a2df03beffd37-Edit_shipping_account_option.png" caption="Selecting option to edit shipping account" />

        ***
      </ToggleListItem>

      <br />

      <ToggleListItem title={<strong>4. Delete shipping account </strong>} icon="fa-rocket">
        <br />

        In the **Edit Shipping Account\[account name]** form that opens, on the top right corner, select ![alt text](https://files.readme.io/2b717367c6b8d33a03ad2eebc3a40edb38663cb47e41c7e3517289780460ef19-Delete_account_button.png).

        <Image align="center" border={true} src="https://files.readme.io/d0978d6da7df64866e6544071d90031fe5f91669b2cfc0eeef0fbd460c9a20b4-Deleting_shipping_account.png" caption="Deleting shipping account" />

        <br />

        ***
      </ToggleListItem>

      <br />

      <ToggleListItem title={<strong>5. Confirm your action </strong>} icon="fa-rocket">
        <br />

        In the confirmation dialog that appears, select **Yes** to confirm your action.

        <Image align="center" border={true} src="https://files.readme.io/914ca92582b92600a9af9e9237ab6669e325795bab18d4de668c666d6d420606-Confirming_account_deletion.png" width="400px" caption="Confirming account deletion" />

        <br />

        Once confirmed, the shipping account is deleted successfully and no longer displays in the **Shipping Accounts** list.

        <br />

        ***
      </ToggleListItem>
    </ToggleList>
  </Tab>

  <Tab title="Delete via API">
    To delete a shipping account via our API, refer to the following endpoint:

    <Cards columns="2">
      <Card title="Delete Account" href="https://docs.intersoftsapient.net/reference/delete_v4-shippingaccounts-carriercode-shippingaccountid#/" icon="fa-solid fa-code" target="_blank">
        Complete API reference for deleting shipping account
      </Card>
    </Cards>
  </Tab>
</Tabs>

***

### See also

<Cards columns="2">
  <Card title="Add shipping account" href="https://docs.intersoftsapient.net/docs/add-a-shipping-account" icon="fa-solid fa-plus" target="_blank">
    Learn how to create a new shipping account in SAPIENT
  </Card>
</Cards>
