---
title: Add Shipping Account
excerpt: >-
  A _shipping account_ is a specific account set up with a shipping carrier or
  logistics provider that enables businesses to manage shipping activities.
deprecated: false
hidden: false
icon: fad fa-square-plus
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
In SAPIENT, you can create a <Glossary>shipping account</Glossary>, assign your <Glossary>carrier</Glossary> credentials to it, and then link them to the relevant <Glossary>shipping location</Glossary>(s).

<Callout icon="📘" theme="info">
  ### _Note_

  _Users with the_**_Admin_**_&#x20;role permissions can create unlimited shipping accounts for their customers._
</Callout>

## How to add shipping account

<Tabs>
  <Tab title="Add via SAPIENT UI">
    

    To add a shipping account in SAPIENT, perform the steps as explained in the following procedure.

    <ToggleList>
      <ToggleListItem title={<strong>1. Access the shipping accounts page</strong>} icon="fa-rocket">
        <br />

        In the left navigation panel, select **Shipping Accounts**.

        <Image align="center" border={true} src="https://files.readme.io/3e60281b3dfe72e1d825e37b48a9dbcb8a5446f083dc00aa30b8189f109e58dc-Shipping_account_option.png" caption="Accessing shipping accounts" />

        ***
      </ToggleListItem>

      <br />

      <ToggleListItem title={<strong>2. Select the add shipping account button</strong>} icon="fa-rocket">
        <br />

        On the **Shipping Accounts** page that opens, select the **Add Shipping Account** button.

        <Image align="center" border={true} src="https://files.readme.io/8490d8ba65c4eca10caa8c051c5e73bf366fc5a6269e84a2bfb697544105b343-Add_shipping_account_option.png" caption="Accessing option to add shipping account" />

        ***
      </ToggleListItem>

      <br />

      <ToggleListItem title={<strong>3. Enter account details </strong>} icon="fa-rocket">
        <br />

        On the **Add Shipping Account** form that appears, fill in the **ACCOUNT DETAILS** block:

        <Image align="center" border={true} src="https://files.readme.io/dc5c99c4576f2625aa7809d67c9cf26573ed44dbce51fdebc2df7f43013cde3b-Account_details_block.png" caption="Entering account details" />

        <br />

        <Callout icon="💡" theme="default">
          ### *Tip*

          *In the following table, the mandatory fields are marked with an asterisk (\*).*
        </Callout>

        | Element                 | Description                                                                                                   |
        | ----------------------- | ------------------------------------------------------------------------------------------------------------- |
        | **Carrier**\*           | From the dropdown list, select the carrier for which you want to add a shipping account.                      |
        | **Shipping Location**\* | From the dropdown menu, select the location that you want to assign to the shipping account you are creating. |

        ***
      </ToggleListItem>

      <br />

      <ToggleListItem title={<strong>4. Enter shipping account details </strong>} icon="fa-rocket">
        <br />

        In the **SHIPPING ACCOUNT** block, enter the necessary information:

        <Image align="center" border={true} src="https://files.readme.io/86c792139df738b9d3d72e61e3a2d9edf6e95e49ebaed402137335a66e796d4a-Shipping_account_block.png" width="400px" caption="Specifying shipping account details" />

        <br />

        <Callout icon="💡" theme="default">
          ### *Tip*

          *In the following table, the mandatory fields are marked with an asterisk (\*).*
        </Callout>

        | Element                         | Description                                                                                                                                                                                      |
        | ------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
        | **Carrier Account Number**\*    | Enter the carrier account number. The format must be compliant with your selected carrier. Add leading zeros if needed to meet character length requirements                                     |
        | **Account Type**\*              | Select either [Production](https://docs.intersoftsapient.net/docs/sandbox-account) (live environment) or [Sandbox](https://docs.intersoftsapient.net/docs/sandbox-account) (testing environment) |
        | **Account Name**\*              | Enter the account name if different from customer name                                                                                                                                           |
        | **Registered Email Address**\*  | Enter the email address used to register with the carrier                                                                                                                                        |
        | **Registered Billing Postcode** | Enter the postcode for billing.<br /> `Note`: *If you are unsure of the postcode, use the one shown on your invoice.*                                                                            |

        ### Contact Information

        | Element              | Description                                                                          |
        | -------------------- | ------------------------------------------------------------------------------------ |
        | **Alias**\*          | Enter a memorable custom name for API requests instead of using shipping location ID |
        | **Contact Name**\*   | Enter the primary contact name for this account                                      |
        | **Contact Number**\* | Enter the contact phone number for this account                                      |

        ***
      </ToggleListItem>

      <br />

      <ToggleListItem title={<strong>5. Enter carrier-specific details</strong>} icon="fa-rocket">
        <br />

        In the **CARRIER DETAILS** block, complete the carrier-specific fields.

        > 🚧 *Important*
        >
        > *The fields in this section vary depending on your selected carrier. Each carrier has unique requirements and authentication methods. To get more information on how to fill the fields in this block, refer to the [carrier specific guides](https://docs.intersoftsapient.net/v4.04/docs/carrier-specific-user-guides) section.*

        <br />

        After entering all the required information, select ![](https://files.readme.io/c8e36ac323cf6d3859bfa7081ee7ab63495ded4fd04cdb97aa685e06071cf4b4-add_shipping_account_button_2.png).
      </ToggleListItem>
    </ToggleList>
  </Tab>

  <Tab title="Add via API">
    To add a shipping account via our API, refer to the following endpoint:

    <Cards>
      <Card title="Add Account" href="https://docs.intersoftsapient.net/reference/post_v4-shippingaccounts-rm" icon="fa-solid fa-code">
        Complete API reference for adding shipping account
      </Card>
    </Cards>
  </Tab>
</Tabs>

***

## Next steps

<Accordion title="What's Next?">
  Once you've successfully added your shipping account, you can:

  * [Add a shipping location](https://docs.intersoftsapient.net/docs/add-a-shipping-location) to your new shipping account
  * Configure additional carrier settings
  * Test your account in the sandbox environment before going live
</Accordion>

<br />