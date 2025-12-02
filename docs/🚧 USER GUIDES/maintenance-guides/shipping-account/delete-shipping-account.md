---
title: Delete shipping account
excerpt: >-
  Learn how to delete shipping accounts in SAPIENT through the UI with
  step-by-step instructions, including when deletion is necessary and API
  alternatives.
deprecated: false
hidden: false
icon: fad fa-circle-trash
link:
  new_tab: false
metadata:
  title: ''
  description: ''
  robots: index
---
Deleting the <Glossary>shipping account</Glossary> that is no longer required is quite handy in certain situations, for example, if an account was set up incorrectly or is causing issues, deleting it can clear up any confusion and prevent operational problems or removing obsolete data that could complicate integration processes with external APIs or systems.

> 💡 *Tip*
>
> *You can delete the shipping account both via UI and the API. For more information on how to delete shipping accounts via API, refer to the [API References](https://docs.intersoftsapient.net/reference/delete_v4-shippingaccounts-carriercode-shippingaccountid) section.*

## Deletion Methods

<Tabs>
  <Tab title="UI Method">
    <Accordion title="Step-by-step procedure" icon="list-ol">
      To delete a shipping account in SAPIENT, follow the steps as explained in the following procedure.

      1. On the **Home** page that opens, in the left navigation panel, select **Shipping Accounts**.

      <Image align="center" alt="Accessing shipping accounts" border={true} caption="Accessing shipping accounts" src="https://files.readme.io/3e60281b3dfe72e1d825e37b48a9dbcb8a5446f083dc00aa30b8189f109e58dc-Shipping_account_option.png" />

      2. On the **Shipping Accounts** page that opens, from the list of shipping accounts, select the account that you want to delete.

      3. In the **View Shipping Account\[account name]** page that opens, select ![alt text](https://files.readme.io/af5c41de6009316deb4ab39f682b3be215f7a7673548911d06c333bc5ccf7606-Edit_shipping_account_button.png).

      <Image align="center" alt="Selecting option to edit shipping account" border={true} caption="Selecting option to edit shipping account" src="https://files.readme.io/153a46ff1f4d9ffde3425fc25c9710c7b4a368c0f3f340a0f181b67b7b74a657-View_shipping_account_page.png" />

      4. In the **Edit Shipping Account\[account name]** form that opens, on the top right corner, select ![alt text](https://files.readme.io/2b717367c6b8d33a03ad2eebc3a40edb38663cb47e41c7e3517289780460ef19-Delete_account_button.png).

      <Image align="center" alt="Editing shipping account" border={true} caption="Deleting shipping account" src="https://files.readme.io/d0978d6da7df64866e6544071d90031fe5f91669b2cfc0eeef0fbd460c9a20b4-Deleting_shipping_account.png" />

      5. In the confirmation dialog that appears, select **Yes** to confirm your action.

      <Image align="center" alt="Confirming account deletion" border={true} caption="Confirming account deletion" src="https://files.readme.io/914ca92582b92600a9af9e9237ab6669e325795bab18d4de668c666d6d420606-Confirming_account_deletion.png" width="400px" />

      Once confirmed, the shipping account is deleted successfully and no longer displays in the **Shipping Accounts** list.
    </Accordion>
  </Tab>
  <Tab title="API Method">
    For programmatic deletion of shipping accounts, use the SAPIENT API. This method is ideal for:
    - Bulk operations
    - Automated workflows
    - Integration with external systems

    **API Endpoint:** `DELETE /v4/shippingaccounts/{carrierCode}/{shippingAccountId}`

    For detailed API documentation and examples, refer to the [API References](https://docs.intersoftsapient.net/reference/delete_v4-shippingaccounts-carriercode-shippingaccountid).
  </Tab>
</Tabs>

## Related Topics

<Cards columns={2}>
  <Card title="Add shipping account" href="https://docs.intersoftsapient.net/docs/add-a-shipping-account" icon="plus">
    Learn how to create new shipping accounts in SAPIENT
  </Card>
  <Card title="API Reference" href="https://docs.intersoftsapient.net/reference/delete_v4-shippingaccounts-carriercode-shippingaccountid" icon="code">
    Complete API documentation for shipping account deletion
  </Card>
</Cards>