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

<Image align="center" border={true} caption="Entering MFA code" src="https://files.readme.io/62cbde26119f29ee7a847236d4c2e41c06307a6ed5032fe3cd6ea45161adbe04-image.png" width="400px" />

    | Element                          | Description                                                                                                                                      |
    | :------------------------------- | :----------------------------------------------------------------------------------------------------------------------------------------------- |
    | **Code**                         | Enter the 6-digit code sent your email address associated with your SAPIENT account.                                                             |
    | **Do not ask again for 14 days** | Select this link to snooze the MFA for 14 days, after which you are required to complete the MFA step again to login to the SAPIENT application. |
    | **Send a new code**              | Select this link if you did not receive the verification code. This option will generate and send a new code to your registered email address.   |

    ***
  </ToggleListItem>

  <ToggleListItem title={<strong>4. Access the home page</strong>} icon="fa-rocket">
    <br />

    Once clicked, the SAPIENT Home page opens. You can now start using the system and execute your workflows.
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



<br />
