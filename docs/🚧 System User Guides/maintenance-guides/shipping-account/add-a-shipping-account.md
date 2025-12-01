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
In SAPIENT, you can create a shipping account, assign your <Glossary>carrier</Glossary> credentials to it, and then link them to the relevant <Glossary>shipping location</Glossary>(s).

> 📘 _Note_
>
> _Users with the**Admin** role permissions can create unlimited shipping accounts for their customers._

<br />

<Tabs>
  <Tab title="Add via SAPIENT UI">
    <br />

    To add a shipping account in SAPIENT, perform the steps as explained in the following procedure.

    <ToggleList>
      <ToggleListItem title={<strong>1. Access the shipping accounts page</strong>} icon="fa-rocket">
        <br />

        In the left navigation panel, select **Shipping Accounts**.

    <Image align="center" border={true} src="https://files.readme.io/3e60281b3dfe72e1d825e37b48a9dbcb8a5446f083dc00aa30b8189f109e58dc-Shipping_account_option.png" alt="Accessing shipping accounts" />

        ***
      </ToggleListItem>

      <br />

      <ToggleListItem title={<strong>2. Select the add shipping account button</strong>} icon="fa-rocket">
        <br />

 On the **Shipping Accounts** page that opens, select the **Add Shipping Account** button.
<br></br>
        <Image align="center" border={true} src="https://files.readme.io/8490d8ba65c4eca10caa8c051c5e73bf366fc5a6269e84a2bfb697544105b343-Add_shipping_account_option.png" alt="Accessing option to add shipping account" />
