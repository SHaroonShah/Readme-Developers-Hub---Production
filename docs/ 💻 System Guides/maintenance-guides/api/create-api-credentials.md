---
title: Create API Credentials
excerpt: >-
  _API credentials_ are unique identifiers that are used to authenticate and
  authorise applications or users accessing a web-based service via an
  Application Programming Interface (API).
deprecated: false
hidden: false
icon: fad fa-certificate
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
The primary purpose of creating API credentials is to enable secure and controlled access to the functionalities offered by the API, allowing developers to integrate their systems with external services.

In SAPIENT, you can create you own API credentials with which you can track usage, manage permissions effectively, and protect your data from unauthorised access.

## How to create API credentials

To create new API credentials, follow the instructions as explained in the following procedure.

<ToggleList>
  <ToggleListItem title={<strong>1. Navigate to API credentials</strong>} icon="fa-rocket">
    <br />

    On the **Home** page, in the left navigation panel, select **API** > **Credentials**.

    <Image align="center" border={true} src="https://files.readme.io/d293d6725e51d7d9aefd357ce17c120786c04f72132f6751c0051aa2fcacdd76-Credentials_option.png" caption="Accessing API credentials" />

    ***
  </ToggleListItem>

  <br />

  <ToggleListItem title={<strong>2. Access option to create credentials</strong>} icon="fa-rocket">
    <br />

    On the **API Credentials** page, select the **Create API Credentials** button.

    <Image align="center" src="https://files.readme.io/94c18d9f5d3e5c663beae626b71b6bd8bd0d72614e7d70cb57905b252570c20e-Create_API_Credentials_button.png" caption="Selecting option to create API credentials" />

    <br />

    > 📘 *Note*
    >
    > *You are only required to create these credentials the first time you log in.*

    ***
  </ToggleListItem>

  <br />

  <ToggleListItem title={<strong>3. Select user type</strong>} icon="fa-rocket">
    <br />

    On the **Add User** form that opens, in the **USER TYPE** block, from the **Type of User** dropdown, select the user type from the list of available ones.

    <Image align="center" border={true} src="https://files.readme.io/bb66dcbf937dc36953a8242a21580c7d67c3e4d804f438040b8aecdebe3defe5-User_type_block.png" width="400px" caption="Specifying user type" />

    ***
  </ToggleListItem>

  <br />

  <ToggleListItem title={<strong>4. Enter credential details </strong>} icon="fa-rocket">
    <br />

    In the **Create API Credentials** dialog, enter a brief memorable name for your API credential and select **Create**.

    <Image align="center" border={true} src="https://files.readme.io/b15de257efd0a5495ae25acad8252acf0173f3a48bce625c4e5e4a9c461a7811-Create_API_Credentials_dialog.png" width="400px" caption="Creating API credentials" />

    ***
  </ToggleListItem>

  <br />

  <ToggleListItem title={<strong>5. Copy your credentials</strong>} icon="fa-rocket">
    <br />

    In the **API Credentials** dialog, copy the generated **Client ID** and **Secret**.

    <Image align="center" border={true} src="https://files.readme.io/2792065801168e1bbda76a6bdae6035bf62a1d53d16fd27b2e49b72b2d199746-API_Credentials_dialog.png" width="400px" caption="Saving client ID and secret" />

    <br />

    > 🚧 *Important*
    >
    > *Make sure you copy the **Secret** and keep it safe as we do not store this anywhere within the application and you cannot see it again. If you lose the secret, you must create a new set of credentials.*<br />

    After copying the client ID and secret, select **Close**.

    Once done,  your new API credentials are successfully created and appear in the **CURRENT API CREDENTIALS** table on the **API Credentials** page.  You can now use these credentials to authenticate each API call when making requests to the SAPIENT API.
  </ToggleListItem>
</ToggleList>
