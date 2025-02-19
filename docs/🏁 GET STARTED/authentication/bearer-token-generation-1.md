---
title: Generate bearer token
excerpt: >-
  _Bearer token_ is a type of access token that is used in the authentication
  and authorisation processes for APIs. It is a string that provides the user or
  system the identity to access sensitive resources or actions on a server.
  Bearer tokens are commonly used in the token-based authentication systems,
  such as OAuth2.
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
Generating a bearer token is essential for securely managing access to APIs, allowing for robust authentication mechanisms while maintaining a stateless, scalable architecture.

> 📘 _Note_
> 
> _This section explains the process of generating the bearer token via the Postman application. You may use other platforms to generate the bearer token, if applicable._

To generate the bearer token via the Postman application, follow the instructions as explained in the following procedure. 

1. Launch the Postman application or log in into your Postman account. If you have selected the online version, make sure to activate your account.

> 💡 Tip
> 
> If you do not have the Postman application, you can download it [here](https://www.postman.com/downloads/) or register for an online Postman account, respectively.

1. After successfully logging in, on your workspace toolbar, select **New** > **HTTP** . Alternatively, on your workspace, select **+** tab to add a new HTTP request tab. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/93a14a1a00ff5ad67a4e5ad4a74677828b0e364b445c378ee24cd5795fe6acd5-New_HTTP_request_option.png",
        "",
        "Creating new HTTP request in Postman"
      ],
      "align": "center",
      "border": true,
      "caption": "Creating new HTTP request in Postman"
    }
  ]
}
[/block]


2. In the new request tab that opens, from the left dropdown menu, select **POST** and enter the following URL in the **Enter request URL** field.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/ab6a0e55d341d8aaf0cddbe95208ebc3c035155faeb32dd652bf011f79369dec-Postman_dropdown.png",
        "",
        "Entering URL"
      ],
      "align": "center",
      "border": true,
      "caption": "Entering URL"
    }
  ]
}
[/block]


3. Now, select the **Body** tab and then click the **x-www-form-urlencoded** option. In the table that appears, enter the following key-value pairs in the **KEY** column:

- **client_id**
- **client_secret**
- **grant_type**

After, in the VALUE column, enter the credentials generated via the [SAPIENT API Credentials](https://docs.intersoftsapient.net/docs/create-api-credentials) functionality. For the **grant_type** key, set the value to **client-credentials**. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/ca361ef126d7b2b88c83d9c6b38ae3e56a4e1d5a0e38b0beed057fc05b86067c-Adding_key_value_pairs.png",
        null,
        "Adding keys value pairs"
      ],
      "align": "center",
      "border": true,
      "caption": "Adding keys value pairs"
    }
  ]
}
[/block]


5. After entering the necessary information, select **Send**.

<!----->

5. If the credentials match the ones that have been set in the **Create API Credentials** functionality, then the bearer token is returned in the response.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/b8499e2-image.png",
        null,
        "Bearer token response example"
      ],
      "align": "center",
      "border": true,
      "caption": "Bearer token response example"
    }
  ]
}
[/block]


7. The **expires in** value returned in the preceding token response is the amount of time the token is valid in seconds (that is, 3600 seconds = 60 minutes).

> 🚧 _Important_
> 
> _Please ensure you cache the authentication token and check for expiry before requesting a new one._

8. You can use the generated bearer token provided in the [API References](https://docs.intersoftsapient.net/reference/get_v4-shippingaccounts) section for testing purposes.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/c67152f-image.png",
        null,
        "Sample bearer token"
      ],
      "align": "center",
      "sizing": "50% ",
      "border": true,
      "caption": "Bearer token sample"
    }
  ]
}
[/block]


Once the bearer token has been generated successfully, you can now use it for authentication purposes.