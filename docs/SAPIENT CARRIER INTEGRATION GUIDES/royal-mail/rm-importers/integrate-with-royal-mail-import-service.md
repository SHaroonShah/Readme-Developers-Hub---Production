---
title: Integrate with Royal Mail Import service
excerpt: >-
  The Royal Mail import service is a logistic solution provided by Royal Mail
  that facilitates the importation of goods into the UK from overseas. It is
  designed to simplify the process of receiving international parcels and
  packages, ensuring that they are delivered efficiently and securely to the
  customers.
deprecated: false
hidden: false
icon: fad fa-circle-exclamation-check
metadata:
  robots: index
---
If you wish to use the Royal Mail import services, you can integrate with Intersoft SAPIENT and start your seamless importing journey.

<Callout icon="🚧" theme="warn">
  ### _Important_

  _This section is only applicable if you are a Royal Mail customer who is importing goods into the UK. Before initiating the integration, make sure you have an agreement with Royal Mail to use this service._
</Callout>

To integrate with the Royal Mail import services via SAPIENT, follow the steps listed below:

<ToggleList>
  <ToggleListItem title="1. Activate your SAPIENT account" icon="fa-solid fa-user-check">
    Activate your account on SAPIENT as directed in the account confirmation email sent to you from [onboarding@intersoftsapient.net](mailto:noreply@intelligentshipper.net).

    ***
  </ToggleListItem>

  <br />

  <ToggleListItem title="2. Create your API credentials" icon="fa-solid fa-key">
  <br />

    Proceed to [creating your API Credentials](https://docs.intersoftsapient.net/docs/create-api-credentials).

    ***
  </ToggleListItem>

  <br />

  <ToggleListItem title="3. Select the Royal Mail Labels integration" icon="fa-solid fa-tags">
    On the SAPIENT Home page, select **Integrations**. On the **Integrations** page that opens, within the **Royal Mail** block, select **LABELS**.

    <Image align="center" border={true} src="https://files.readme.io/d83f58ad7239cbd1faadbb4d1783adbfceaaef163fb864672d6c2600b954e14e-Rm_lables_integration.png" alt="Selecting Royal Mail labels integration" />

    ***
  </ToggleListItem>

  <br />

  <ToggleListItem title="4. Activate the Labels integration" icon="fa-solid fa-toggle-on">
    On the integrations page that opens, in the **LABELS** block, select **ACTIVATE**.

    <Image align="center" border={true} src="https://files.readme.io/abc4b6de2300fc06a50a56e87560afb0251fd5a13cf521fff5c473cdc4502d51-RM_Labels_activation.png" alt="Activating Royal Mail labels integration" />

    ***
  </ToggleListItem>

  <br />

  <ToggleListItem title="5. Add Shipping Account and Shipping Location" icon="fa-solid fa-location-dot">
    Add the [Shipping Account](https://docs.intersoftsapient.net/docs/shipping-account-requirements) and [Shipping Location](https://docs.intersoftsapient.net/docs/add-a-shipping-location) for Royal Mail.

    <Callout icon="💡" theme="default">
      ### *Tip*

      *For Sandbox (Test) account, fill the information with dummy details. For more information on how to set up a Royal Mail S<Glossary>hipping Account</Glossary>, refer to the [Set up Royal Mail Shipping Account](https://docs.intersoftsapient.net/docs/shipping-account-requirements) section.*
    </Callout>

    ***
  </ToggleListItem>

  <br />

  <ToggleListItem title="6. Set up International Arrival Containers (Freight 2 Post only)" icon="fa-solid fa-barcode">
    If you are a Freight 2 Post customer, set up [International Arrival Containers (A-scan)](https://docs.intersoftsapient.net/docs/add-barcode-range-for-international-arrival-containers). For now the Customer Number can be filled with dummy details. The Barcode Range used for testing purposes should be **AC40000001** to **AC49999999**.

    Production details will be provided to you when your account is switched onto production.

    ***
  </ToggleListItem>

  <br />

  <ToggleListItem title="7. Develop the required API calls" icon="fa-solid fa-code">
    Develop all the [API calls required](https://docs.intersoftsapient.net/docs/sandbox-development-api-requirements) considering the specific requirements applicable to you:

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
    > *Ensure that you adhere to the[API Rate Limits](https://docs.intersoftsapient.net/docs/api-rate-limiting).*

    ***
  </ToggleListItem>

  <br />

  <ToggleListItem title="8. Complete and submit the Test Pack" icon="fa-solid fa-clipboard-check">
    Complete the [Test Pack](https://docs.intersoftsapient.net/docs/royal-mail-importers-sandbox-test-pack) and submit it at [onboarding@intersoft.co.uk](mailto:onboarding@intersoft.co.uk).

    > 📘 *Note*
    >
    > *A test pack is a critical step in the implementation process, ensuring a smooth transition to the live environment and minimising disruptions in shipping operations.*

    ***
  </ToggleListItem>

  <br />

  <ToggleListItem title="9. Switch to Production" icon="fa-solid fa-rocket">
    Once the **Test Pack** is approved, our team will [switch your account to Production](https://docs.intersoftsapient.net/docs/switching-the-account-to-production) and share with you the details on the sign off process required by Royal Mail.
  </ToggleListItem>
</ToggleList>

## Need Help?

<Callout icon="💡" theme="default">
  ###

  _Please direct any questions or issues with this service to [onboarding@intersoft.co.uk](mailto:onboarding@intersoft.co.uk). For INTERSOFT to investigate your issue accordingly, kindly include copies of both the API request and API response._

  _While submitting your issues to Intersoft, please do not include your API credentials in the request._
</Callout>

***

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
  ### _Note_

  _To enable the&#x20;_**_Tracking Webhook_**_&#x20;solution, contact the [Intersoft Onboarding](mailto:onboarding@intersoft.co.uk) team._
</Callout>

<br />
