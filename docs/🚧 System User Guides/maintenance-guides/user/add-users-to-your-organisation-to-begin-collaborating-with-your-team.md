---
title: Add user
excerpt: >-
  Adding a user involves creating a new account within the system for
  individuals who will be involved in shipping operations. This process includes
  assigning roles and permissions appropriate to their responsibilities
deprecated: false
hidden: false
icon: fad fa-user-plus
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
The main purpose of adding users is to enhance collaboration among various departments, ensuring efficient communication and coordination in logistics operations. It established accountability by tracking users actions, thereby promoting responsibility.

Moreover, different roles and permissions improve security by restricting access to sensitive information, while also allowing for a customised user experience.

> 📘 *Note*
>
> *You cannot add or manage users via API.*

In SAPIENT, users with the Admin role can add users and assign them specific roles and permissions. To add users in SAPIENT, follow the steps explained in the following procedure.

1. In the left navigation panel, select **Users**.

<Image align="center" alt="Accessing users" border={true} caption="Accessing users" src="https://files.readme.io/dda0e89b323a4d869472cc629a9fc0349403f8ba24930ac43a31a8f9a7542929-Users_option.png" />

2. On the **Users** page that appears, select the **Add User** button.

<Image align="center" alt="Selecting option to add user" border={true} caption="Selecting option to add user" src="https://files.readme.io/5dd3caded45f180a719da8bad14bebe550fa87a1a49abe4dd32d6ac541979509-Add_users_button.png" />

3. On the **Add User** form that opens, In the **USER TYPE** block, from the **Type of User** dropdown, select the user type from the list of available ones.

<Image align="center" alt="Specifying user type" border={true} caption="Specifying user type" src="https://files.readme.io/bb66dcbf937dc36953a8242a21580c7d67c3e4d804f438040b8aecdebe3defe5-User_type_block.png" width="400px" />

4. In the **CUSTOMER DETAILS** block, from the **Location** dropdown, select the location of the user from the list of available ones. Optionally, you can turn on/off the **Restrict to own shipments** toggle, enabling the users to do the following:

* **Toggle on**: view, manage, and interact with <Glossary>shipments</Glossary> that they have personally created or are directly responsible for it.
* **Toggle off** (a default state): gain access to view and manage all shipments within the system. However, If the user is assigned to a customer account, then with the toggle turned off, the user will be able to view shipments for their own customer account only, not all shipments in the system.

<Image align="center" alt="Entering customer details" border={true} caption="Entering customer details" src="https://files.readme.io/5c3b0190d7620a52e992ee8a9f1e82aa374d36c20b2394ff4c64531b2ad888f3-Customer_details_block.png" width="400px" />

5. In the **USER DETAILS** block, enter the necessary information as explained in the following table.

<Image align="center" alt="Entering user details" border={true} caption="Entering user details" src="https://files.readme.io/4cf9c1127ab7a7b23af6107408ed6fc0e7500f1bacef3af2f2a51ad15c3be18e-User_details_block.png" width="400px" />

<AsteridkForMandatoryElements />

|       Element       | Description                                                                                                                                                    |
| :-----------------: | :------------------------------------------------------------------------------------------------------------------------------------------------------------- |
|  **Upload Avatar**  | Drag the image that you want to upload to this block, or simply click the upload (cloud) icon to select the images from the desired location on your computer. |
| **Email Address\*** | Enter a valid email address that is accessible to the user you are adding.                                                                                     |
|  **Display Name\*** | Enter the display name for the user you are adding.                                                                                                            |
|  **Contact Number** | Enter a valid contact number that is accessible to the user you are adding.                                                                                    |

6. Now, after entering the user details, in the **PERMISSIONS** block, next to each permission, turn the toggle on to assign the necessary permission to the user you are adding.

<Image align="center" alt="Assigning permissions" border={true} caption="Assigning permissions" src="https://files.readme.io/2ed27a48c71de0cb667898056414d5f35d0fef1e4ba93113f74a641dddc8b13a-Permissions_block.png" width="400px" />

In SAPIENT, you can assign the following user types or permissions to the users:

* **Carrier accounts Administrator**: a user type with the ability to manage carrier accounts for all assigned  <Glossary>carrier</Glossary>(s).
* **Customer Configuration Manager**: a user type with the ability to update settings relating to the customer.
* **User Administrator**: a user type with the ability to manage website users.
* **History access**:  a permission that allows access to previous <Glossary>shipments</Glossary> and manifests.
* **Shipment Manifesting**: a permission that allows to <Glossary>manifest</Glossary> the shipments via the SAPIENT UI.

> 📘 *Note*
>
> *The availability of the permissions may vary based on the selected location of the user*.

7. After entering all the necessary user details, select the **Add User** button.

Once done, the new user is created successfully and a corresponding success message displays in the **Add User** dialog. From the dialog, you can either choose to continue editing the user or go back to the **Users** list.

<Image align="center" alt="Confirmation message" border={true} caption="Confirmation message" src="https://files.readme.io/8d8f9b98121ae25f8892d3079beff6342030746c83ec67bf5ae55a3166688ce4-Add_user_confirmation_dialog.png" width="350px" />

After the user is added, a confirmation is sent to the specified email address. Once the user confirms it and set their user credentials (username and password), the status of the user account is set to **Active**.

> 🚧 *Important*
>
> *The Admin user has the access to all functionalities, but an Administrator, Lead or Operator must be assigned to different permissions. Whether the user has accepted the invite or not, you can quickly update their roles and permissions straight from the**Users** tab on the **Edit User** page. Make your choice and select the **Save Changes** button to update your changes.*
>
> For more information on the user role and access permissions, refer to the [role-based access to SAPIENT actions](https://docs.intersoftsapient.net/docs/sapient-user-roles-and-permissions#/) section.