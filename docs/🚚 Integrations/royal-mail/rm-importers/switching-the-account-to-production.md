---
title: Set up your Production Shipping Account
deprecated: false
hidden: false
icon: fad fa-arrow-up-right-dots
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
After your [Test Pack](https://docs.intersoftsapient.net/docs/royal-mail-importers-sandbox-test-pack) has been approved, you can set up a separate Production Shipping Account.  <br /><br />Keep your Sandbox Shipping Account for testing. Do not change it to Production.

## How to set up your Production Shipping Account

Complete the steps below to create and set up your Production Shipping Account.

<ToggleList>
  <ToggleListItem title="1. Create your Production Shipping Account">

    <br />

    Create a new Royal Mail [Shipping Account](https://docs.intersoftsapient.net/docs/add-a-shipping-account) and set the Account Type to Production. Enter your Production Royal Mail account details:

- Royal Mail Account Number
- Posting Location Number (PLN)
- Registered Email Address
- Registered Billing Postcode

The Registered Email Address must be the email address used to access your Royal Mail Online Business Account (OBA).

See [Set up Royal Mail Shipping Account](https://docs.intersoftsapient.net/docs/shipping-account-requirements) for more information about these fields.

    > 🚧 *Important*
    >
    > *Enter your Posting Location Number Postcode in the **Shipping Location** details in SAPIENT. The postcode must match the Posting Location Number Postcode in your Royal Mail OBA.* 

    ***
  </ToggleListItem>

  <br />

  <ToggleListItem title="2. Validate your Production Shipping Account">

    <br />

    After you create your Production Shipping Account, SAPIENT automatically sends the account details to the Royal Mail OBA API for validation. Royal Mail will either accept or reject the details provided.

    ***
  </ToggleListItem>

  <br />

  <ToggleListItem title="3. Check the account status">

    <br />

    If Royal Mail accepts the account details, the **Account Status** changes from **Pending** to **Enabled**.

If the details are rejected, the **Account Status** remains **Pending**. Check your Royal Mail account details, correct any incorrect information, and submit the request again.

You cannot use the **Production** Shipping Account until the Account Status is **Enabled**.

    <Callout icon="💡" theme="default">
      ### *Tip*

      *Keep your existing **Sandbox Shipping Account** for testing. Your new Production Shipping Account is separate from your Sandbox Shipping Account.*
    </Callout>

    ***
  </ToggleListItem>

  <br />

  <ToggleListItem title="4. Set up International Arrival Containers">

    <br />

    If you are a Freight 2 Post customer, ensure that [International Arrival Containers (A-scan)](https://docs.intersoftsapient.net/docs/add-barcode-range-for-international-arrival-containers) is set up with valid details provided to you by INTERSOFT Onboarding team.

    ***
  </ToggleListItem>

  <br />

  <ToggleListItem title="5. Complete label sign off">

    <br />

    After this, you can proceed with the **label sign off** required by Royal Mail. The sign off depends on what type of Royal Mail customer you are:

    * **Royal Mail importers using Commercial Clearance route and Tracked High Volume customers**: involves physical label sign off—where you are requested to create couple of labels, manifest them, print them out using your production printers and ship them to Royal Mail for review and quality testing.
    * **Royal Mail importers using Freight 2 Post route**: involves CDS checks as well as physical label sign off. For CDS checks, you are requested to create a couple of <Glossary>labels</Glossary>, <Glossary>manifest</Glossary> them and share with us the <Glossary>PDF</Glossary>s, so they can be reviewed and signed off before you proceed to the physical label sign off.

    The full details on this are shared with you closer to the date.

    ***
  </ToggleListItem>

  <br />

  <ToggleListItem title="6. Start shipping via Intersoft SAPIENT">

    <br />

    Once the labels are signed off and the go-live action is agreed with Royal Mail, you can start shipping via Intersoft SAPIENT.

    <Callout icon="⚠️" theme="warning">
      ### *Important*

      *Once you go-live any technical issues should be raised directly with our Tech Support team by following the steps listed [here](https://docs.intersoftsapient.net/docs/troubleshooting#/).* *Enquiries regarding addition of the new services, features, and so on should be continued being sent to [onboarding@intersoft.co.uk](mailto:onboarding@intersoft.co.uk).*
    </Callout>
  </ToggleListItem>
</ToggleList>

***

### See also

If you are interested in creating a tracking account for the newly added shipping account, refer to the following sections on how to set up our <Glossary>Tracking Webhook</Glossary> solution:

<Cards>
  <Card title="Tracking Webhook" href="https://docs.intersoftsapient.net/docs/tracking-webhook-1" icon="fa-solid fa-satellite-dish" target="_blank">
    Set up the webhook connection, create tracking account, and much more.
  </Card>

  <Card title="Response examples" href="https://docs.intersoftsapient.net/reference/post_v4-trackings-pushpayloadexample" icon="fa-solid fa-code" target="_blank">
    View response example of the tracking webhook push notification payload, as sent to a customer's webhook when tracking information is received from a carrier.
  </Card>

  <Card title="Royal Mail Tracking Account setup" href="https://docs.intersoftsapient.net/docs/royal-mail-tracking-account-setup" icon="fa-solid fa-truck" target="_blank">
    Set up Royal Mail tracking account.
  </Card>
</Cards>

<Callout icon="📘" theme="info">
  ### _Note_

  _To enable the&#x20;_**_Tracking Webhook_**_&#x20;solution, please contact our&#x20;_[Intersoft Onboarding](mailto:onboarding@intersoft.co.uk)_&#x20;team._
</Callout>