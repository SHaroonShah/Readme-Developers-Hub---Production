---
title: Add Users to Your Organisation
excerpt: >-
  Learn how to add users to SAPIENT, assign roles and permissions, and manage
  user access for efficient collaboration in shipping operations.
deprecated: false
hidden: false
icon: fad fa-user-plus
link:
  new_tab: false
metadata:
  title: ''
  description: ''
  robots: index
---
<Tabs>
  <Tab title="Overview">
    
## Purpose of Adding Users

The main purpose of adding users is to enhance collaboration among various departments, ensuring efficient communication and coordination in logistics operations. It establishes accountability by tracking users' actions, thereby promoting responsibility.

<Cards columns={2}>
  <Card title="Enhanced Security" icon="shield-alt">
    Different roles and permissions improve security by restricting access to sensitive information while allowing for a customized user experience.
  </Card>
  <Card title="Better Collaboration" icon="users">
    Enable efficient communication and coordination across departments involved in shipping operations.
  </Card>
</Cards>

> 📘 **Important Note**
>
> You cannot add or manage users via API. All user management must be done through the SAPIENT interface.

  </Tab>
  
  <Tab title="Adding Users">
    
## Prerequisites

<Cards>
  <Card title="Required Role" icon="user-shield">
    You must have **Admin** role permissions to add users and assign roles in SAPIENT.
  </Card>
</Cards>

## Step-by-Step Procedure

<Accordion title="Step 1: Access Users Section" icon="arrow-right">

In the left navigation panel, select **Users**.

<Image align="center" alt="Accessing users" border={true} caption="Accessing users" src="https://files.readme.io/dda0e89b323a4d869472cc629a9fc0349403f8ba24930ac43a31a8f9a7542929-Users_option.png" />

</Accordion>

<Accordion title="Step 2: Start Adding User" icon="arrow-right">

On the **Users** page that appears, select the **Add User** button.

<Image align="center" alt="Selecting option to add user" border={true} caption="Selecting option to add user" src="https://files.readme.io/5dd3caded45f180a719da8bad14bebe550fa87a1a49abe4dd32d6ac541979509-Add_users_button.png" />

</Accordion>

<Accordion title="Step 3: Select User Type" icon="arrow-right">

On the **Add User** form that opens, in the **USER TYPE** block, from the **Type of User** dropdown, select the user type from the list of available ones.

<Image align="center" alt="Specifying user type" border={true} caption="Specifying user type" src="https://files.readme.io/bb66dcbf937dc36953a8242a21580c7d67c3e4d804f438040b8aecdebe3defe5-User_type_block.png" width="400px" />

</Accordion>

<Accordion title="Step 4: Configure Customer Details" icon="arrow-right">

In the **CUSTOMER DETAILS** block, from the **Location** dropdown, select the location of the user from the list of available ones. 

**Restrict to Own Shipments Toggle:**
- **Toggle on**: Users can view, manage, and interact with <Glossary>shipments</Glossary> that they have personally created or are directly responsible for
- **Toggle off** (default): Users gain access to view and manage all shipments within the system. If assigned to a customer account, they can only view shipments for their own customer account

<Image align="center" alt="Entering customer details" border={true} caption="Entering customer details" src="https://files.readme.io/5c3b0190d7620a52e992ee8a9f1e82aa374d36c20b2394ff4c64531b2ad888f3-Customer_details_block.png" width="400px" />

</Accordion>

<Accordion title="Step 5: Enter User Details" icon="arrow-right">

In the **USER DETAILS** block, enter the necessary information:

<Image align="center" alt="Entering user details" border={true} caption="Entering user details" src="https://files.readme.io/4cf9c1127ab7a7b23af6107408ed6fc0e7500f1bacef3af2f2a51ad15c3be18e-User_details_block.png" width="400px" />

<AsteridkForMandatoryElements />

| Element | Description |
|---------|-------------|
| **Upload Avatar** | Drag the image to upload or click the upload icon to select from your computer |
| **Email Address*** | Enter a valid, accessible email address for the user |
| **Display Name*** | Enter the display name for the user |
| **Contact Number** | Enter a valid, accessible contact number for the user |

</Accordion>

<Accordion title="Step 6: Assign Permissions" icon="arrow-right">

In the **PERMISSIONS** block, turn on toggles next to each permission to assign necessary permissions to the user.

<Image align="center" alt="Assigning permissions" border={true} caption="Assigning permissions" src="https://files.readme.io/2ed27a48c71de0cb667898056414d5f35d0fef1e4ba93113f74a641dddc8b13a-Permissions_block.png" width="400px" />

> 📘 **Note**: The availability of permissions may vary based on the selected user location.

</Accordion>

<Accordion title="Step 7: Complete User Creation" icon="arrow-right">

After entering all necessary details, select the **Add User** button.

Once completed, a success message displays. You can choose to continue editing the user or return to the **Users** list.

<Image align="center" alt="Confirmation message" border={true} caption="Confirmation message" src="https://files.readme.io/8d8f9b98121ae25f8892d3079beff6342030746c83ec67bf5ae55a3166688ce4-Add_user_confirmation_dialog.png" width="350px" />

</Accordion>

  </Tab>
  
  <Tab title="User Types & Permissions">
    
## Available User Types and Permissions

<Cards columns={2}>
  <Card title="Carrier Accounts Administrator" icon="truck">
    User type with the ability to manage carrier accounts for all assigned <Glossary>carrier</Glossary>(s).
  </Card>
  <Card title="Customer Configuration Manager" icon="cog">
    User type with the ability to update settings relating to the customer.
  </Card>
  <Card title="User Administrator" icon="user-cog">
    User type with the ability to manage website users.
  </Card>
  <Card title="History Access" icon="history">
    Permission that allows access to previous <Glossary>shipments</Glossary> and manifests.
  </Card>
  <Card title="Shipment Manifesting" icon="clipboard-list">
    Permission that allows to <Glossary>manifest</Glossary> shipments via the SAPIENT UI.
  </Card>
</Cards>

## Post-Creation Process

<Accordion title="Email Confirmation & Account Activation" icon="envelope">

After the user is added:
1. A confirmation email is sent to the specified email address
2. The user must confirm the email and set their credentials (username and password)
3. Once confirmed, the user account status is set to **Active**

</Accordion>

<Accordion title="Managing User Permissions" icon="user-shield">

> 🚧 **Important**
>
> The Admin user has access to all functionalities, but Administrator, Lead, or Operator roles must be assigned specific permissions. 
>
> Whether the user has accepted the invite or not, you can update their roles and permissions from the **Users** tab on the **Edit User** page. Make your changes and select **Save Changes** to update.

For detailed information on user roles and access permissions, refer to the [role-based access to SAPIENT actions](https://docs.intersoftsapient.net/docs/sapient-user-roles-and-permissions#/) section.

</Accordion>

  </Tab>
</Tabs>