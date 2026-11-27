---
title: Integrate with Royal Mail Import service
excerpt: >-
  The Royal Mail Import service allows you to send goods from overseas into the
  UK for delivery by Royal Mail.
deprecated: false
hidden: false
icon: fad fa-circle-exclamation-check
metadata:
  robots: index
---
You can integrate with Intersoft SAPIENT to use the Royal Mail Import service.

<Callout icon="🚧" theme="warn">
  ### _Important_

  _This section is only for Royal Mail customers importing goods into the UK. Before you start the integration, you must have an agreement with Royal Mail to use the Royal Mail Import service._
</Callout>

Follow the steps below to integrate the Royal Mail Import service with SAPIENT:

<ToggleList>
  <ToggleListItem title="1. Activate your SAPIENT account" icon="fa-solid fa-user-check">
    Follow the instructions in your account confirmation email to activate your SAPIENT account. The email will be sent from onboarding@intersoftsapient.net.

    ***
  </ToggleListItem>

  <br />

  <ToggleListItem title="2. Create your API credentials" icon="fa-solid fa-key">

    <br />

    Follow the [API Credentials guide](https://docs.intersoftsapient.net/docs/create-api-credentials) to create your credentials.

    ***
  </ToggleListItem>

  <br />

  <ToggleListItem title="3. Select the Royal Mail Labels integration" icon="fa-solid fa-tags">

    <br />

    On the SAPIENT Home page, select **Integrations**. In the Royal Mail section, select **LABELS**.

    <Image align="center" border={true} src="https://files.readme.io/d83f58ad7239cbd1faadbb4d1783adbfceaaef163fb864672d6c2600b954e14e-Rm_lables_integration.png" caption="Selecting the Royal Mail Labels integration" />

    ***
  </ToggleListItem>

  <br />

  <ToggleListItem title="4. Activate the Labels integration" icon="fa-solid fa-toggle-on">

    <br />

    On the Integrations page, in the **LABELS** section, select **ACTIVATE**.

    <Image align="center" border={true} src="https://files.readme.io/abc4b6de2300fc06a50a56e87560afb0251fd5a13cf521fff5c473cdc4502d51-RM_Labels_activation.png" caption="Activating the Royal Mail labels integration" />

    ***
  </ToggleListItem>

  <br />

  <ToggleListItem title="5. Add your Shipping Account and Shipping Location" icon="fa-solid fa-location-dot">

    <br />

    Add your Royal Mail [Shipping Account](https://docs.intersoftsapient.net/docs/shipping-account-requirements) and [Shipping Location](https://docs.intersoftsapient.net/docs/add-a-shipping-location).

    <Callout icon="💡" theme="default">
      ### *Tip*

      *For your Sandbox (Test) account, you can use dummy details. For more instructions on how to set up a Royal Mail S<Glossary>hipping Account</Glossary>, see [Set up Royal Mail Shipping Account](https://docs.intersoftsapient.net/docs/shipping-account-requirements).*
    </Callout>

    ***
  </ToggleListItem>

  <br />

  <ToggleListItem title="6. Set up International Arrival Containers (Freight 2 Post only)" icon="fa-solid fa-barcode">

    <br />

    If you are a Freight 2 Post customer, set up [International Arrival Containers (A-Scan)](https://docs.intersoftsapient.net/docs/add-barcode-range-for-international-arrival-containers). For Sandbox testing, you can use dummy details for the Customer Number. Use the barcode range **AC40000001** to **AC49999999** for testing.

    We will provide your Production details when your account is switched to Production.

    ***
  </ToggleListItem>

  <br />

  <ToggleListItem title="7. Develop the required API calls" icon="fa-solid fa-code">

    <br />

    Develop and test the required [API calls](https://docs.intersoftsapient.net/docs/sandbox-development-api-requirements) in the Sandbox environment. For more information, refer to the [Sandbox API development](https://docs.intersoftsapient.net/docs/sandbox-development-api-requirements) section.
Additionally, you must follow the requirements for your service:

    <Columns layout="auto">
      <Column>
       * **Commercial Clearance**: Refer to the [Commercial Clearance requirements](https://docs.intersoftsapient.net/docs/commercial-clearance-customers).
      </Column>

      <Column>
       * **Freight 2 Post**: Refer to the [Freight 2 Post requirements](https://docs.intersoftsapient.net/docs/freight-2-post-customers).
      </Column>
    </Columns>
<br />

    > 🚧 *Important*
    >
    > *Ensure that you adhere to the [API Rate Limits](https://docs.intersoftsapient.net/docs/api-rate-limiting).*

    ***
  </ToggleListItem>

  <br />

  <ToggleListItem title="8. Complete and submit the Test Pack" icon="fa-solid fa-clipboard-check">

    <br />

    Complete the following [Test Pack requirements](https://docs.intersoftsapient.net/docs/royal-mail-importers-sandbox-test-pack) and submit the completed Test Pack to [onboarding@intersoft.co.uk](mailto:onboarding@intersoft.co.uk).

    > 📘 *Note*
    >
    > *Before you can move to Production, you must complete and submit the Royal Mail Import Sandbox Test Pack. The Test Pack confirms that your integration has been tested correctly.*

    ***
  </ToggleListItem>

  <br />

  <ToggleListItem title="9. Set up your Production Shipping Account" icon="fa-solid fa-rocket">

    <br />

    Once your **Test Pack** is approved, set up a separate Production Shipping Account. Keep your existing Sandbox Shipping Account for testing. See   [Set up your Production Shipping Account](https://docs.intersoftsapient.net/docs/switching-the-account-to-production) for the steps to complete your Production setup and Royal Mail sign-off.
  </ToggleListItem>
</ToggleList>

<Callout icon="💡" theme="default">
  ### _Tip_

  _If you have a question or experience an issue with the Royal Mail Import service, contact the&#x20;_<Anchor target="_blank" href="mailto:onboarding@intersoft.co.uk">_Intersoft Onboarding_</Anchor>_&#x20;team_

  _If you are reporting an API issue, include a copy of both the API request and API response. This will help us investigate the issue._

  _Do not include your API credentials when sending API requests or responses to Intersoft._
</Callout>

***

### Related guides

<Cards columns="2">
  <Card title="Returns Services" href="https://docs.intersoftsapient.net/docs/switching-the-account-to-production" icon="fa-solid fa-rotate-left" target="_blank">
    View all the requirements for using Royal Mail returns services.
  </Card>

  <Card title="Webhooks" href="https://docs.intersoftsapient.net/docs/tracking-webhook-1" icon="fad fa-webhook" target="_blank">
    Set up the webhook connection, create a tracking account, and more.

    > _To enable the&#x20;_**_Tracking Webhook_**_&#x20;solution, contact the&#x20;_[_Intersoft Onboarding_](mailto:onboarding@intersoft.co.uk)_&#x20;team._
  </Card>

  <Card title="Add Royal Mail Tracking Account" href="https://docs.intersoftsapient.net/docs/royal-mail-tracking-account-setup" icon="fa-solid fa-magnifying-glass-location" target="_blank">
    Access the step-by-step guide on how to set up Royal Mail tracking account on SAPIENT.
  </Card>

  <Card title="Response Examples" href="https://docs.intersoftsapient.net/reference/post_v4-trackings-pushpayloadexample" icon="fa-solid fa-code">
    View response examples of the tracking webhook push notification payload.
  </Card>
</Cards>