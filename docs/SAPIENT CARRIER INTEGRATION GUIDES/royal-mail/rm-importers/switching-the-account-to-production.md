---
title: Switch account to production
excerpt: >-
  The switching of the shipping account from **Sandbox** to the **Production**
  environment occurs after thorough testing is completed in the **Sandbox**
  environment, ensuring that all functionalities work as intended, bugs have
  been fixed, and performance is optimised.
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
Following the [Test Pack](https://docs.intersoftsapient.net/docs/royal-mail-importers-sandbox-test-pack) run and approval, and successful UAT (user acceptance test), your account is switched from **Sandbox** to **Production**.

## How to switch account from Sandbox to Production

To set up the Production <Glossary>Shipping Account</Glossary>, perform the steps as explained in the following procedure. 

<ToggleList>
  <ToggleListItem title="1. Edit the shipping account">
    Edit the [Shipping Account](https://docs.intersoftsapient.net/docs/add-a-shipping-account), ensuring that the <Glossary>account type</Glossary> is set to **Production**, and it is prepopulated with the correct Royal Mail account details, Royal Mail Account Number, Posting Location Number (PLN), Registered Email Address (email address used to access your <Glossary>Online Business Account</Glossary> (OBA) to view billing and reporting), and Registered Billing Postcode. For more information on how to fill in the fields, refer to the [Set up Royal Mail Shipping Account.](https://docs.intersoftsapient.net/docs/shipping-account-requirements) section.

    > 🚧 *Important*
    >
    > *Please ensure to enter the Posting Location Number Postcode in the**Shipping Locations** screen in SAPIENT, which must match the Posting Location Number Postcode provided in the Royal Mail OBA.*

    ***
  </ToggleListItem>

  <br />

  <ToggleListItem title="2. Send the OBA API request">
    After switching the Shipping Account to **Production**, an automatic request is sent to the Royal Mail OBA API. Depending on the account details provided, the system either accepts it or rejects it.

    ***
  </ToggleListItem>

  <br />

  <ToggleListItem title="3. Check the account status">
    If the OBA request is accepted, the **Account Status** changes from **Pending** to **Enabled**. Otherwise, it remains in the **Pending** state and you need to go back, fill in the correct Royal Mail account details and send the request again. You will be unable to use the **Production** Shipping Account until the Account Status is **Enabled**.

    <Callout icon="💡" theme="default">
      ### *Tip*

      *The Shipping Account you set up previously stays as the**Sandbox** account type and you can continue using it for testing purposes.*
    </Callout>

    ***
  </ToggleListItem>

  <br />

  <ToggleListItem title="4. Set up International Arrival Containers">
    If you are a Freight 2 Post customer, ensure that [International Arrival Containers (A-scan)](https://docs.intersoftsapient.net/docs/add-barcode-range-for-international-arrival-containers) is set up with valid details provided to you by INTERSOFT Onboarding team.

    ***
  </ToggleListItem>

  <br />

  <ToggleListItem title="5. Complete label sign off">
    After this, you can proceed with the **label sign off** required by Royal Mail. The sign off depends on what type of Royal Mail customer you are:

    * **Royal Mail importers using Commercial Clearance route and Tracked High Volume customers**: involves physical label sign off—where you are requested to create couple of labels, manifest them, print them out using your production printers and ship them to Royal Mail for review and quality testing.
    * **Royal Mail importers using Freight 2 Post route**: involves CDS checks as well as physical label sign off. For CDS checks, you are requested to create a couple of <Glossary>labels</Glossary>, <Glossary>manifest</Glossary> them and share with us the <Glossary>PDF</Glossary>s, so they can be reviewed and signed off before you proceed to the physical label sign off.

    The full details on this are shared with you closer to the date.

    ***
  </ToggleListItem>

  <br />

  <ToggleListItem title="6. Start shipping via Intersoft SAPIENT">
    Once the labels are signed off and the go-live action is agreed with Royal Mail, you can start shipping via Intersoft SAPIENT.

    <Callout icon="⚠️" theme="warning">
      ### *Important*

      *Once you go-live any technical issues should be raised directly with our Tech Support team by following the steps listed[here](https://docs.intersoftsapient.net/docs/troubleshooting#/).* *Enquiries regarding addition of the new services, features etc. should be continued being sent to[onboarding@intersoft.co.uk](mailto:onboarding@intersoft.co.uk).*
    </Callout>
  </ToggleListItem>
</ToggleList>

***

### See also

If you are interested in creating a Tracking Account for the newly added Shipping Account, refer to the following sections on how to set up our <Glossary>Tracking Webhook</Glossary> solution:

<Cards columns={3}>
  <Card title="Tracking Webhook" href="https://docs.intersoftsapient.net/docs/tracking-webhook-1" icon="fa-solid fa-satellite-dish">
    Set up the webhook connection, create tracking account, and much more.
  </Card>

  <Card title="Response examples" href="https://docs.intersoftsapient.net/reference/post_v4-trackings-pushpayloadexample" icon="fa-solid fa-code">
    View response example of the tracking webhook push notification payload, as sent to a customer's webhook when tracking information is received from a carrier.
  </Card>

  <Card title="Royal Mail Tracking Account setup" href="https://docs.intersoftsapient.net/docs/royal-mail-tracking-account-setup" icon="fa-solid fa-truck">
    Set up Royal Mail tracking account.
  </Card>
</Cards>

> 📘 _Note_
>
> _To enable the **Tracking Webhook** solution, please contact our [Intersoft Onboarding](mailto:onboarding@intersoft.co.uk) team._
