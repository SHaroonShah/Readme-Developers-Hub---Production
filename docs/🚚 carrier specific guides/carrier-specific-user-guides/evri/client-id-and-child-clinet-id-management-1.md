---
title: Add child client department to parent shipping account
excerpt: >-
  A child client department is a sub-account associated with the parent shipping
  account. This structure allows SAPIENT to create separate accounts for
  different departments, teams, or locations while maintaining central control
  under a primary parent account.
deprecated: false
hidden: false
icon: 😀
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
In SAPIENT, unlike other carriers, EVRi customers can have a main (parent) <Glossary>shipping account</Glossary> and may choose to have multiple sub-accounts under the main account. For example, if the customers want to ship multiple different brands, enabling different departments, branches, or teams to manage their shipping needs independently while still being governed by a central administration.

To add the child client department to the EVRi's parent shipping account, follow the steps as explained in the following procedure.

1. In the left navigation panel, select **Shipping Accounts**.

<Image align="center" alt="Accessing shipping accounts" border={true} caption="Accessing shipping accounts" src="https://files.readme.io/3e60281b3dfe72e1d825e37b48a9dbcb8a5446f083dc00aa30b8189f109e58dc-Shipping_account_option.png" />

2. In the **Shipping Accounts** page that appears, in the table, select the EVRi shipping account to which you want to add the child client department.

<Image align="center" border={true} caption="Selecting EVRi shipping account" src="https://files.readme.io/5c7b97571f4faf1a56e4084cf6216305a6215cf5fc95b824a38466f0ea9dfdd2-Selecting_EVRi_shipping_account.png" />

3. In the **View Shipping Account \[Account Name]** page that opens, in the **CARRIER DETAILS** block, select ![](https://files.readme.io/1a04f65a02853417ac0ba36c0771ed4e9c07f508e5e3b7ee7423d7a572aeba18-Child_client_departments_button.png).

<Image align="center" border={true} caption="Accessing option to view child client departments" src="https://files.readme.io/b426866fc50d28daa7c738c1c9fef6c88d45fb993b37f57b742e83e40fa4b1a7-Accesisng_option_to_view_child_client_departments.png" />

4. In the **Child Client Departments** page that opens, select select ![](https://files.readme.io/a5634b2e65393faf626f20ce0e94e629ef718bff94a1dd808e0acdf74a0b4314-Add_child_client_departments_button.png).

<Image align="center" border={true} caption="Selecting option to add child client department" src="https://files.readme.io/576751ba28c641b484d85cbea8a3f3f7bfd3eafc2a21dc3408b18441d9f686f5-Selecting_option_to_add_child_client_department.png" />

5. In the **Add Child Client Department** form that opens, enter the necessary information as explained in the following table.

<Image align="center" border={true} caption="Adding child client department" src="https://files.readme.io/7349a7086efc76c3d5cffdaaf65b671a702cc733d090a03688277c701e833ea4-Adding_child_client_department.png" width="400px" />

<AsteridkForMandatoryElements />

<Table align={["center","left"]}>
  <thead>
    <tr>
      <th>
        Element
      </th>

      <th>
        Description
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        **Shipping Account Name**\*
      </td>

      <td>
        Represents the name of the carrier account in the read-only mode for which you want to add the child client department.
      </td>
    </tr>

    <tr>
      <td>
        **Child Client Id**\*
      </td>

      <td>
        Enter your 3-digit client ID that you want to associate with the parent shipping account.
      </td>
    </tr>

    <tr>
      <td>
        **Child Client Name**\*
      </td>

      <td>
        Enter the name of the client that you are associating with the parent shipping account.
      </td>
    </tr>

    <tr>
      <td>
        **SMS Alert Group Code**
      </td>

      <td>
        Enter the SMS group code if you wish you receive delivery updates via SMS.

        *`Note`: This is an optional field. If you provide this information, make sure to enable the SMS service enhancement in your[Create Shipment request](https://docs.intersoftsapient.net/reference/post_v4-shipments-evri#/).*
      </td>
    </tr>
  </tbody>
</Table>

6. After entering all the required information, select ![](https://files.readme.io/0db8af6a214edf8388a6fe90740721c220967596413a59cddb80e7cc96b07b19-Add_child_client_department_button_2.png).

Once done, the child client department is successfully added to your parent shipping account. You can now start using it in your create shipment requests.

<Callout icon="💡" theme="default">
  ### *Tip*

  *You can link more than one child client department to your parent shipping account. To do that, repeat the steps as explained in the preceding procedure.*
</Callout>