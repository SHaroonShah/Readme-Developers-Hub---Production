---
title: Create API Credentials
excerpt: >-
  _API credentials_ are unique identifiers that are used to authenticate and
  authorise applications or users accessing a web-based service via an
  Application Programming Interface (API).
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
The primary purpose of creating API credentials is to enable secure and controlled access to the functionalities offered by the API, allowing developers to integrate their systems with external services. 

In SAPIENT, you can create you own API credentials with which you can track usage, manage permissions effectively, and protect your data from unauthorised access. 

To create new API credentials, follow the instructions as explained in the following procedure.

1. Log in to the SAPIENT platform using your credentials.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/639e7805edcaa9527380c1d5cd14463e8753cce43eda79ac3ccdd09732e045b2-Sapient_Login_window.png",
        "",
        "Logging into SAPIENT"
      ],
      "align": "center",
      "sizing": "400px",
      "border": true,
      "caption": "Logging into SAPIENT"
    }
  ]
}
[/block]


2. On the **Home** page that opens, in the left navigation panel, select **API** > **Credentials**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/d293d6725e51d7d9aefd357ce17c120786c04f72132f6751c0051aa2fcacdd76-Credentials_option.png",
        "",
        "Accessing API credentials"
      ],
      "align": "center",
      "border": true,
      "caption": "Accessing API credentials"
    }
  ]
}
[/block]


3. On the **API Credentials** page that appears, select the **Create API Credentials** button. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/94c18d9f5d3e5c663beae626b71b6bd8bd0d72614e7d70cb57905b252570c20e-Create_API_Credentials_button.png",
        "",
        "Selecting option to create API credentials"
      ],
      "align": "center",
      "caption": "Selecting option to create API credentials"
    }
  ]
}
[/block]


> 📘 _Note_
> 
> _You are only required to create these credentials the first time you log in_.

4. In the **Create API Credentials** dialog that opens, enter a brief memorable name for your API credential and select **Create**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/b15de257efd0a5495ae25acad8252acf0173f3a48bce625c4e5e4a9c461a7811-Create_API_Credentials_dialog.png",
        "",
        "Creating API credentials"
      ],
      "align": "center",
      "sizing": "400px",
      "border": true,
      "caption": "Creating API credentials"
    }
  ]
}
[/block]


5. In the **API Credentials** dialog that appears, copy the generated **Client ID** and **Secret**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/2792065801168e1bbda76a6bdae6035bf62a1d53d16fd27b2e49b72b2d199746-API_Credentials_dialog.png",
        "",
        "Saving client ID and secret"
      ],
      "align": "center",
      "sizing": "400px",
      "border": true,
      "caption": "Saving client ID and secret"
    }
  ]
}
[/block]


> 🚧 _Important_
> 
> _Make sure you copy the **Secret** and keep it safe as we do not store this anywhere within the application and you are not able to see it again. If you lose the secret, you are required to create a new set of credentials._

6. After copying the client ID and secret, select **Close**.

Once done, the new API credentials are created successfully and appear in the **CURRENT API CREDENTAILS** table of the **API Credentials** page. You can now use these credentials when initiating an API request to authenticate each call made to the API.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/282a98da9661dd060294cc5dcb0019d061b7a756357f81147fe765cac8a22217-API_credentials_created.png",
        "",
        "Newly created API credentials"
      ],
      "align": "center",
      "border": true,
      "caption": "Newly created API credentials"
    }
  ]
}
[/block]