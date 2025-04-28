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

## Authentication with recent invoice

If you want to validate your FedEx shipping account via the recent invoice, then you must select the **Recent Invoice** option, and enter the necessary information as described in the following table.

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
        Enter the carrier account number.

        The format of the account number must be compliant with the carrier you have selected. If your account number does not meet the requirements, you may need to add the required amount of zero's at the beginning of the number to ensure it lies within the standard character length range for that carrier.
      </td>
    </tr>

    <tr>
      <td>
        **Invoice Date**\*
      </td>

      <td>
        From the dropdown menu, select one of the following account types that you want to set up for the the shipping account you are adding:

        • **[Production](https://docs.intersoftsapient.net/docs/sandbox-account)**: a live environment where the final version of the application is deployed and made available to the users.

        • **[Sandbox](https://docs.intersoftsapient.net/docs/sandbox-account)**: a testing environment that mimics the **Production** environment but is isolated from it. The sandbox environment is primarily used for development and testing purposes.
      </td>
    </tr>

    <tr>
      <td>
        **Currency**\*
      </td>

      <td>
        Enter the account name.
      </td>
    </tr>

    <tr>
      <td>
        **Invoice Amount**\*
      </td>

      <td>
        Enter the email address that was used to register the account for the carrier you selected.
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
        **Validate**\*
      </td>

      <td>
        Enter the contact number for the account you are adding.
      </td>
    </tr>
  </tbody>
</Table>