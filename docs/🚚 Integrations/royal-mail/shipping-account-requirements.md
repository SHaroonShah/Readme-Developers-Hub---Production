---
title: Add Royal Mail shipping account
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
In SAPIENT, you can create a Royal Mail shipping account by selecting your desired <Glossary>shipping location</Glossary>,  entering the corresponding account and carrier details, and then adding the account to the system.

<Callout icon="🚧" theme="warn">
  ### _Important_

  _Before you can set up a shipping account, you must ensure you have [enabled the label integration](https://docs.intersoftsapient.net/docs/integration-activation) with Royal Mail and have already [created a shipping location](https://docs.intersoftsapient.net/docs/add-a-shipping-location)._
</Callout>

## How to Add Royal Mail shipping account

<Tabs>
  <Tab title="Via SAPIENT UI">
    To add a shipping account for Royal Mail in SAPIENT, follow the instructions as explained in the following procedure.

      <ToggleListItem title="1. Navigate to shipping accounts" icon="fa-truck">
        <br />

        On the **Home** page, in the left navigation panel, select **Shipping Accounts**.

        <Image align="center" border={true} src="https://files.readme.io/3e60281b3dfe72e1d825e37b48a9dbcb8a5446f083dc00aa30b8189f109e58dc-Shipping_account_option.png" caption="Accessing shipping accounts" />

        ***
      </ToggleListItem>

      <ToggleListItem title="2. Select the Add Shipping Account button" icon="fa-plus-circle">
        <br />

        On the **Shipping Accounts** page, select ![](https://files.readme.io/44690bc0342682d80d45da0ca9e41920f4a8e30430a7279053ef6348e2900569-add_shipping_account_button.png).

        <Image align="center" border={true} src="https://files.readme.io/6a8c9af67fce1cfe9d27b55871687460e467417da0f236b1fa0a7a622241a67d-RM_create_shiipping_accounts_option.png" caption="Accessing option to add shipping account" />

        ***
      </ToggleListItem>

      <ToggleListItem title="3. Enter account details" icon="fa-id-card">
        <br />

        On the **Add Shipping Account** form, in the **ACCOUNT DETAILS** block, fill in the information described in the following table.

        <Image align="center" border={true} src="https://files.readme.io/dc5c99c4576f2625aa7809d67c9cf26573ed44dbce51fdebc2df7f43013cde3b-Account_details_block.png" caption="Entering account details" />
        <br />

        <AsteridkForMandatoryElements />

        |         Element         | Description                                                                                                   |
        | :---------------------: | :------------------------------------------------------------------------------------------------------------ |
        |      **Carrier**\*      | From the dropdown list, select **RM - Royal Mail**.                                                           |
        | **Shipping Location**\* | From the dropdown menu, select the location that you want to assign to the shipping account you are creating. |

        ***
      </ToggleListItem>

      <ToggleListItem title="4. Enter shipping account details" icon="fa-file-alt">
        <br />

        In the **SHIPPING ACCOUNT** block, enter the necessary information as explained in the following table.

        <Image align="center" border={true} src="https://files.readme.io/86c792139df738b9d3d72e61e3a2d9edf6e95e49ebaed402137335a66e796d4a-Shipping_account_block.png" width="400px" caption="Specifying shipping account details" />

        <Callout icon="💡" theme="default">
          ### *Tip*

          *In the following table, the mandatory fields are marked with an asterisk (\*).*
        </Callout>

        <table>
          <thead>
            <tr>
              <th>Element</th>
              <th>Description</th>
            </tr>
          </thead>
          <tbody>
            <tr>
              <td><strong>Carrier Account Number</strong>&#42;</td>
              <td>
                Enter a ten digit account number. This must be a ten digit number. If your account number is shorter than this, then you need to add the required amount of zero's at the beginning of the number to ensure it is ten digits long.
                <br />
                <br />
                The format of the account number must be compliant with the carrier you have selected. If your account number does not meet the requirements, you may need to add the required amount of zero's at the beginning of the number to ensure it is ten digit long.
              </td>
            </tr>
            <tr>
              <td><strong>Account Type</strong>&#42;</td>
              <td>
                <p>From the dropdown menu, select one of the following account types that you want to set up for the the shipping account you are adding:</p>
                <ul>
                  <li><strong>Production</strong>: a live environment where the final version of the application is deployed and made available to the users.</li>
                  <li><strong>Sandbox</strong>: a testing environment that mimics the <strong>Production</strong> environment but is isolated from it. The sandbox environment is primarily used for development and testing purposes.</li>
                </ul>
                <em><code>Note</code>: For testing purposes, you can set up a <strong>Sandbox</strong> account for Royal Mail by using a dummy account number and PLN as this data is not validated and allows you to test the integration. If you choose to switch the account to <strong>Production</strong>, then the account details are sent to the Online Business Account (OBA) team and validated. Based on this validation, the shipping account is either approved or rejected.</em>
              </td>
            </tr>
            <tr>
              <td><strong>Account Name (if different than customer)</strong>&#42;</td>
              <td>Enter the name of the account you are adding.</td>
            </tr>
            <tr>
              <td><strong>Registered Email Address</strong>&#42;</td>
              <td>
                Enter the email address that was used to register the Royal Mail online business account (OBA).
                <br />
                <br />
                For more information on OBA, refer to the <a href="https://docs.intersoftsapient.net/docs/oba-email-validation">Set up Royal Mail OBA account</a> section.
              </td>
            </tr>
            <tr>
              <td><strong>Registered Billing Postcode</strong></td>
              <td>
                Enter the postcode registered with Royal Mail for receiving invoices.
                <br />
                <br />
                <em><code>Note</code>: If you are unsure of the postcode, use the one shown on your invoice.</em>
              </td>
            </tr>
            <tr>
              <td><strong>Alias</strong>&#42;</td>
              <td>Enter a custom name which can be used in the API request instead of using the shipping account ID when connecting to us. Therefore, it is recommended that this name must be memorable and available for reference purposes.</td>
            </tr>
            <tr>
              <td><strong>Contact Name</strong>&#42;</td>
              <td>Enter the contact name for the account you are adding.</td>
            </tr>
            <tr>
              <td><strong>Contact Number</strong>&#42;</td>
              <td>Enter the contact number for the account you are adding.</td>
            </tr>
          </tbody>
        </table>

        ***
      </ToggleListItem>

      <ToggleListItem title="5. Enter carrier details" icon="fa-building">
        <br />

        In the **CARRIER DETAILS** block, enter the necessary information as explained in the following table.

        <Image align="center" border={true} src="https://files.readme.io/0ca47335dbea534cb7d1b4ddce82c5eef9de68c4e17ac2c7169d6b82f3738835-carrier_details_block.png" width="400px" caption="Entering carrier details" />
        <br />

        <AsteridkForMandatoryElements />

        <table>
          <thead>
            <tr>
              <th>Element</th>
              <th>Description</th>
            </tr>
          </thead>
          <tbody>
            <tr>
              <td><strong>Posting Location Code</strong>&#42;</td>
              <td>
                This is a Royal Mail specific code given for each location you are despatching shipments from.
                <br />
                <br />
                This must be a 10 digit number that always starts with 9000. For example, 9000257150.
              </td>
            </tr>
            <tr>
              <td><strong>Receiving Hub Code</strong>&#42;</td>
              <td>
                Enter the code allocated by Royal Mail for the receiving Hub to where your goods will be taken.
                <br />
                <br />
                The <strong>Receiving Hub Code</strong> is automatically populated based on the postcode of the shipping location to which you are linking this account.
              </td>
            </tr>
            <tr>
              <td><strong>OBA Access Code</strong></td>
              <td>This field is autopopulated by INTERSOFT and is something we communicate directly with the carrier after the shipping account has been added.</td>
            </tr>
          </tbody>
        </table>

        ***
      </ToggleListItem>

      <ToggleListItem title="6. Submit and save the shipping account" icon="fa-check">
        <br />

        After entering all the required information, select ![](https://files.readme.io/db03c9a2b7ee816f42db617829469dce01bbdfd35aca00ace480fd78db31aa11-add_shipping_account_button_2.png).

        Once done, you have successfully added a shipping account. Once the account is [approved](https://docs.intersoftsapient.net/docs/royal-mail-sign-off#/), you can start shipping with it.

        ***
      </ToggleListItem>

    </ToggleList>
  </Tab>

  <Tab title="Via API">
    To add a Royal Mail shipping account via API, refer to the following API endpoint.

    <Cards>
      <Card title="Add Account" href="https://docs.intersoftsapient.net/v4.04/reference/post_v4-shippingaccounts-rm" icon="fa-code">
        Add and manage Royal Mail shipping account via API.
      </Card>
    </Cards>
  </Tab>
</Tabs>

***

### See also

<Cards columns="2">
  <Card title="Edit shipping account" href="https://docs.intersoftsapient.net/docs/edit-shipping-account" icon="fa-pen-to-square" target="_blank">
    Modify an existing shipping account's details.
  </Card>
</Cards>
