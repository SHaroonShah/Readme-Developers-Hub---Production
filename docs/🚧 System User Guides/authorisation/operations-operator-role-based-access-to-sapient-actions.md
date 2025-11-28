---
title: Operations operator role-based access to SAPIENT actions
excerpt: >-
  Access to SAPIENT options and features varies by organisational role. Explore
  detailed permissions for UI access and maintenance functionality across
  different user roles.
deprecated: false
hidden: false
icon: fad fa-users-between-lines
metadata:
  robots: index
---
Access to SAPIENT options and features varies and depends on your role within the organisation. The following sections detail recommended roles and permissions for each functionality in SAPIENT.

<Callout icon="💡" theme="default">
  ### _Tip_

  _To make reviewing permissions more convenient, it is helpful to understand the following information:_

  * **✅** _indicates the user role has access to the functionality_
  * **⛔** _indicates the user role does not have access to the functionality_
  * _Roles can be combined to provide users with the specific permissions they need_
  * _Contact your system administrator to modify role assignments and permissions_
</Callout>

<Tabs>
  <Tab title="SAPIENT User Interface Access"> <br></br>
    <Accordion title="Carrier Accounts Administrator" icon="user-cog">
      **Role Description:** Can configure any carrier they are assigned to

      **Permissions:**

      * ✅ Home page
      * ⛔ Shipment search
      * ⛔ View shipments
      * ⛔ View manifest history
      * ⛔ View cancelled shipments
      * ⛔ View held shipments
      * ⛔ Manifesting
    </Accordion>

    <Accordion title="User Administrator" icon="users-cog">
      **Role Description:** Can manage website users

      **Permissions:**

      * ✅ Home page
      * ⛔ Shipment search
      * ⛔ View shipments
      * ⛔ View manifest history
      * ⛔ View cancelled shipments
      * ⛔ View held shipments
      * ⛔ Manifesting
    </Accordion>

    <Accordion title="Customer Configuration Manager" icon="cogs">
      **Role Description:** Can access and update settings related to the customer

      **Permissions:**

      * ✅ Home page
      * ⛔ Shipment search
      * ⛔ View shipments
      * ⛔ View manifest history
      * ⛔ View cancelled shipments
      * ⛔ View held shipments
      * ⛔ Manifesting
    </Accordion>

    <Accordion title="History Access" icon="history">
      **Role Description:** A permission to gain access to past shipments and manifests

      **Permissions:**

      * ✅ Home page
      * ✅ Shipment search
      * ✅ View shipments
      * ✅ View manifest history
      * ⛔ View cancelled shipments
      * ⛔ View held shipments
      * ⛔ Manifesting
    </Accordion>

    <Accordion title="Shipment Manifesting" icon="clipboard-list">
      **Role Description:** A permission to manifest the shipments via the UI

      **Permissions:**

      * ✅ Home page
      * ⛔ Shipment search
      * ⛔ View shipments
      * ⛔ View manifest history
      * ✅ View cancelled shipments
      * ✅ View held shipments
      * ✅ Manifesting
    </Accordion>
  </Tab>

  <Tab title="Maintenance Functionality Access"><br></br>
    <Accordion title="Carrier Accounts Administrator" icon="user-cog">
      **Role Description:** Can configure any carrier they are assigned to

      **Customer Management:**

      * ⛔ View Customers
      * ⛔ Customer onboarding wizard
      * ⛔ View customer details
      * ⛔ Edit customer details
      * ⛔ Delete customer
      * ⛔ View customer users

      **Location & Account Management:**

      * ✅ View shipping locations
      * ⛔ Add shipping location
      * ⛔ View location users
      * ✅ Edit shipping location
      * ✅ Link existing shipping account
      * ✅ View shipping accounts
      * ✅ Edit shipping account
      * ✅ Delete account
      * ✅ Refresh account status
      * ✅ Add shipping account

      **Billing & Services:**

      * ✅ View billing departments
      * ✅ View service contracts

      **Products & Integrations:**

      * ⛔ Add product
      * ⛔ Lists products
      * ⛔ Edit product
      * ⛔ Delete product
      * ⛔ Integrations

      **Other:**

      * ⛔ View Held shipments
    </Accordion>

    <Accordion title="User Administrator" icon="users-cog">
      **Role Description:** Can manage website users

      **Permissions:** This role has no access to maintenance functionality features.

      All maintenance functions are restricted (⛔) for this role.
    </Accordion>

    <Accordion title="Customer Configuration Manager" icon="cogs">
      **Role Description:** Can access and update settings related to the customer

      **Customer Management:**

      * ⛔ View Customers
      * ⛔ Customer onboarding wizard
      * ⛔ View customer details
      * ⛔ Edit customer details
      * ⛔ Delete customer
      * ⛔ View customer users

      **Location Management:**

      * ✅ View shipping locations
      * ✅ Add shipping location
      * ✅ View location users
      * ✅ Edit shipping location

      **Account Management:**

      * ⛔ Link existing shipping account
      * ⛔ View shipping accounts
      * ⛔ Edit shipping account
      * ⛔ Delete account
      * ⛔ Refresh account status
      * ⛔ Add shipping account

      **Products & Integrations:**

      * ✅ Add product
      * ✅ Lists products
      * ✅ Edit product
      * ✅ Delete product
      * ✅ Integrations

      **Other:**

      * ⛔ View Held shipments
      * ⛔ View billing departments
      * ⛔ View service contracts
    </Accordion>

    <Accordion title="History Access" icon="history">
      **Role Description:** A permission to gain access to past shipments and manifests

      **Customer Management:**

      * ✅ View Customers
      * ✅ Customer onboarding wizard
      * ✅ View customer details
      * ✅ Edit customer details
      * ⛔ Delete customer
      * ⛔ View customer users

      **Other Permissions:**
      All other maintenance functionality features are restricted (⛔) for this role, including location management, account management, products, and integrations.
    </Accordion>

    <Accordion title="Shipment Manifesting" icon="clipboard-list">
      **Role Description:** A permission to manifest the shipments via the UI

      **Permissions:** This role has no access to maintenance functionality features.

      All maintenance functions are restricted (⛔) for this role.
    </Accordion>
  </Tab>
</Tabs>
