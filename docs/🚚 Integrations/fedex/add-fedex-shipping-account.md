---
title: Add FedEx shipping account
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
In SAPIENT, you can create a FedEx shipping account by selecting your desired <Glossary>shipping location</Glossary>, entering the corresponding account and carrier details, and then adding the account to the system.

<Callout icon="🚧" theme="warn">
  ### _Important_

  _Before setting up the <Glossary>shipping account</Glossary>, make sure:_

  - _You have [enabled the integration](https://docs.intersoftsapient.net/docs/integration-activation) with FedEx and have already [created a shipping location](https://docs.intersoftsapient.net/docs/add-a-shipping-location)._
  - _You have the 9-digit FedEx carrier account number._
  - _You have the exact shipping address that you have provided to FedEx, as this information is validated via the Address Validation API. If the address does not match, then a corresponding error message is displayed—and you will not proceed to the&#x20;_**_Multi-Factor Authentication_**_&#x20;(MFA) stage of the&#x20;_**_Add Shipping Account_**_&#x20;form._

  _The multi-factor authentication is a crucial stage of the FedEx shipping account creation process, and this authentication must be completed by the FedEx account holder. This is done so that the account is validated in a secure manner and then can be used for shipping via our API._
</Callout>

## How to add FedEx shipping account

To add a shipping account for FedEx in SAPIENT, follow the instructions as explained in the following procedure:

<Callout icon="🚧" theme="warn">
  ### _Important_

  _You can create and manage the FedEx shipping account only via the SAPIENT UI._
</Callout>

<ToggleList>
  <ToggleListItem title="1. Select the Shipping Accounts page">
    In the left navigation panel, select **Shipping Accounts**.

    <Image align="center" border={true} src="https://files.readme.io/3e60281b3dfe72e1d825e37b48a9dbcb8a5446f083dc00aa30b8189f109e58dc-Shipping_account_option.png" caption="Accessing shipping accounts" />

    ***
  </ToggleListItem>

  <br />

  <ToggleListItem title="2. Select option to add shipping account">
    On the **Shipping Accounts** page that opens, select ![](https://files.readme.io/5eb134426849b1adb3049756830b6bef19e7dc67dca55891e64ff7b9c8eadd8e-add_shipping_account_button.png).

    <Image align="center" border={true} src="https://files.readme.io/3b149ee84f86fb8d4f02c43b2733c7eb85aea3ac6e2f01692af371f631570bf3-Add_shipping_account_button_DX.png" caption="Selecting option to add shipping account" />

    ***
  </ToggleListItem>

  <br />

  <ToggleListItem title="3. Enter account details">
    On the **Add Shipping Account** form that appears, in the **ACCOUNT DETAILS** block, fill in the necessary information as described in the following table.

    <Image align="center" border={true} src="https://files.readme.io/0aa0c2e5571aecb4b468578dd7f4575502f692fed3703818183b78c9a4548a82-Add_shipping_account_FedEx.png" width="500px" caption="Entering account details" />

    <br />

    <AsteridkForMandatoryElements />

    |         Element         | Description                                                                                                                                 |
    | :---------------------: | :------------------------------------------------------------------------------------------------------------------------------------------ |
    |      **Carrier**\*      | From the dropdown list, select **FEDEX - FedEx**.                                                                                           |
    | **Shipping Location**\* | From the dropdown menu, select the <Glossary>shipping location</Glossary> that you want to assign to the shipping account you are creating. |

    ***
  </ToggleListItem>

  <br />

  <ToggleListItem title="4. Connect account">
    After specifying the carrier and shipping location, a new **CONNECT YOUR FEDEX ACCOUNT** form appears, which is comprised of multiple stages. Enter the necessary information as explained in the followig tabs.

    <Callout icon="💡" theme="default">
      ### *Tip*

      *When entering the information, follow the order in which the tabs are displayed.*
    </Callout>

    <Tabs>
      <Tab title="1. Shipping Account">
        <br />

        At the **Shipping Account** stage, you can specify the general details associated to your FedEx account number.

        <Image align="center" border={true} src="https://files.readme.io/8822b5421cd564a71a5d9e39a2ad6ec6cc6eb783034bb5979b0b2522299bdc55-FEDEX_Shipping_account_stage.png" caption="Entering shipping account details" />

        <br />

        The information on how to fill in the the necessary information at this stage are explained in the following table.

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
                Enter the 9-digit account number for FedEx.

                *`Note`: The carrier account number must be an exact match with what FedEx have provided.*
              </td>
            </tr>

            <tr>
              <td>
                **Account Name (if different than customer)**\*
              </td>

              <td>
                Enter the name of the account you are adding.
              </td>
            </tr>

            <tr>
              <td>
                **Account Type**\*
              </td>

              <td>
                From the dropdown menu, select one of the following account types that you want to set up for the the shipping account you are adding:

                • **[Production](https://docs.intersoftsapient.net/docs/sandbox-account)**: a live environment where the final version of the application is deployed and made available to the users. When you select **Production**, then upon selecting ![alt text](https://files.readme.io/9a8ec72b5969b1f4747f125dbf2e278b2442e39cb1dfe637a2d635f6020db504-Next_button.png), you are proceeded to the next stages of the form for the address and MFA validation processes.

                • **[Sandbox](https://docs.intersoftsapient.net/docs/sandbox-account)**: a testing environment that mimics the **Production** environment but is isolated from it. The sandbox environment is primarily used for development and testing purposes. If you select the **Sandbox** environment, then the shipping account is created without the address and MFA validation processes.

                *`Note`: You can use the**Sandbox** account to test the integration and generate test labels to ensure that it is configured correctly.*
              </td>
            </tr>

            <tr>
              <td>
                **Alias**\*
              </td>

              <td>
                Enter a custom name which can be used when connecting to us. Therefore, it is recommend that this name must be memorable and available for reference purposes.
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

            <tr>
              <td>
                **Enable Electronic Trade Documents (ETD)**
              </td>

              <td>
                Select this checkbox if you want to utilise electronic trade documents when shipping with FedEx. If you have completed the account creation process with this option selected, then at the end of the from, the system prompts you to go to the [Add signature and logo](https://docs.intersoftsapient.net/docs/add-signature-and-logos-to-etd-documents#/) page of the application to configure the required data for ETD.
              </td>
            </tr>

            <tr>
              <td>
                **Duties and taxes payment type**\*
              </td>

              <td>
                From the dropdown menu, select one of the following options:

                • **Sender** (a default value): The sender (or shipper) is responsible for any duties and taxes incurred when the <Glossary>shipment</Glossary> reaches its destination. This option is typically used when the sender wants full control over the shipment's costs.

                • **ThirdParty**: A third-party account is billed for duties and taxes. This option is used when the sender wants another designated company (not the sender or receiver) to pay the applicable fees. This means that the designated third party will bear the costs of duties and taxes instead of the sender or recipient.

                *`Note`: When the**ThirdParty** option is selected, an additional form is displayed for you to enter the third-party account details. For more information on how to fill this form, refer to the fields explained in the following table.*
              </td>
            </tr>
          </tbody>
        </Table>

        <br />

        If the **Duties and taxes payment type** field is set to **Third Party**, then you must fill the additional fields as explained in the following table.

        |              Element             | Description                                                                                                                                                                                                                                                                                      |
        | :------------------------------: | :----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
        |         **Contact Name**         | Enter the name of the primary contact person associated with the third party account.                                                                                                                                                                                                            |
        |         **Company Name**         | Enter the name of the company associated with the third party account.                                                                                                                                                                                                                           |
        |            **Country**           | From the dropdown menu, select the country in which the third party operates.                                                                                                                                                                                                                    |
        |           **Address**\*          | Enter the first line of the third party's address, typically including the street address or location where the company is based. This is important for accurate delivery and communication.                                                                                                     |
        |           **Address 2**          | Enter any additional address information that may be necessary, such as suite or apartment numbers, building names, or other relevant details that can help clarify the location.                                                                                                                |
        |           **Address 3**          | Enter any extra details on the address to specify the location if the previous two fields do not fully convey the address.                                                                                                                                                                       |
        |            **Town**\*            | Enter the town or city where the third party company is located.                                                                                                                                                                                                                                 |
        |            **County**            | Enter the name of the county in which the the third party company is located.                                                                                                                                                                                                                    |
        |           **Postcode**           | Enter the postal/ZIP code for the third party's address.                                                                                                                                                                                                                                         |
        |         **Contact Phone**        | Enter the phone number for the third party's primary contact person.                                                                                                                                                                                                                             |
        | **Third Party Account Number**\* | Enter the the unique FedEx account number of the third party that will be billed for the duties and taxes.                                                                                                                                                                                       |
        | **Tax Identification Numbers**\* | Enter the third party's tax identification numbers (TINs). If there are multiple TINs that need to be provided, separate each ID with a comma. This information is often required for customs clearance and ensures compliance with tax regulations.                                             |
        |             **Next**             | Select ![alt text](https://files.readme.io/b6c8af0dd2df7d574d6e95a6d57dee08b1b36bfe92e4350a94cb3b7eee6a5b71-Next_button.png) to proceed to the **Shipping Address** stage of the form.                                                                                                           |
        |            **Submit**            | Select ![alt text](https://files.readme.io/2ffa9cf28233588e3fa0be9258d8a2d6f5aa9d84f5e25f263c2c4d8c214cdbba-Submit_button.png) to create the shipping account and close the form. *`Note`: This button is only displayed if you have selected the**Sandbox** <Glossary>account type</Glossary>*. |
      </Tab>

      <Tab title="2. EULA">
        <br />

        After successfully specifying the shipping account details, at the **EULA** stage, read the FedEx 3rd party end user license agreement and confirm it by selecting the **I accept the terms of FedEx EULA to start shipping** checkbox and ![alt text](https://files.readme.io/a544674d471b96aadef7f8afe38ba10b912f11fb7b7fd758dc372d04dfbdd7da-I_agree_button.png) button.

        <Image align="center" border={true} src="https://files.readme.io/81109fca62feb4ab8c27b0f031bbdd6e5f8e16fb0cc80ebb9e01d243bafc1621-FedEx_Eula_tab.png" caption="Confirming EULA agreement"/>

        <br />

        > 🚧 *Important*
        >
        > *The checkbox is only activated after you have fully scrolled down to the bottom of the agreement. Please make sure you read the license agreement carefully before accepting it. Once the account is created, you cannot undo this selection.*

        After you have read the EULA and confirmed your agreement, the system marks the agreement as signed with the current date and the name of the user who signed it. Now, you are proceeded to the **Shipping Address** stage of the form.
      </Tab>

      <Tab title="3. Shipping Address (MFA 1)"> <br />
        After confirming the FedEx End-User License Agreement (EULA), the **Shipping Address** stage is the first factor of authentication, where you can specify the shipping address details that are associated with the 9-digit FedEx account number, so that the system can validate and match it with the addresses stored in the FedEx system.

        <Image align="center" border={true} src="https://files.readme.io/e0abd56eb4207f5e043cd1ba3259992715398fa85a2deaf011a014c8d02b85ca-FedEx_Shippig_address_stage.png" caption="Entering shipping address details"/>

        <br />

        The information on how to fill in the the necessary information at this stage are explained in the following table.

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
                **Customer Name**\*
              </td>

              <td>
                Enter the name of the company or organisation registered with FedEx.
              </td>
            </tr>

            <tr>
              <td>
                **Country**\*
              </td>

              <td>
                From the dropdown menu, select the country in which the customer resides.
              </td>
            </tr>

            <tr>
              <td>
                **Address**\*
              </td>

              <td>
                Enter the first line of the customer's address, typically including the street address or location where the customer is based. This is important for accurate validation of the customer details.

                *`Note:`Make sure you enter the exact address that you have provided against your FedEx account number. If the address validation fails, you will not proceed to the**Multi-Factor Authentication** stage of the form.*
              </td>
            </tr>

            <tr>
              <td>
                **Address 2**\*
              </td>

              <td>
                Enter any additional address information that may be necessary, such as suite or apartment numbers, building names, or other relevant details that can help clarify the location.
              </td>
            </tr>

            <tr>
              <td>
                **Address 3**\*
              </td>

              <td>
                Enter any extra details on the address to specify the location if the previous two fields do not fully convey the address.
              </td>
            </tr>

            <tr>
              <td>
                **Town**\*
              </td>

              <td>
                Enter the town or city where the customer is located.
              </td>
            </tr>

            <tr>
              <td>
                **County**
              </td>

              <td>
                Enter the sate of the county where the customer is based.
              </td>
            </tr>

            <tr>
              <td>
                **Postcode**\*
              </td>

              <td>
                Enter the postal/ZIP code for the customer's address.
              </td>
            </tr>

            <tr>
              <td>
                **This is a residential address**
              </td>

              <td>
                Select this checkbox if the address provided is a residential address.
              </td>
            </tr>

            <tr>
              <td>
                **Previous**
              </td>

              <td>
                Select ![alt text](https://files.readme.io/32d1e0325bb43e32995a83a961895c700550d54e72e6ecdece1661a2fe88d0a9-Previous_button.png) to return to the **Shipping Account** stage and update the information, if needed.
              </td>
            </tr>

            <tr>
              <td>
                **Submit**
              </td>

              <td>
                Select ![alt text](https://files.readme.io/d1aaa1a96df2bb864b3c2ff0bca425a2c21b8a8e159fa5bca06bdd323c0b3775-Submit_button.png) to save the entered information.
              </td>
            </tr>
          </tbody>
        </Table>

        Once the information is submitted, the system runs a validation check by validating the provided address via the**Address Validation** API. Based on the validation output, the system does the following:

        * If the validation is successful, you can proceed to the **Multi Factor Authentication** stage of the form.
        * If the validation fails (that is, the address is not matched in the FedEx systems), then a corresponding error message is displayed—and you will not proceed to the **Multi-Factor Authentication** (MFA) stage of the **Add Shipping Account** form. To proceed, you must enter the correct address details.
      </Tab>

      <Tab title="4. Multi Factor Authentication (MFA 2)"> <br />
        After specifying the shipping address details of your FedEx account and successfully completing the address validation, you are proceeded to the **Multi Factor Authentication** stage. This stage is the second factor of authentication, where you can validate your account with FedEx.

        <Accordion title="Authentication with recent invoice details">
          If you want to validate your FedEx shipping account via the recent invoice, then you must select the **Recent Invoice** option, and enter the necessary information as described in the following table.

          <Image align="center" border={true} src="https://files.readme.io/d5ab0db4e4030ad6c483ebfee1f964109f4d0d4c3d8839a9224b656fb463a4e9-Recent_invoice_option.png" caption="Configuring MFA with invoice details" />

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
                  **Invoice Number**\*
                </td>

                <td>
                  Enter a valid invoice number through which you want to authenticate the shipping account.
                </td>
              </tr>

              <tr>
                <td>
                  **Invoice Date**\*
                </td>

                <td>
                  Enter the date when the invoice was issued.

                  *`Note`: The invoice date must have been issued within the last 90 days.*
                </td>
              </tr>

              <tr>
                <td>
                  **Currency**\*
                </td>

                <td>
                  From the dropdown menu, select the currency specified with the amount in your invoice.
                </td>
              </tr>

              <tr>
                <td>
                  **Invoice Amount**\*
                </td>

                <td>
                  Enter the exact amount displayed on your invoice.\
                  *`Note`: The invoice amount must be in the US format with decimals, for example, 234.50.*
                </td>
              </tr>

              <tr>
                <td>
                  **Validate**
                </td>

                <td>
                  Select ![alt text](https://files.readme.io/9ad4e9682f0c8d463a45785d7597c52ee40602f9e6a914f27bb6656409011726-Validate_button.png) to initiate the MFA validation process.
                </td>
              </tr>
            </tbody>
          </Table>
        </Accordion>

        <br />

        <Accordion title="Authentication with PIN generation">
          If you want to validate your FedEx shipping account via PIN, then you must select the **PIN Generation** option, and enter the necessary information as described in the following table.

          <Image align="center" border={true} src="https://files.readme.io/1dd479887e9c4881543742d8ef07a3a1c993eefa871db0e9125ccaa3918fc77e-PIN_generation_options.png" caption="Configuring MFA with PIN generation"/>

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
                  **Verify with PIN**\*
                </td>

                <td>
                  From the dropdown menu, select one of the following options for the PIN generation request:

                  • **SMS**: Select this option if you want to receive the PIN via SMS. In this case, the PIN is sent as as a text message to your contact number registered with your FedEx account.

                  • **Phone Call**: Select this option if you want to receive the PIN via phone call. In this case, the PIN is disclosed on a phone call at your contact number registered with your FedEx account.

                  • **Email**: Select this option if you want to receive the PIN via email. In this case, the PIN is sent as an email to your email address registered with your FedEx account.
                </td>
              </tr>

              <tr>
                <td>
                  **Request PIN**\*
                </td>

                <td>
                  After selecting the desired method for PIN generation, select ![alt text](https://files.readme.io/ebe52fd81561c33e443aee0579c17fdf72a4d5359574d110acd760c025baec5a-Request_pin_button.png) to trigger the PIN generation process.
                </td>
              </tr>

              <tr>
                <td>
                  **Enter the 6 digit code we sent you**\*
                </td>

                <td>
                  Enter the 6-digit PIN code you received via the method you selected for the PIN generation request.

                  *`**Note**`: The pin is valid for 10 minutes only. If it is not utilised within this duration, you must request a new one.*
                </td>
              </tr>

              <tr>
                <td>
                  **Request a new PIN**\*
                </td>

                <td>
                  Select this link if your current PIN has expired or you did not receive one in the initial request.
                </td>
              </tr>

              <tr>
                <td>
                  **Validate**
                </td>

                <td>
                  Select ![alt text](https://files.readme.io/9ad4e9682f0c8d463a45785d7597c52ee40602f9e6a914f27bb6656409011726-Validate_button.png) to initiate the MFA validation process.
                </td>
              </tr>
            </tbody>
          </Table>
        </Accordion>

        <br />

        > 📘 *Note*
        >
        > *After submitting the form, if you have selected the**Enable Electronic Trade Documents (ETD)** checkbox, then a corresponding link is displayed with your successful account creation notification, prompting you to configure the ETD data via the [Signatures and logos](https://docs.intersoftsapient.net/docs/add-signature-and-logos-to-etd-documents#/) feature of SAPIENT.*

        ***
      </Tab>
    </Tabs>
  </ToggleListItem>

  <br />

  <ToggleListItem title="5. Start shipping">
    Once validated, if all the entered information is correct, FedEx passes the MFA validation and your FedEx shipping account is created successfully. At this point, INTERSOFT will get the new API credentials from FedEx for your shipping account for you to start shipping with your newly created FedEx account via our API.
  </ToggleListItem>
</ToggleList>

***

### See also

<Cards columns={2}>
  <Card title="Enable carrier integration" icon="fa-plug" href="https://docs.intersoftsapient.net/docs/integration-activation">
    Enable the FedEx integration before creating a FedEx shipping account.
  </Card>

  <Card title="Add a shipping location" icon="fa-location-dot" href="https://docs.intersoftsapient.net/docs/add-a-shipping-location">
    Create the shipping location that you want to assign to the FedEx shipping account.
  </Card>

  <Card title="Add signatures and logos to ETD documents" icon="fa-file-signature" href="https://docs.intersoftsapient.net/docs/add-signature-and-logos-to-etd-documents#/">
    Configure ETD signatures and logos after creating the FedEx shipping account.
  </Card>
</Cards>

<br />
