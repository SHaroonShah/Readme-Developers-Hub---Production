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

> 🚧 _Important_
>
> _Before setting up the <Glossary>shipping account</Glossary>, make sure:_
>
> * _You have [enabled the integration](https://docs.intersoftsapient.net/docs/integration-activation) with FedEx and have already [created a shipping location](https://docs.intersoftsapient.net/docs/add-a-shipping-location)._
> * _You have the 9-digit FedEx carrier account number._
> * _You have the exact shipping address that you have provided to FedEx, as this information is validated via the Address Validation API. If the address does not match, then a corresponding error message is displayed—and you will not proceed to the **Multi-Factor Authentication** (MFA) stage of the **Add Shipping Account** form._
>
> _The multi-factor authentication is a crucial stage of the FedEx shipping account creation process, and this authentication must be completed by the FedEx account holder. This is done so that the account is validated in a secure manner and then can be used for shipping via our API._

## How to add FedEx shipping account

To add a shipping account for FedEx in SAPIENT, follow the instructions as explained in the following procedure:

> 🚧 _Important_
>
> _You can create and manage the FedEx shipping account only via the SAPIENT UI._

<ToggleList>
  <ToggleListItem title="1. Select the Shipping Accounts page">
    In the left navigation panel, select **Shipping Accounts**.

    <Image align="center" border={true} src="https://files.readme.io/3e60281b3dfe72e1d825e37b48a9dbcb8a5446f083dc00aa30b8189f109e58dc-Shipping_account_option.png" alt="Accessing shipping accounts" />

    ***
  </ToggleListItem>

  <br />

  <ToggleListItem title="2. Select option to add shipping account">
    On the **Shipping Accounts** page that opens, select ![](https://files.readme.io/5eb134426849b1adb3049756830b6bef19e7dc67dca55891e64ff7b9c8eadd8e-add_shipping_account_button.png).

    <Image align="center" border={true} src="https://files.readme.io/3b149ee84f86fb8d4f02c43b2733c7eb85aea3ac6e2f01692af371f631570bf3-Add_shipping_account_button_DX.png" alt="Accessing option to add shipping account" />

    ***
  </ToggleListItem>

  <br />

  <ToggleListItem title="3. Enter account details">
    On the **Add Shipping Account** form that appears, in the **ACCOUNT DETAILS** block, fill in the necessary information as described in the following table.

    <Image align="center" border={true} src="https://files.readme.io/0aa0c2e5571aecb4b468578dd7f4575502f692fed3703818183b78c9a4548a82-Add_shipping_account_FedEx.png" width="500px" alt="Entering account details" />

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
    After specifying the carrier and shipping location, a new **CONNECT YOUR FEDEX ACCOUNT** form appears. At the **Shipping Account** stage of the form, [specify the general details](https://docs.intersoftsapient.net/docs/specify-shipping-account-details#/) associated to your FedEx account number.

    <Tabs>
 <Tab title="5. Specify shipping account details">
        At the **EULA** stage, [carefully read the FedEx end user license agreement](https://docs.intersoftsapient.net/docs/confirm-fedex-end-user-license-agreement#/) and confirm it by selecting the checkbox and ![](https://files.readme.io/a544674d471b96aadef7f8afe38ba10b912f11fb7b7fd758dc372d04dfbdd7da-I_agree_button.png) button to proceed to the next stage.

        <Image align="center" border={true} src="https://files.readme.io/c3319a8a8ce0acdd3155e5d73cec44011b84d796486eca6a56e62728392a6925-FedEx_Eula_tab.png" alt="Accepting FedEx end-user license agreement" />
      </Tab>

      <Tab title="5. Confirm EULA">
        At the **EULA** stage, [carefully read the FedEx end user license agreement](https://docs.intersoftsapient.net/docs/confirm-fedex-end-user-license-agreement#/) and confirm it by selecting the checkbox and ![](https://files.readme.io/a544674d471b96aadef7f8afe38ba10b912f11fb7b7fd758dc372d04dfbdd7da-I_agree_button.png) button to proceed to the next stage.

        <Image align="center" border={true} src="https://files.readme.io/c3319a8a8ce0acdd3155e5d73cec44011b84d796486eca6a56e62728392a6925-FedEx_Eula_tab.png" alt="Accepting FedEx end-user license agreement" />
      </Tab>

      <Tab title="6. Enter shipping address details">
        At the **Shipping Address** stage that appears, [specify the FedEx shipping address details](https://docs.intersoftsapient.net/docs/specify-shipping-address-details#/) so that the system can validate and match it with the address registered in the FedEx systems. Select ![](https://files.readme.io/467fc35d98b9402e95108b15780beb269e7b7c935be406e916cb506d31d25663-Submit_button.png). After the address has been validated, the **accountAuthToken** is generated. Save the generated token.

        <Image align="center" border={true} src="https://files.readme.io/44a0d7bc452b2b65f362c4365107b07a28760e52cfce04c2ddd7418dbae127f3-FedEx_Shippig_address_stage.png" alt="Specifying FedEx shipping address details" />
      </Tab>

      <Tab title="7. Complete MFA">
        At the **Multi Factor Authentication** stage, [complete the multi-factor authentication process](https://docs.intersoftsapient.net/docs/initiate-multi-factoer-authentication-process#/) by using the invoice number or PIN generation validation methods. Select ![](https://files.readme.io/9ad4e9682f0c8d463a45785d7597c52ee40602f9e6a914f27bb6656409011726-Validate_button.png).

        <Image align="center" src="https://files.readme.io/7b2058eb6bf72d27640c63a5d639fd9b2a4675a4c0e83b7236a917e77f748842-Recent_invoice_option.png" alt="Completing multi-factor authentication" />

        <Callout icon="📘" theme="info">
          *After submitting the form, if you have selected the**Enable Electronic Trade Documents (ETD)** checkbox, then a corresponding link is displayed with your successful account creation notification, prompting you to configure the ETD data via the [Signatures and logos](https://docs.intersoftsapient.net/docs/add-signature-and-logos-to-etd-documents#/) feature of SAPIENT.*
        </Callout>
      </Tab>

      <Tab title="8. Start shipping">
        Once validated, if all the entered information is correct, FedEx passes the MFA validation, and your FedEx shipping account is created successfully. At this point, INTERSOFT will get the new API credentials from FedEx for your shipping account for you to start shipping with your newly created FedEx account via our API.
      </Tab>
    </Tabs>
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

  <Card title="Specify shipping account details" icon="fa-list-check" href="https://docs.intersoftsapient.net/docs/specify-shipping-account-details#/">
    Enter the general details associated with your FedEx account number.
  </Card>

  <Card title="Add signatures and logos to ETD documents" icon="fa-file-signature" href="https://docs.intersoftsapient.net/docs/add-signature-and-logos-to-etd-documents#/">
    Configure ETD signatures and logos after creating the FedEx shipping account.
  </Card>
</Cards>

<br />
