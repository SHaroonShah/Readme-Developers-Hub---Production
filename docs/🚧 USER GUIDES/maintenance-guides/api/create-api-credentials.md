---
title: Create API Credentials
excerpt: >-
  Learn how to create secure API credentials in SAPIENT to authenticate and
  authorize access to web services through Application Programming Interfaces.
deprecated: false
hidden: false
icon: fad fa-certificate
link:
  new_tab: false
metadata:
  title: ''
  description: ''
  robots: index
---
## What are API Credentials?

<Cards columns={2}>
  <Card title="Security & Authentication" icon="shield-alt">
    API credentials are unique identifiers that authenticate and authorize applications or users accessing web-based services via APIs.
  </Card>
  <Card title="Access Control" icon="key">
    Enable secure and controlled access to API functionalities, allowing developers to integrate systems with external services safely.
  </Card>
</Cards>

In SAPIENT, you can create your own API credentials to track usage, manage permissions effectively, and protect your data from unauthorized access.

## Creating Your API Credentials

<Accordion title="Step-by-Step Guide" icon="list-ol">

### Step 1: Access SAPIENT Platform
Log in to the SAPIENT platform using your credentials.

<Image alt="Logging into SAPIENT" align="center" width="400px" border={true} src="https://files.readme.io/639e7805edcaa9527380c1d5cd14463e8753cce43eda79ac3ccdd09732e045b2-Sapient_Login_window.png">
  Logging into SAPIENT
</Image>

### Step 2: Navigate to API Credentials
On the **Home** page, in the left navigation panel, select **API** > **Credentials**.

<Image alt="Accessing API credentials" align="center" border={true} src="https://files.readme.io/d293d6725e51d7d9aefd357ce17c120786c04f72132f6751c0051aa2fcacdd76-Credentials_option.png">
  Accessing API credentials
</Image>

### Step 3: Initiate Credential Creation
On the **API Credentials** page, select the **Create API Credentials** button.

<Image alt="Selecting option to create API credentials" align="center" src="https://files.readme.io/94c18d9f5d3e5c663beae626b71b6bd8bd0d72614e7d70cb57905b252570c20e-Create_API_Credentials_button.png">
  Selecting option to create API credentials
</Image>

> 📘 **Note**
>
> You are only required to create these credentials the first time you log in.

### Step 4: Name Your Credentials
In the **Create API Credentials** dialog, enter a brief memorable name for your API credential and select **Create**.

<Image alt="Creating API credentials" align="center" width="400px" border={true} src="https://files.readme.io/b15de257efd0a5495ae25acad8252acf0173f3a48bce625c4e5e4a9c461a7811-Create_API_Credentials_dialog.png">
  Creating API credentials
</Image>

### Step 5: Copy Your Credentials
In the **API Credentials** dialog, copy the generated **Client ID** and **Secret**.

<Image alt="Saving client ID and secret" align="center" width="400px" border={true} src="https://files.readme.io/2792065801168e1bbda76a6bdae6035bf62a1d53d16fd27b2e49b72b2d199746-API_Credentials_dialog.png">
  Saving client ID and secret
</Image>

> 🚧 **Important Security Notice**
>
> Make sure you copy the **Secret** and keep it safe as we do not store this anywhere within the application and you cannot see it again. If you lose the secret, you must create a new set of credentials.

### Step 6: Complete the Process
After copying the client ID and secret, select **Close**.

</Accordion>

## What Happens Next?

<Columns layout="auto">
  <Column>
    ### ✅ Credentials Created
    Your new API credentials are successfully created and appear in the **CURRENT API CREDENTIALS** table on the **API Credentials** page.
  </Column>
  <Column>
    ### 🔧 Ready to Use
    You can now use these credentials to authenticate each API call when making requests to the SAPIENT API.
  </Column>
</Columns>

<Image alt="Newly created API credentials" align="center" border={true} src="https://files.readme.io/282a98da9661dd060294cc5dcb0019d061b7a756357f81147fe765cac8a22217-API_credentials_created.png">
  Newly created API credentials
</Image>

## Best Practices

<Cards columns={3}>
  <Card title="Secure Storage" icon="lock">
    Store your API credentials in a secure location and never share them publicly.
  </Card>
  <Card title="Regular Monitoring" icon="chart-line">
    Monitor your API usage through the credentials dashboard to track activity.
  </Card>
  <Card title="Access Management" icon="users-cog">
    Create separate credentials for different applications or team members when needed.
  </Card>
</Cards>