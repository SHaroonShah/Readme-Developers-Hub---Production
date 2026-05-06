---
title: Obtain DX API credentials
excerpt: >-
  _API credentials_ are unique identifiers that are used to authenticate and
  authorise applications or users accessing a web-based service via an
  Application Programming Interface (API).
deprecated: false
hidden: false
icon: fad fa-gear-code
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
Before [adding the DX shipping cccount](https://docs.intersoftsapient.net/docs/shipping-accounts-5) with Intersoft, you need to make sure you have the necessary information required for the account setup. This is typically your **Username** and **Password** provided in your DX API credentials.

To set up your DX API credentials, follow the instructions in the following procedure.

<ToggleList>
  <ToggleListItem title="Step 1: Log in to DX Despatch Manager">
    Log into [DX Despatch Manager](https://despatch.dxdelivery.com/login?ReturnUrl=%2F) with your login credentials. These credentials are provided when your DX account was setup.
  </ToggleListItem>

  <ToggleListItem title="Step 2: Open API Access Management">
    Once you are logged in, select **Settings** > **API Access Management**.

    <Image align="center" alt="Accessing API access management" border={true} caption="Accessing API access management" src="https://files.readme.io/ed20103-image.png" />
  </ToggleListItem>

  <ToggleListItem title="Step 3: Add an API user">
    On the page that opens, select **Add API User**.

    <Image align="center" alt="Selecting option to add API user " border={true} caption="Selecting option to add API user" src="https://files.readme.io/60673e2-image.png" />
  </ToggleListItem>

  <ToggleListItem title="Step 4: Enter the API user details">
    In the **Add API User** form that opens, enter the necessary information as explained in the following table.

    <Image align="center" alt="Adding API user" border={true} caption="Adding API user" src="https://files.readme.io/3e31ffe-image.png" />

    |       Element      | Description                                                                                                     |
    | :----------------: | :-------------------------------------------------------------------------------------------------------------- |
    |    **User name**   | Enter your username that you want to use to set up your DX <Glossary>shipping account</Glossary> via Intersoft. |
    |    **Password**    | Enter a strong memorable password for the username you entered.                                                 |
    | **Password again** | Enter your password again for confirmation.                                                                     |
    |      **Name**      | Enter the name of the API user you are adding.                                                                  |
    |     **Account**    | From the dropdown menu, select the account type that you want use for the API user you are adding               |
    |      **Role**      | From the dropdown menu, select the role that you want to assign to the API user you are adding                  |
  </ToggleListItem>

  <ToggleListItem title="Step 5: Save the API user">
    After entering the information, select **Save**.
  </ToggleListItem>
</ToggleList>

Once saved, the new API user has been created successfully. You can now use this information to set up the shipping account via Intersoft.

> 📘 *Note*
>
> *If you would like an account specifically for testing purposes, you can log a request with DX's service desk at [service.desk@dxdelivery.com](mailto:service.desk@dxdelivery.com) and request your own test API credentials.*