---
title: Initiate Multi-factor authentication process
deprecated: false
hidden: true
metadata:
  robots: index
---
After specifying the shipping address details of your FedEx account, at the **Multi Factor Authentication** stage, you can validate your account

With FedEx, you can only create shipments using the OAuth token in the header of the FedEx API request. To obtain the OAuth token, you need to send the client ID, client secret, child key, and child secret in the API authorisation request.

To retrieve the child key and child secret, you first need to complete the multi-factor authentication process by using one of the following validation methods available at the **Multi Factor Authentication** stage of the form.

## Authentication with recent invoice details

If you want to validate your FedEx shipping account via the recent invoice, then you must select the **Recent Invoice** option, and enter the necessary information as described in the following table.

<Image align="center" border={true} caption="Authenticating FedEx shipping account with invoice details" src="https://files.readme.io/d5ab0db4e4030ad6c483ebfee1f964109f4d0d4c3d8839a9224b656fb463a4e9-Recent_invoice_option.png" />

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
        **Validate**\*
      </td>

      <td>
        select ![alt text](https://files.readme.io/9ad4e9682f0c8d463a45785d7597c52ee40602f9e6a914f27bb6656409011726-Validate_button.png) to initiate the MFA validation process.
      </td>
    </tr>
  </tbody>
</Table>

Upon validation, SAPIENT calls the Invoice Validation API request using the Authorisation and AccountAuthToken and returns the child ID and child secret in the success response. This information is stored in the your shipping account record and will be used to get the OAuth token for your account.

## Authentication with PIN generation

If you want to validate your FedEx shipping account via PIN, then you must select the **PIN Generation** option, and enter the necessary information as described in the following table.

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
      </td>
    </tr>

    <tr>
      <td>
        **Request a new PIN**\*
      </td>

      <td>
        Enter the exact amount displayed on your invoice.

        *`Note`: The invoice amount must be in the US format with decimals, for example, 234.50.*
      </td>
    </tr>

    <tr>
      <td>
        **Validate**\*
      </td>

      <td>
        select ![alt text](https://files.readme.io/9ad4e9682f0c8d463a45785d7597c52ee40602f9e6a914f27bb6656409011726-Validate_button.png) to initiate the MFA validation process.
      </td>
    </tr>
  </tbody>
</Table>

Upon validation, SAPIENT calls the Invoice Validation API request using the Authorisation and AccountAuthToken and returns the child ID and child secret in the success response. This information is stored in the your shipping account record and will be used to get the OAuth token for your account.