***
      </ToggleListItem>

      <br />

      <ToggleListItem title={<strong>3. Enter account details </strong>} icon="fa-rocket">
        <br />

 On the **Add Shipping Account** form that appears, fill in the **ACCOUNT DETAILS** block:

    <Image align="center" border={true} src="https://files.readme.io/dc5c99c4576f2625aa7809d67c9cf26573ed44dbce51fdebc2df7f43013cde3b-Account_details_block.png" alt="Entering account details" />

    ### Required Fields

    | Element                 | Description                                                                                                  |
    | ----------------------- | ------------------------------------------------------------------------------------------------------------ |
    | **Carrier**\*           | From the dropdown list, select the carrier for which you want to add a shipping account                      |
    | **Shipping Location**\* | From the dropdown menu, select the location that you want to assign to the shipping account you are creating |

    *Required fields are marked with an asterisk (*)

        ***
      </ToggleListItem>

      <br />

      <ToggleListItem title={<strong>4. Enter shipping account details </strong>} icon="fa-rocket">
        <br />

        In the **SHIPPING ACCOUNT** block, enter the necessary information:

    <Image align="center" border={true} src="https://files.readme.io/86c792139df738b9d3d72e61e3a2d9edf6e95e49ebaed402137335a66e796d4a-Shipping_account_block.png" width="400px" alt="Specifying shipping account details" />

    <Accordion title="Shipping Account Fields" icon="list">
      ### Account Configuration

      | Element                         | Description                                                                                                                                                  |
      | ------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------ |
      | **Carrier Account Number**\*    | Enter the carrier account number. The format must be compliant with your selected carrier. Add leading zeros if needed to meet character length requirements |
      | **Account Type**\*              | Select either **Production** (live environment) or **Sandbox** (testing environment)                                                                         |
      | **Account Name**\*              | Enter the account name if different from customer name                                                                                                       |
      | **Registered Email Address**\*  | Enter the email address used to register with the carrier                                                                                                    |
      | **Registered Billing Postcode** | Enter the postcode for billing (optional)                                                                                                                    |

      ### Contact Information

      | Element              | Description                                                                          |
      | -------------------- | ------------------------------------------------------------------------------------ |
      | **Alias**\*          | Enter a memorable custom name for API requests instead of using shipping location ID |
      | **Contact Name**\*   | Enter the primary contact name for this account                                      |
      | **Contact Number**\* | Enter the contact phone number for this account                                      |

      *Required fields are marked with an asterisk (*)
    </Accordion>

        ***
      </ToggleListItem>

      <br />

      <ToggleListItem title={<strong>5. Enter carrier-specific details</strong>} icon="fa-rocket">
        <br />

        In the **CARRIER DETAILS** block, complete the carrier-specific fields.

    <Callout icon="💡" theme="info">
      **Important**: The fields in this section vary depending on your selected carrier. Each carrier has unique requirements and authentication methods. To get more information on how to fill the fields in this block, refer to the [carrier specific guides](https://docs.intersoftsapient.net/docs/carrier-specific-user-guides) section.
        </Callout><br></br>
After entering all the required information, select ![](https://files.readme.io/c8e36ac323cf6d3859bfa7081ee7ab63495ded4fd04cdb97aa685e06071cf4b4-add_shipping_account_button_2.png).
        ***
      </ToggleListItem>
</ToggleList>
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

To create a shipping account in SAPIENT, follow the instructions as explained in the following procedure.

1. In the left navigation panel, select **Shipping Accounts**.

<Image align="center" alt="Accessing shipping accounts" border={true} caption="Accessing shipping accounts" src="https://files.readme.io/3e60281b3dfe72e1d825e37b48a9dbcb8a5446f083dc00aa30b8189f109e58dc-Shipping_account_option.png" />

2. On the **Shipping Accounts** page that opens, select ![](https://files.readme.io/0a2190f702c512528e9b264765a05e8b507cecbb379fd3fe390767ed8518382a-add_shipping_account_button.png).

<Image align="center" alt="Accessing option to add shipping account" border={true} caption="Selecting option to add shipping account" src="https://files.readme.io/8490d8ba65c4eca10caa8c051c5e73bf366fc5a6269e84a2bfb697544105b343-Add_shipping_account_option.png" />

3. On the **Add Shipping Account** form that appears, in the **ACCOUNT DETAILS** block, fill in the necessary information as described in the following tables.

<Image align="center" alt="Entering account details" border={true} caption="Entering account details" src="https://files.readme.io/dc5c99c4576f2625aa7809d67c9cf26573ed44dbce51fdebc2df7f43013cde3b-Account_details_block.png" />

<AsteridkForMandatoryElements />

|         Element        | Description                                                                                                                        |
| :--------------------: | :--------------------------------------------------------------------------------------------------------------------------------- |
|      **Carrier***      | From the dropdown list, select the carrier for which you want to add a shipping account.                                           |
| **Shipping Location*** | From the dropdown menu, select the location that you want to assign to the <Glossary>shipping account</Glossary> you are creating. |

4. In the **SHIPPING ACCOUNT** block, enter the necessary information as explained in the following table.

<Image align="center" alt="Specifying shipping account details" border={true} caption="Specifying shipping account details" src="https://files.readme.io/86c792139df738b9d3d72e61e3a2d9edf6e95e49ebaed402137335a66e796d4a-Shipping_account_block.png" width="400px" />

<Callout icon="💡" theme="default">
  ### _Tip_

  _In the following table, the mandatory fields are marked with an asterisk (*)._
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
        **Carrier Account Number***
      </td>

      <td>
        Enter the carrier account number.

        The format of the account number must be compliant with the carrier you have selected. If your account number does not meet the requirements, you may need to add the required amount of zero's at the beginning of the number to ensure it lies within the standard character length range for that carrier.
      </td>
    </tr>

    <tr>
      <td>
        **Account Type***
      </td>

      <td>
        From the dropdown menu, select one of the following account types that you want to set up for the the shipping account you are adding:

        • **[Production](https://docs.intersoftsapient.net/docs/sandbox-account)**: a live environment where the final version of the application is deployed and made available to the users.

        • **[Sandbox](https://docs.intersoftsapient.net/docs/sandbox-account)**: a testing environment that mimics the **Production** environment but is isolated from it. The sandbox environment is primarily used for development and testing purposes.
      </td>
    </tr>

    <tr>
      <td>
        **Account Name (if different than customer)***
      </td>

      <td>
        Enter the account name.
      </td>
    </tr>

    <tr>
      <td>
        **Registered Email Address***
      </td>

      <td>
        Enter the email address that was used to register the account for the carrier you selected.
      </td>
    </tr>

    <tr>
      <td>
        **Registered Billing Postcode**
      </td>

      <td>
        Enter the postcode registered with the carrier for receiving invoices.
      </td>
    </tr>

    <tr>
      <td>
        **Alias***
      </td>

      <td>
        Enter a custom name which can be used in the API request instead of using the shipping location ID when connecting to us. Therefore, it is recommend that this name must be memorable and available for reference purposes.
      </td>
    </tr>

    <tr>
      <td>
        **Contact Name***
      </td>

      <td>
        Enter the contact name for the account you are adding.
      </td>
    </tr>

    <tr>
      <td>
        **Contact Number***
      </td>

      <td>
        Enter the contact number for the account you are adding.
      </td>
    </tr>
  </tbody>
</Table>

5. In the **CARRIER DETAILS** block, the fields you see are carrier-specific and vary for each carrier. To get more information on how to fill the fields in this block, refer to the [carrier specific guides](https://docs.intersoftsapient.net/docs/carrier-specific-user-guides) section.
6. After entering all the required information, select ![](https://files.readme.io/c8e36ac323cf6d3859bfa7081ee7ab63495ded4fd04cdb97aa685e06071cf4b4-add_shipping_account_button_2.png).

Once done, you have now successfully added a shipping account. You can now [add a shipping location](https://docs.intersoftsapient.net/docs/add-a-shipping-location) to your new shipping account.

> 📘 _Note_
>
> _Shipping account(s) can be added and managed via API. For more information, refer to the [API References](https://docs.intersoftsapient.net/reference/get_v4-shippingaccounts) section._
