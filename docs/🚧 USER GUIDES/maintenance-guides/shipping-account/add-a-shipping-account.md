---
title: Add Shipping Account
excerpt: >-
  Learn how to create and configure shipping accounts in SAPIENT by assigning
  carrier credentials and linking them to shipping locations.
deprecated: false
hidden: false
icon: fad fa-square-plus
link:
  new_tab: false
metadata:
  title: ''
  description: >-
    A _shipping account_ is a specific account set up with a shipping carrier or
    logistics provider that enables businesses to manage shipping activities.
  robots: index
---
In SAPIENT, you can create a shipping account, assign your carrier credentials to it, and then link them to the relevant shipping location(s).

<Accordion title="Prerequisites" icon="info-circle">

**Admin Role Required**: Users with the **Admin** role permissions can create unlimited shipping accounts for their customers.

</Accordion>

## Step-by-Step Process

<Tabs>
<Tab title="Access Shipping Accounts">

1. In the left navigation panel, select **Shipping Accounts**.

<Image align="center" alt="Accessing shipping accounts" border={true} caption="Accessing shipping accounts" src="https://files.readme.io/3e60281b3dfe72e1d825e37b48a9dbcb8a5446f083dc00aa30b8189f109e58dc-Shipping_account_option.png" />

2. On the **Shipping Accounts** page that opens, select the **Add Shipping Account** button.

<Image align="center" alt="Accessing option to add shipping account" border={true} caption="Selecting option to add shipping account" src="https://files.readme.io/8490d8ba65c4eca10caa8c051c5e73bf366fc5a6269e84a2bfb697544105b343-Add_shipping_account_option.png" />

</Tab>
<Tab title="Account Details">

3. On the **Add Shipping Account** form that appears, fill in the **ACCOUNT DETAILS** block:

<Image align="center" alt="Entering account details" border={true} caption="Entering account details" src="https://files.readme.io/dc5c99c4576f2625aa7809d67c9cf26573ed44dbce51fdebc2df7f43013cde3b-Account_details_block.png" />

### Required Fields

| Element | Description |
|---------|-------------|
| **Carrier*** | From the dropdown list, select the carrier for which you want to add a shipping account |
| **Shipping Location*** | From the dropdown menu, select the location that you want to assign to the shipping account you are creating |

*Required fields are marked with an asterisk (*)

</Tab>
<Tab title="Shipping Account Details">

4. In the **SHIPPING ACCOUNT** block, enter the necessary information:

<Image align="center" alt="Specifying shipping account details" border={true} caption="Specifying shipping account details" src="https://files.readme.io/86c792139df738b9d3d72e61e3a2d9edf6e95e49ebaed402137335a66e796d4a-Shipping_account_block.png" width="400px" />

<Accordion title="Shipping Account Fields" icon="list">

### Account Configuration

| Element | Description |
|---------|-------------|
| **Carrier Account Number*** | Enter the carrier account number. The format must be compliant with your selected carrier. Add leading zeros if needed to meet character length requirements |
| **Account Type*** | Select either **Production** (live environment) or **Sandbox** (testing environment) |
| **Account Name*** | Enter the account name if different from customer name |
| **Registered Email Address*** | Enter the email address used to register with the carrier |
| **Registered Billing Postcode** | Enter the postcode for billing (optional) |

### Contact Information

| Element | Description |
|---------|-------------|
| **Alias*** | Enter a memorable custom name for API requests instead of using shipping location ID |
| **Contact Name*** | Enter the primary contact name for this account |
| **Contact Number*** | Enter the contact phone number for this account |

*Required fields are marked with an asterisk (*)

</Accordion>

</Tab>
<Tab title="Carrier-Specific Details">

5. In the **CARRIER DETAILS** block, complete the carrier-specific fields.

<Callout icon="💡" theme="info">
**Important**: The fields in this section vary depending on your selected carrier. Each carrier has unique requirements and authentication methods.
</Callout>

<Cards columns={2}>
<Card title="Get Carrier Guides" href="https://docs.intersoftsapient.net/docs/carrier-specific-user-guides" icon="truck">
Access detailed guides for each supported carrier including field requirements and setup instructions.
</Card>
<Card title="Account Types" href="https://docs.intersoftsapient.net/docs/sandbox-account" icon="cogs">
Learn about the differences between Production and Sandbox environments.
</Card>
</Cards>

6. After entering all required information, select **Add Shipping Account**.

</Tab>
</Tabs>

## Next Steps

<Accordion title="What's Next?" icon="arrow-right">

Once you've successfully added your shipping account, you can:

- [Add a shipping location](https://docs.intersoftsapient.net/docs/add-a-shipping-location) to your new shipping account
- Configure additional carrier settings
- Test your account in the sandbox environment before going live

</Accordion>

## API Management

<Callout icon="📘" theme="info">
**API Access**: Shipping accounts can also be added and managed via API. For more information, refer to the [API References](https://docs.intersoftsapient.net/reference/get_v4-shippingaccounts) section.
</Callout>