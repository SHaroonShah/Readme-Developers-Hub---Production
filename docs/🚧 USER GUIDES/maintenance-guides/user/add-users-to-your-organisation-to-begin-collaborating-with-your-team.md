---
title: Add user
excerpt: >-
  Adding a user involves creating a new account within the system for
  individuals who will be involved in shipping operations. This process includes
  assigning roles and permissions appropriate to their responsibilities
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
The main purpose of adding users is to enhance collaboration among various departments, ensuring efficient communication and coordination in logistics operations. It established accountability by tracking users actions, thereby promoting responsibility.

Moreover, different roles and permissions improve security by restricting access to sensitive information, while also allowing for a customised user experience. 

> 📘 _Note_
> 
> _You cannot add or manage users via API._

In SAPIENT, users with the Admin role can add users and assign them specific roles and permissions. To add users in SAPIENT, follow the steps explained in the following procedure.

1. In the left navigation panel, select **Users**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/dda0e89b323a4d869472cc629a9fc0349403f8ba24930ac43a31a8f9a7542929-Users_option.png",
        "",
        "Accessing users"
      ],
      "align": "center",
      "border": true,
      "caption": "Accessing users"
    }
  ]
}
[/block]


2. On the **Users** page that appears, select the **Add User** button.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/5dd3caded45f180a719da8bad14bebe550fa87a1a49abe4dd32d6ac541979509-Add_users_button.png",
        "",
        "Selecting option to add user"
      ],
      "align": "center",
      "border": true,
      "caption": "Selecting option to add user"
    }
  ]
}
[/block]


3. On the **Add User** form that opens, In the **USER TYPE** block, from the **Type of User** dropdown, select the user type from the list of available ones.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/bb66dcbf937dc36953a8242a21580c7d67c3e4d804f438040b8aecdebe3defe5-User_type_block.png",
        "",
        "Specifying user type"
      ],
      "align": "center",
      "sizing": "400px",
      "border": true,
      "caption": "Specifying user type"
    }
  ]
}
[/block]


4. In the **CUSTOMER DETAILS** block, from the **Location** dropdown, select the location of the user from the list of available ones. Optionally, you can turn on/off the **Restrict to own shipments** toggle, enabling the users to do the following: 

- **Toggle on**: view, manage, and interact with <<glossary:shipments>> that they have personally created or are directly responsible for it.
- **Toggle off** (a default state): gain access to view and manage all shipments within the system. However, If the user is assigned to a customer account, then with the toggle turned off, the user will be able to view shipments for their own customer account only, not all shipments in the system.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/5c3b0190d7620a52e992ee8a9f1e82aa374d36c20b2394ff4c64531b2ad888f3-Customer_details_block.png",
        "",
        "Entering customer details"
      ],
      "align": "center",
      "sizing": "400px",
      "border": true,
      "caption": "Entering customer details"
    }
  ]
}
[/block]


5. In the **USER DETAILS** block, enter the necessary information as explained in the following table. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/4cf9c1127ab7a7b23af6107408ed6fc0e7500f1bacef3af2f2a51ad15c3be18e-User_details_block.png",
        "",
        "Entering user details"
      ],
      "align": "center",
      "sizing": "400px",
      "border": true,
      "caption": "Entering user details"
    }
  ]
}
[/block]


<AsteridkForMandatoryElements />

|       Element       | Description                                                                                                                                                    |
| :-----------------: | :------------------------------------------------------------------------------------------------------------------------------------------------------------- |
|  **Upload Avatar**  | Drag the image that you want to upload to this block, or simply click the upload (cloud) icon to select the images from the desired location on your computer. |
| **Email Address\*** | Enter a valid email address that is accessible to the user you are adding.                                                                                     |
|  **Display Name\*** | Enter the display name for the user you are adding.                                                                                                            |
|  **Contact Number** | Enter a valid contact number that is accessible to the user you are adding.                                                                                    |

6. Now, after entering the user details, in the **PERMISSIONS** block, next to each permission, turn the toggle on to assign the necessary permission to the user you are adding. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/2ed27a48c71de0cb667898056414d5f35d0fef1e4ba93113f74a641dddc8b13a-Permissions_block.png",
        "",
        "Assigning permissions"
      ],
      "align": "center",
      "sizing": "400px",
      "border": true,
      "caption": "Assigning permissions"
    }
  ]
}
[/block]


In SAPIENT, you can assign the following permissions to the users: 

- **Carrier accounts Administrator**: to manage carrier accounts for all assigned  <<glossary:carrier>>(s).
- **Customer Configuration Manager**: to update settings relating to the customer.
- **History access**:  access to previous <<glossary:shipments>> and manifests.
- **Shipment Manifesting**: to <<glossary:manifest>> the shipments via the SAPIENT UI.
- **User Administrator**: to manage website users.

> 📘 _Note_
> 
> _The availability of the permissions may vary based on the selected location of the user_.

7. After entering all the necessary user details, select the **Add User** button.

Once done, the new user is created successfully and a corresponding success message displays in the **Add User** dialog. From the dialog, you can either choose to continue editing the user or go back to the **Users** list.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/8d8f9b98121ae25f8892d3079beff6342030746c83ec67bf5ae55a3166688ce4-Add_user_confirmation_dialog.png",
        "",
        "Confirmation message"
      ],
      "align": "center",
      "sizing": "350px",
      "border": true,
      "caption": "Confirmation message"
    }
  ]
}
[/block]


 After the user is added, a confirmation is sent to the specified email address. Once the user confirms it and set their user credentials (username and password), the status of the user account is set to **Active**.

> 🚧 _Important_
> 
> _The Admin user has the access to all functionalities, but an Administrator, Lead or Operator must be assigned to different permissions. Whether the user has accepted the invite or not, you can quickly update their roles and permissions straight from the **Users** tab on the **Edit User** page. Make your choice and select the **Save Changes** button to update your changes._