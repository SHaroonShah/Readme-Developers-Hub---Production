---
title: Add EVRi shipping account
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
  pages:
    - type: basic
      slug: client-id-and-child-clinet-id-management-1
      title: Client Id and Child Clinet Id management
    - type: basic
      slug: tracking-account-setup
      title: Tracking account setup
---
In SAPIENT, you can create an EVRi shipping account by selecting your desired <Glossary>shipping location</Glossary>,  entering the corresponding account and carrier details, and then adding the account to the system.

Unlike other carriers, EVRi customers can have a main (parent) shipping account and may choose to have multiple sub-accounts under the main account. For example, if the customers want to ship multiple different brands.

> 🚧 _Important_
>
> _Before you can set up a shipping account, make sure you have[enabled the label integration](https://docs.intersoftsapient.net/docs/integration-activation) with EVRi._

## How to add EVRi shipping account

To add a parent shipping account for EVRi in SAPIENT, follow the instructions as explained in the following procedure.

<Tabs>
  <Tab title="Via SAPIENT UI">
    <ToggleList>
      <ToggleListItem title="1. Select the Shipping Accounts page">
        In the left navigation panel, select **Shipping Accounts**.

        <Image align="center" border={true} src="https://files.readme.io/3e60281b3dfe72e1d825e37b48a9dbcb8a5446f083dc00aa30b8189f109e58dc-Shipping_account_option.png" alt="Accessing shipping accounts" />

        ***
      </ToggleListItem>

      <br />

      <ToggleListItem title="2. Select option to add shipping account">
        On the **Shipping Accounts** page that opens, select ![](https://files.readme.io/4dc0470535418171d8c974546d130f04a0fc60a878c7f7648b2da21309450830-add_shipping_account_button.png).

        <Image align="center" border={true} src="https://files.readme.io/93a0d9cc66a38e49c4bcffc89b73c11a567a5b518b19eac7ae22c7e39063c1b1-Add_shipping_account_button_EVRi.png" alt="Accessing option to add shipping account" />

        ***
      </ToggleListItem>

      <br />

      <ToggleListItem title="3. Enter account details">
        On the **Add Shipping Account** form that appears, in the **ACCOUNT DETAILS** block, fill in the necessary information as described in the following table.

        <Image align="center" border={true} src="https://files.readme.io/43991905bc228df5a0737e883ebcf6125535727cdb622711887e427c375d6763-Account_details_block_EVRi.png" alt="Entering account details" />

        <br />

        <AsteridkForMandatoryElements />

        |         Element         | Description                                                                                                                                 |
        | :---------------------: | :------------------------------------------------------------------------------------------------------------------------------------------ |
        |      **Carrier**\*      | From the dropdown list, select **EVRI - EVRi**.                                                                                             |
        | **Shipping Location**\* | From the dropdown menu, select the <Glossary>shipping location</Glossary> that you want to assign to the shipping account you are creating. |

        ***
      </ToggleListItem>

      <br />

      <ToggleListItem title="4. Enter shipping account details">
        In the **SHIPPING ACCOUNT** block, enter the necessary information as explained in the following table.

        <Image align="center" border={true} src="https://files.readme.io/9546c2ab0f9d76d0ac27f5b028e0be8c38f7ac52f6b46cc177ceefdb63a32de5-Shipping_account_block_EVRi.png" width="400px" alt="Specifying shipping account details" />

        <br />

        <Callout icon="💡" theme="default">
          ### *Tip*

          *In the following table, the mandatory fields are marked with an asterisk (\*).*
        </Callout>

        <Table align={["center","left"]}>
          <thead>
            <tr>
              <th>
                Element
              </th>

              <th>
                Description
              </th>
            </tr>
          </thead>

          <tbody>
            <tr>
              <td>
                **Carrier Account Number**\*
              </td>

              <td>
                Enter the account number for EVRi. This can also be known as your EVRi ClientID.
              </td>
            </tr>

            <tr>
              <td>
                **Account Name (if different than customer)**\*
              </td>

              <td>
                Enter the name of the account you are adding. This can also be known as your EVRi Client Name.
              </td>
            </tr>

            <tr>
              <td>
                **Account Type**\*
              </td>

              <td>
                From the dropdown menu, select one of the following account types that you want to set up for the the shipping account you are adding:

                • **[Production](https://docs.intersoftsapient.net/docs/sandbox-account)**: a live environment where the final version of the application is deployed and made available to the users.

                • **[Sandbox](https://docs.intersoftsapient.net/docs/sandbox-account)**: a testing environment that mimics the **Production** environment but is isolated from it. The sandbox environment is primarily used for development and testing purposes.
              </td>
            </tr>

            <tr>
              <td>
                **Alias**\*
              </td>

              <td>
                Enter a custom name which can be used in the API request instead of using the shipping account ID when connecting to us. Therefore, it is recommended that this name must be memorable and available for reference purposes.
              </td>
            </tr>

            <tr>
              <td>
                **Contact Name**\*
              </td>

              <td>
                Enter the contact name for the account you are adding.
              </td>
            </tr>

            <tr>
              <td>
                **Contact Number**\*
              </td>

              <td>
                Enter the contact number for the account you are adding.
              </td>
            </tr>
          </tbody>
        </Table>

        ***
      </ToggleListItem>

      <br />

      <ToggleListItem title="5. Enter carrier details">
        In the **CARRIER DETAILS** block, enter the necessary information as explained in the following table.

        <Image align="center" border={true} src="https://files.readme.io/60e2321138104b3b4c2a28966427ea131d2d4a8fb8a5dc283362a9ded6220585-carrier_details_block_EVRi.png" width="400px" alt="Entering carrier details" />

        <br />

        <AsteridkForMandatoryElements />

        <Table align={["center","left"]}>
          <thead>
            <tr>
              <th>
                Element
              </th>

              <th>
                Description
              </th>
            </tr>
          </thead>

          <tbody>
            <tr>
              <td>
                **Username**\*
              </td>

              <td>
                Enter your username (EVRi API credentials) These are received via email from EVRi's IT integration team for both the **Test** (SIT) and **Production** (Prod) environment.

                *`Note`: If you have chosen**Sandbox** in the **Account Type** field of the **SHIPPING ACCOUNT** block, then enter your SIT credentials and if you have chosen **Production** in the **Account Type** field of the **SHIPPING ACCOUNT** block, then enter your Prod credentials.*
              </td>
            </tr>

            <tr>
              <td>
                **Password**\*
              </td>

              <td>
                Enter the password for the username you have entered. This is received via email from EVRi's IT Integration team for both the **Test** (SIT) and **Production** (Prod) environment.
              </td>
            </tr>

            <tr>
              <td>
                **SMS Alert Group Code**
              </td>

              <td>
                Enter the alert group code that is allocated to you by EVRi.

                This feature is only required if you wish to use the SMS notification enhancement.
              </td>
            </tr>
          </tbody>
        </Table>

        ***
      </ToggleListItem>

      <br />

      <ToggleListItem title="6. Save and add the shipping account">
        After entering all the required information, select ![](https://files.readme.io/99e4e322c6a3f874e0258a73646a551aa2120d8d359b2ce5d09a4cf0eabcd44a-add_shipping_account_button_2.png). <br />
        Once done, you have now successfully added a shipping account. You can now start shipping with it.
      </ToggleListItem>
    </ToggleList>
  </Tab>

  <Tab title="Via API">
    <Cards>
      <Card title="Add Account" href="https://docs.intersoftsapient.net/reference/post_v4-shippingaccounts-dpduk" icon="fa-code">
        Add and manage DPD UK shipping account via API.
      </Card>
    </Cards>
  </Tab>
</Tabs>

***

### See also

* [Edit shipping account](https://docs.intersoftsapient.net/docs/edit-shipping-account)
