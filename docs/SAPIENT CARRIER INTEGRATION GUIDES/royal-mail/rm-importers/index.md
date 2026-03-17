---
title: Royal Mail import service
excerpt: >-
  The Royal Mail import service is a logistic solution provided by Royal Mail
  that facilitates the importation of goods into the UK from overseas. It is
  designed to simplify the process of receiving international parcels and
  packages, ensuring that they are delivered efficiently and securely to the
  customers.
deprecated: false
hidden: false
icon: fad fa-file-import
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
If you wish to use the Royal Mail import services, you can integrate with Intersoft SAPIENT and start your seamless importing journey.

> 🚧 *Important*
>
> *This section is only applicable if you are a Royal Mail customer who is importing goods into the UK. Before initiating the integration, make sure you have an agreement with Royal Mail to use this service.*

To integrate with the Royal Mail import services via SAPIENT, follow the steps listed below:

1. At first, ensure to activate your account on SAPIENT as directed in an account confirmation email  sent to you from [onboarding@intersoftsapient.net](mailto:noreply@intelligentshipper.net).

2. After, proceed to [creating your API Credentials](https://docs.intersoftsapient.net/docs/create-api-credentials).

3. Now, on the SAPIENT Home page, select **Integrations**. On the **Integrations** page that opens, within the **Royal Mail** block, select **LABELS**.

<Image align="center" alt="Selecting Royal Mail labels integration" border={true} caption="Selecting Royal Mail labels integration" src="https://files.readme.io/d83f58ad7239cbd1faadbb4d1783adbfceaaef163fb864672d6c2600b954e14e-Rm_lables_integration.png" />

4. On the integrations page that opens, in the **LABELS** block, select **ACTIVATE**.

<Image align="center" alt="Activating Royal Mail labels integration" border={true} caption="Activating Royal Mail labels integration" src="https://files.readme.io/abc4b6de2300fc06a50a56e87560afb0251fd5a13cf521fff5c473cdc4502d51-RM_Labels_activation.png" />

5. Once activated, now proceed to adding the  [Shipping Account](https://docs.intersoftsapient.net/docs/shipping-account-requirements) and [Shipping Location](https://docs.intersoftsapient.net/docs/add-a-shipping-location) for Royal Mail.

> 💡 *Tip*
>
> *For Sandbox (Test) account, please fill the information with dummy details. For more information on how to set up a Royal Mail S<Glossary>hipping Account</Glossary> , refer to the [Set up Royal Mail Shipping Account](https://docs.intersoftsapient.net/docs/shipping-account-requirements) section.*

6. If you are a Freight 2 Post customer, set up [International Arrival Containers (A-scan)](https://docs.intersoftsapient.net/docs/add-barcode-range-for-international-arrival-containers). For now the Customer Number can be filled with dummy details. The Barcode Range used for testing purposes should be AC40000001 to AC49999999.\
   Production details will be provided to you when your account is switched onto production.
7. After, develop all the [API calls required](https://docs.intersoftsapient.net/docs/sandbox-development-api-requirements) considering the specific requirements applicable to you:

<Columns layout="auto">
  <Column>
    **Commercial Clearance customers**

    Refer to the [Commercial Clearance requirements](https://docs.intersoftsapient.net/docs/commercial-clearance-customers).
  </Column>

  <Column>
    **Freight 2 Post customers**

    Refer to the [Freight 2 Post requirements](https://docs.intersoftsapient.net/docs/freight-2-post-customers).
  </Column>
</Columns>

> 🚧 *Important*
>
> *Please also ensure that you adhere to our[API Rate Limits](https://docs.intersoftsapient.net/docs/api-rate-limiting).*

8. Once all the above steps have been done, make sure you complete our [Test Pack](https://docs.intersoftsapient.net/docs/royal-mail-importers-sandbox-test-pack) and submit it at [onboarding@intersoft.co.uk](mailto:onboarding@intersoft.co.uk).

> 📘 *Note*
>
> *A test pack is a critical step in the implementation process, ensuring a smooth transition to the live environment and minimising disruptions in shipping operations.*

9. Once the **Test Pack** is approved, our team will [switch your account to Production](https://docs.intersoftsapient.net/docs/switching-the-account-to-production) and share with you the details on the sign off process required by Royal Mail.

<Callout icon="📧" theme="info">
  **Need help?** Direct any questions or issues to [onboarding@intersoft.co.uk](mailto:onboarding@intersoft.co.uk).

  When submitting an issue, include copies of both the API request and API response so INTERSOFT can investigate accordingly.

  ⚠️ **Do not** include your API credentials in the request.
</Callout>
## See also

<Cards columns={2}>
  <Card title="Returns services" href="https://docs.intersoftsapient.net/docs/switching-the-account-to-production" icon="fa-solid fa-rotate-left">
    View all the requirements for using Royal Mail returns services.
  </Card>

  <Card title="Tracking Webhook" href="https://docs.intersoftsapient.net/docs/tracking-webhook-1" icon="fa-solid fa-bell">
    Set up the webhook connection, create a tracking account, and more.
  </Card>

  <Card title="Royal Mail tracking account setup" href="https://docs.intersoftsapient.net/docs/royal-mail-tracking-account-setup" icon="fa-solid fa-magnifying-glass-location">
    Set up a Royal Mail tracking account.
  </Card>

  <Card title="Response examples" href="https://docs.intersoftsapient.net/reference/post_v4-trackings-pushpayloadexample" icon="fa-solid fa-code">
    View response examples of the tracking webhook push notification payload.
  </Card>
</Cards>

<Callout icon="📘" theme="info">
  To enable the **Tracking Webhook** solution, contact the [Intersoft Onboarding](mailto:onboarding@intersoft.co.uk) team.
</Callout>
