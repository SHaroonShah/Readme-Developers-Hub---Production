---
title: Log in to SAPIENT
excerpt: >-
  This section describes how you can log in to the SAPIENT system, change or
  reset your password, and also log out of SAPIENT.
deprecated: false
hidden: false
icon: fad fa-chalkboard-user
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
## Overview

To access the SAPIENT system, you'll need to log in with your credentials. This guide covers the login process for different user types and includes helpful tips for managing your account.

<Cards columns={2}>
  <Card title="Admin Users" icon="fa-solid fa-user-shield">
    Administrative users with full system access and management capabilities
  </Card>

  <Card title="Customer Users" icon="fa-solid fa-user">
    Regular users with access to customer-specific features and workflows
  </Card>
</Cards>

## Logging into SAPIENT

To log in to the SAPIENT system, follow the instructions as explained in the following procedure.

<ToggleList>
  <ToggleListItem title={<strong>1. Access the system</strong>} icon="fa-rocket">
    <br />

    Open your browser and in the address bar, enter the URL address of the SAPIENT system.

    ***
  </ToggleListItem>

  <br />

  <ToggleListItem title={<strong>2. Enter your credentials</strong>} icon="fa-rocket">
    <br />

    Depending on the type of the user (<Glossary>admin</Glossary> or <Glossary>customer</Glossary>), you are offered to enter your email address and password, and then click **Sign in**.

    <Image align="center" src="https://files.readme.io/fa5d0ced6ed38b419fa15c57f5b03fdddf6284adfcc85b48370c67d1aa07c5f8-Sapient_Login_window.png" width="300px" alt="Logging into SAPIENT" />

    ***
  </ToggleListItem>

  <br />

  <ToggleListItem title={<strong>3. Complete Multi-Factor Authentication (MFA) if enabled</strong>} icon="fa-rocket">
    <br />

    After selecting the **Sign in** option, if MFA has been enabled on your customer account, then the **Account Verification** dialog is displayed. Enter the necessary information as explained in the following table.

    <Image align="center" src="https://files.readme.io/aedd19ae14dc2acd5800c767d63962b0f8275f09b30b58156c2bf9165ac6744f-image.png" width="400px" />

    | Element                          | Description                                                                                                                                                                      |
    | :------------------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
    | **Code**                         | Enter the 6-digit code sent your email address associated with your SAPIENT account.                                                                                             |
    | **Do not ask again for 14 days** | Select this link to snooze the MFA for 14 days, after which you are required to complete the MFA step again to login to the SAPIENT application.                                 |
    | **Send a new code**              | Select this link if you did not receive the verification code. This option will generate and send a new code to your registered email address.                                   |
    | **Verify and sign in**           | Select ![alt text](https://files.readme.io/8a307af6c7ec1ced0489d4f630029434fe08a575de45b9bf835df17bf4eaec82-Verify_and_sign_in_button.png) to log in to the SAPIENT application. |
    <br />
> 📘 _Note_
>
> _If MFA is not enabled for your customer account or you have snoozed the MFA prompt, then the SAPIENT home page opens._


    ***
  </ToggleListItem>

  <br />

  <ToggleListItem title={<strong>4. Access the home page</strong>} icon="fa-rocket">
    <br />

    Once the MFA process has been completed successfully, the SAPIENT Home page opens. You can now start using the system and execute your workflows.
  </ToggleListItem>
</ToggleList>

## Account management

On the application header of the home page, you can access additional account options by selecting the user profile icon:

<Cards columns={2}>
  <Card title="Change Password" href="https://docs.intersoftsapient.net/v4.02/docs/change-password" icon="fa-solid fa-key">
    Learn how to update the password for enhanced security.
  </Card>

  <Card title="Log out" href="https://docs.intersoftsapient.net/v4.02/docs/log-out" icon="fa-solid fa-arrow-right-from-bracket">
    Learn how to exit the system securely.
  </Card>
</Cards>
