---
title: Operations operator role-based access to SAPIENT actions
excerpt: >-
  Access to SAPIENT options and features varies by organizational role. Explore
  detailed permissions for UI access and maintenance functionality across
  different user roles.
deprecated: false
hidden: false
icon: fad fa-users-between-lines
link:
  new_tab: false
metadata:
  description: >-
    Acess to SAPIENT options and features varies and depends on your role within
    the organisation. A list of recommended and basic roles and permissions are
    explained in detail in the following tables for each functionality in
    SAPIENT. 
  robots: index
---
## Access permissions to SAPIENT user interface

| User role                                                                                   | Home page | Shipment search | View shipments | View manifest history | View cancelled shipments | View held shipments | Manifesting |
| :------------------------------------------------------------------------------------------ | :-------- | :-------------- | :------------- | :-------------------- | :----------------------- | :------------------ | :---------- |
| **Carrier Accounts Administrator** (Can configure any carrier they are assigned to)         | ✅         | ⛔               | ⛔              | ⛔                     | ⛔                        | ⛔                   | ⛔           |
| **User Administrator** (can manage website users)                                           | ✅         | ⛔               | ⛔              | ⛔                     | ⛔                        | ⛔                   | ⛔           |
| **Customer Configuration Manager** (can access and update settings related to the customer) | ✅         | ⛔               | ⛔              | ⛔                     | ⛔                        | ⛔                   | ⛔           |
| **History Access** (a permission to gain access to past shipments and manifests)            | ✅         | ✅               | ✅              | ✅                     | ⛔                        | ⛔                   | ⛔           |
| **Shipment Manifesting** (a permission to manifest the shipments via the UI)                | ✅         | ⛔               | ⛔              | ⛔                     | ✅                        | ✅                   | ✅           |

## Access permissions to maintenance functionality

<br />

| User role/permission                                                                        | View Customers | Customer onboarding wizard | View customer details | Edit customer details | Delete customer | View Held shipments | View customer users | View shipping locations | Add shipping location | View location users | Edit shipping location | Link existing shipping account | View shipping accounts | Edit shipping account | Delete account | Refresh account status | View billing departments | View service contracts | Add shipping account | Add product | Lists products | Edit product | Delete product | Integrations |
| :------------------------------------------------------------------------------------------ | :------------- | :------------------------- | :-------------------- | :-------------------- | :-------------- | :------------------ | :------------------ | :---------------------- | :-------------------- | :------------------ | :--------------------- | :----------------------------- | :--------------------- | :-------------------- | :------------- | :--------------------- | :----------------------- | :--------------------- | :------------------- | :---------- | :------------- | :----------- | :------------- | :----------- |
| **Carrier Accounts Administrator** (can configure any carrier they are assigned to)         | ⛔              | ⛔                          | ⛔                     | ⛔                     | ⛔               | ⛔                   | ⛔                   | ✅                       | ⛔                     | ⛔                   | ✅                      | ✅                              | ✅                      | ✅                     | ✅              | ✅                      | ✅                        | ✅                      | ✅                    | ⛔           | ⛔              | ⛔            | ⛔              | ⛔            |
| **User Administrator** (can manage website users)                                           | ⛔              | ⛔                          | ⛔                     | ⛔                     | ⛔               | ⛔                   | ⛔                   | ⛔                       | ⛔                     | ⛔                   | ⛔                      | ⛔                              | ⛔                      | ⛔                     | ⛔              | ⛔                      | ⛔                        | ⛔                      | ⛔                    | ⛔           | ⛔              | ⛔            | ⛔              | ⛔            |
| **Customer Configuration Manager** (can access and update settings related to the customer) | ⛔              | ⛔                          | ⛔                     | ⛔                     | ⛔               | ⛔                   | ⛔                   | ✅                       | ✅                     | ✅                   | ✅                      | ⛔                              | ⛔                      | ⛔                     | ⛔              | ⛔                      | ⛔                        | ⛔                      | ⛔                    | ✅           | ✅              | ✅            | ✅              | ✅            |
| **History Access** (a permission to gain access to past shipments and manifests)            | ✅              | ✅                          | ✅                     | ✅                     | ⛔               | ⛔                   | ⛔                   | ⛔                       | ⛔                     | ⛔                   | ⛔                      | ⛔                              | ⛔                      | ⛔                     | ⛔              | ⛔                      | ⛔                        | ⛔                      | ⛔                    | ⛔           | ⛔              | ⛔            | ⛔              | ⛔            |
| **Shipment Manifesting** (a permission to manifest the shipments via the UI)                | ⛔              | ⛔                          | ⛔                     | ⛔                     | ⛔               | ⛔                   | ⛔                   | ⛔                       | ⛔                     | ⛔                   | ⛔                      | ⛔                              | ⛔                      | ⛔                     | ⛔              | ⛔                      | ⛔                        | ⛔                      | ⛔                    | ⛔           | ⛔              | ⛔            | ⛔              | ⛔            |