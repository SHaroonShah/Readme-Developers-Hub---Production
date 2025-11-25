---
title: Generate Bearer Token
excerpt: >-
  Learn how to generate bearer tokens using Postman for secure API
  authentication. Step-by-step guide with visual examples and best practices for
  token management.
deprecated: false
hidden: false
icon: fad fa-layer-plus
link:
  new_tab: false
metadata:
  title: ''
  description: ''
  robots: index
---
Generating a bearer token is essential for securely managing access to APIs, allowing for robust authentication mechanisms while maintaining a stateless, scalable architecture.

> 📘 _Note_
>
> _This section explains the process of generating the bearer token via the Postman application. You may use other platforms to generate the bearer token, if applicable._

## Overview

<Cards columns={2}>
  <Card title="What You'll Need" icon="fa-list-check">
    * Postman application or account
    * API credentials from SAPIENT
    * Client ID and Client Secret
  </Card>

  <Card title="What You'll Get" icon="fa-key">
    * Bearer token for API authentication
    * Token expiry information
    * Ready-to-use authentication credentials
  </Card>
</Cards>

## Step-by-Step Process

<Accordion title="Step 1: Set Up Postman" icon="fa-rocket">
  Launch the Postman application or log in into your Postman account. If you have selected the online version, make sure to activate your account.

  <Callout icon="💡" theme="default">
    **###_Tip_ 
If you do not have the Postman application, you can download it [here](https://www.postman.com/downloads/) or register for an online Postman account, respectively.
  </Callout>
</Accordion>

<Accordion title="Step 2: Create HTTP Request" icon="fa-plus">
  After successfully logging in, on your workspace toolbar, select **New** > **HTTP**. Alternatively, on your workspace, select **+** tab to add a new HTTP request tab.

  <Image align="center" border={true} src="https://files.readme.io/93a14a1a00ff5ad67a4e5ad4a74677828b0e364b445c378ee24cd5795fe6acd5-New_HTTP_request_option.png" alt="Creating new HTTP request in Postman" />
</Accordion>

<Accordion title="Step 3: Configure Request URL" icon="fa-link">
  In the new request tab that opens, from the left dropdown menu, select **POST** and enter the following URL in the **Enter request URL** field:

  `https://authentication.intersoftsapient.net/connect/token`

  <Image align="center" border={true} src="https://files.readme.io/ab6a0e55d341d8aaf0cddbe95208ebc3c035155faeb32dd652bf011f79369dec-Postman_dropdown.png" alt="Entering URL" />
</Accordion>

<Accordion title="Step 4: Set Request Body Parameters" icon="fa-table">
  Now, select the **Body** tab and then click the **x-www-form-urlencoded** option. In the table that appears, enter the following key-value pairs:

  <Columns layout="auto">
    <Column>
      **Required Keys:**

      * `client_id`
      * `client_secret`
      * `grant_type`
    </Column>

    <Column>
      **Values:**

      * Your client ID from API credentials
      * Your client secret from API credentials
      * Set to `client_credentials`
    </Column>
  </Columns>

  Enter the credentials generated via the [SAPIENT API Credentials](https://docs.intersoftsapient.net/docs/create-api-credentials) functionality. For the **grant\_type** key, set the value to **client\_credentials**.

  <Image align="center" border={true} src="https://files.readme.io/ca361ef126d7b2b88c83d9c6b38ae3e56a4e1d5a0e38b0beed057fc05b86067c-Adding_key_value_pairs.png" alt="Adding keys value pairs" />
</Accordion>

<Accordion title="Step 5: Send Request and Get Token" icon="fa-paper-plane">
  After entering the necessary information, select **Send**.

  If the credentials match the ones that have been set in the **Create API Credentials** functionality, then the bearer token is returned in the response.

  <Image align="center" border={true} src="https://files.readme.io/b8499e2-image.png" alt="Bearer token response example" />
</Accordion>

## Understanding the Response

<Tabs>
  <Tab title="Token Response">
    The API returns a JSON response containing:

    * `access_token`: Your bearer token
    * `expires_in`: Token validity duration in seconds
    * `token_type`: Usually "Bearer"
  </Tab>

  <Tab title="Token Expiry">
    The **expires\_in** value indicates the duration for which the token remains valid, measured in seconds. For example, a value of 3600 seconds corresponds to 60 minutes of validity.

    <Callout icon="🚧" theme="warning">
      **Important:** Please ensure you cache the authentication token and check for expiry before requesting a new one.
    </Callout>
  </Tab>
</Tabs>

<Image align="center" alt="Sample bearer token" border={true} caption="Bearer token sample" src="https://files.readme.io/c67152f-image.png" width="50%" />

## Next Steps

Once the bearer token has been generated successfully, you can now use it for authentication purposes in your API requests. Include the token in the Authorization header as: `Bearer [your-token-here]`
