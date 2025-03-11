---
title: Add Royal Mail shipping account
excerpt: >-
  A _shipping account_ is a specific account set up with a shipping carrier or
  logistics provider that enables businesses to manage shipping activities.
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
In SAPIENT, you can create a shipping account with Royal Mail, assign your Royal Mail credentials to it, and then link it to the relevant <Glossary>shipping location</Glossary>(s).

> 🚧 *Important*
>
> *Before you can set up a shipping account, you must ensure you have[enabled the label integration](https://docs.intersoftsapient.net/docs/integration-activation) with Royal Mail.*

To add a shipping account for Royal Mail in SAPIENT, follow the instructions as explained in the following procedure.

1. Log in to the SAPIENT platform using your credentials.

<Image align="center" alt="Logging into SAPIENT" border={true} caption="Logging into SAPIENT" src="https://files.readme.io/fa5d0ced6ed38b419fa15c57f5b03fdddf6284adfcc85b48370c67d1aa07c5f8-Sapient_Login_window.png" width="500px" />

2. On the **Home** page that opens, in the left navigation panel, select **Shipping Accounts**.

<Image align="center" alt="Accessing shipping accounts" border={true} caption="Accessing shipping accounts" src="https://files.readme.io/3e60281b3dfe72e1d825e37b48a9dbcb8a5446f083dc00aa30b8189f109e58dc-Shipping_account_option.png" />

3. On the **Shipping Accounts** page that opens, select ![alt text](https://files.readme.io/44690bc0342682d80d45da0ca9e41920f4a8e30430a7279053ef6348e2900569-add_shipping_account_button.png).

<Image align="center" alt="Accessing option to add shipping account" border={true} caption="Selecting option to add shipping account" src="https://files.readme.io/6a8c9af67fce1cfe9d27b55871687460e467417da0f236b1fa0a7a622241a67d-RM_create_shiipping_accounts_option.png" />

4. On the **Add Shipping Account** form that appears, in the **ACCOUNT DETAILS** block, fill in the necessary information as described in the following table.

<Image align="center" alt="Entering account details" border={true} caption="Entering account details" src="https://files.readme.io/dc5c99c4576f2625aa7809d67c9cf26573ed44dbce51fdebc2df7f43013cde3b-Account_details_block.png" />

<AsteridkForMandatoryElements />

|         Element         | Description                                                                                                   |
| :---------------------: | :------------------------------------------------------------------------------------------------------------ |
|      **Carrier\***      | From the dropdown list, select **RM - Royal Mail**.                                                           |
| **Shipping Location\*** | From the dropdown menu, select the location that you want to assign to the shipping account you are creating. |

5. In the **SHIPPING ACCOUNT** block, enter the necessary information as explained in the following table.

<Image align="center" alt="Specifying shipping account details" border={true} caption="Specifying shipping account details" src="https://files.readme.io/86c792139df738b9d3d72e61e3a2d9edf6e95e49ebaed402137335a66e796d4a-Shipping_account_block.png" width="400px" />

> 💡 *Tip*
>
> *In the following table, the mandatory fields are marked with an asterisk (\*).*

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
        **Carrier Account Number\***
      </td>

      <td>
        Enter a ten digit account number. This must be a ten digit number. If your account number is shorter than this, then you need to add the required amount of zero's at the beginning of the number to ensure it is ten digits long.

        The format of the account number must be compliant with the carrier you have selected. If your account number does not meet the requirements, you may need to add the required amount of zero's at the beginning of the number to ensure it is ten digit long.
      </td>
    </tr>

    <tr>
      <td>
        **Account Type\***
      </td>

      <td>
        From the dropdown menu, select one of the following account types that you want to set up for the the shipping account you are adding:

        • **[Production](https://docs.intersoftsapient.net/docs/sandbox-account)**: a live environment where the final version of the application is deployed and made available to the users.

        • **[Sandbox](https://docs.intersoftsapient.net/docs/sandbox-account)**: a testing environment that mimics the **Production** environment but is isolated from it. The sandbox environment is primarily used for development and testing purposes.

        ***Note**: For testing purposes, you can set up a **Sandbox** account for Royal Mail by using a dummy account number and PLN as this data is not validated and allows you to test the integration. If you choose to switch the account to **Production**, then the account details are sent to the <Glossary>Online Business Account</Glossary> (OBA) team and validated. Based on this validation, the shipping account is either approved or rejected.*
      </td>
    </tr>

    <tr>
      <td>
        **Account Name (if different than customer)\***
      </td>

      <td>
        Enter the name of the account you are adding.
      </td>
    </tr>

    <tr>
      <td>
        **Registered Email Address\***
      </td>

      <td>
        Enter the email address that was used to register the Royal Mail online business account (OBA).

        For more information on OBA, refer to the [Set up Royal Mail OBA account](https://docs.intersoftsapient.net/docs/oba-email-validation) section.
      </td>
    </tr>

    <tr>
      <td>
        **Registered Billing Postcode**
      </td>

      <td>
        Enter the postcode registered with Royal Mail for receiving invoices.
      </td>
    </tr>

    <tr>
      <td>
        **Alias\***
      </td>

      <td>
        Enter a custom name which can be used in the API request instead of using the shipping account ID when connecting to us. Therefore, it is recommended that this name must be memorable and available for reference purposes.
      </td>
    </tr>

    <tr>
      <td>
        **Contact Name\***
      </td>

      <td>
        Enter the contact name for the account you are adding.
      </td>
    </tr>

    <tr>
      <td>
        **Contact Number\***
      </td>

      <td>
        Enter the contact number for the account you are adding.
      </td>
    </tr>
  </tbody>
</Table>

6. In the **CARRIER DETAILS** block, enter the necessary information as explained in the following table.

<Image align="center" alt="Entering carrier details" border={true} caption="Entering carrier details" src="https://files.readme.io/0ca47335dbea534cb7d1b4ddce82c5eef9de68c4e17ac2c7169d6b82f3738835-carrier_details_block.png" width="400px" />

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
        **Posting Location Code\***
      </td>

      <td>
        This is a Royal Mail specific code given for each location you are despatching shipments from.

        This must be a 10 digit number that always starts with 9000. For example, 9000257150.
      </td>
    </tr>

    <tr>
      <td>
        **Receiving Hub Code\***
      </td>

      <td>
        Enter the code allocated by Royal Mail for the receiving Hub to where your goods will be taken.

        The **Receiving Hub Code** is automatically populated based on the postcode of the shipping location to which you are linking this account.
      </td>
    </tr>

    <tr>
      <td>
        **OBA Access Code**
      </td>

      <td>
        This field is autopopulated by INTERSOFT and is something we communicate directly with the carrier after the shipping account has been added.
      </td>
    </tr>
  </tbody>
</Table>

7. After entering all the required information, select ![alt text](https://files.readme.io/db03c9a2b7ee816f42db617829469dce01bbdfd35aca00ace480fd78db31aa11-add_shipping_account_button_2.png).

Once done, you have now successfully added a shipping account. You can now [add a shipping location](https://docs.intersoftsapient.net/docs/add-a-shipping-location) to your new shipping account.

> 📘 *Note*
>
> *Shipping account(s) can be added and managed via API. For more information, refer to the[API References](https://docs.intersoftsapient.net/reference/get_v4-shippingaccounts) section.*

### See also

* [Edit shipping account](https://docs.intersoftsapient.net/docs/edit-shipping-account)