---
title: Configure Hurricane commerce service
excerpt: >-
  _Hurricane_ is a UK-based technology company that specialises in cross-border
  e-commerce solutions. With the rise of online shopping, cross-border
  e-commerce has become a crucial part of the retail industry.
deprecated: false
hidden: false
icon: fad fa-scanner-touchscreen
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
There are some significant challenges faced by the retailers, including the accurate calculation of duties, taxes, and fees associated with shipping goods internationally.This is where Hurricane commerce cervices comes in. The company has developed a suite of tools that help retailers and postal operators comply with international regulations and requirements related to cross-border e-commerce.

In SAPIENT, you can configure the Hurricane commerce services, to eliminate your cross-border challenges and streamline your international <Glossary>shipment</Glossary> process.

## How to configure Hurricane commerce service

To configure the Hurricane commerce service, follow the instructions as provided in the following procedure.

<ToggleList>
  <ToggleListItem title={<strong>1. Access integrations page</strong>} icon="fa-rocket">
    <br />

    From the **Home** page, in the left navigation panel, select **Integrations**.

<Image align="center" alt="Accessing integrations" border={true} caption="Accessing integrations" src="https://files.readme.io/9edbbe0f060a9821348b7a077aae6171ab9fde12fd7b6d2ffdbe5d215b463f3a-Sapient_home_page.png" />

> 🚧 _Important_
>
> _Before you configure the Hurricane service, please note that this is a chargeable service, you will be invoiced directly and any associated usage fees will be applied going forwards. Only approved personnel from your company should be given permission to access these pages and activate this service._

    ***
  </ToggleListItem>

  <br />

  <ToggleListItem title={<strong>2. Accessing customs option</strong>} icon="fa-rocket">
    <br />

    On the **Integrations** page that opens, in the **Hurricane** block, select **CUSTOMS** .

<Image align="center" alt="Accessing hurricane service" border={true} caption="Accessing hurricane service" src="https://files.readme.io/6ab95a5c1c86ae354fef99d35a7bc44c455705c6ff7e56217a30a01f58b9a29a-Accessing_hurricane_customs_service.png" />

    ***
  </ToggleListItem>

  <br />

  <ToggleListItem title={<strong>3. Accessing option to configure Hurricane services </strong>} icon="fa-rocket">
    <br />

    On the page that opens, view the services and features provided by Hurricane in their respective blocks, and if you wish to proceed, select **CONFIGURE**.

<Image alt="Selecting option to configure hurricane service" align="center" border={true} src="https://files.readme.io/9617de8bf0d49838392c05d0184155859865df5391536e1b03685863fe928ef9-Selection_option_to_configure_HS.png" alt="
  Selecting option to configure hurricane service" />

    ***
  </ToggleListItem>

  <br />

  <ToggleListItem title={<strong>4. Configure Hurricane services  </strong>} icon="fa-rocket">
    <br />

    On the **Configure Hurricane** page that opens, next to each available service, turn on the toggle for the service that you wish to configure. 

<Image alt="Selecting hurricane services" align="center" border={true} src="https://files.readme.io/3aaa4e5db150ef6800d6595f71b05fa7c207d4ac67d041c4180af7a4bb3b1e6e-Selecting_hurricane_service.png" alt=">
  Selecting Hurricane services" />
  </ToggleListItem>
<br />
<ToggleListItem title={<strong>5. Enable Hurricane services </strong>} icon="fa-rocket">
    <br />
If you wish to select the **Enable Prohibited Items check on shipment creation** or **Enable Denied Parties check on shipment creation** options, then a **DENIED PARTIES AND PROHIBITED ITEMS COUNTRIES[CONTER]** table is displayed with the following columns.

<Image alt="Configuring hurricane services" align="center" border={true} src="https://files.readme.io/034f4680d679a260821c6edc87a787cbb97887a401cb96e3ceb7904a811b6b1d-Configuring_hurricane_services.png" alt=">
  Configuring Hurricane services" />

<Table align={["center","left"]}>
  <thead>
    <tr>
      <th style={{ textAlign: "center" }}>
        Column
      </th>

      <th style={{ textAlign: "left" }}>
        Description
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td style={{ textAlign: "center" }}>
        **Country Name**
      </td>

      <td style={{ textAlign: "left" }}>
        Represents the name of the country for which the service is being configured.
      </td>
    </tr>

    <tr>
      <td style={{ textAlign: "center" }}>
        **Alpha-2 Code**
      </td>

      <td style={{ textAlign: "left" }}>
        Represents the country code (initials) of the country for which the service is being configured.
      </td>
    </tr>

    <tr>
      <td style={{ textAlign: "center" }}>
        **Require Check for Denied Parties**
      </td>

      <td style={{ textAlign: "left" }}>
        Represents whether the service needs to check for <Glossary>denied parties</Glossary> for this country. Typical values are **Yes** and **No**.
      </td>
    </tr>

    <tr>
      <td style={{ textAlign: "center" }}>
        **Denied Party Score**
      </td>

      <td style={{ textAlign: "left" }}>
        Represents the threshold value above which the country is identified as denied.  

        *Note: this value is set to 75 by default. You cannot change this value.*
      </td>
    </tr>

    <tr>
      <td style={{ textAlign: "center" }}>
        **Require Check for Prohibited Items**
      </td>

      <td style={{ textAlign: "left" }}>
        Represents whether the service needs to check for prohibited items. Typical values are **Yes** and **No**.
      </td>
    </tr>

    <tr>
      <td style={{ textAlign: "center" }}>
        **Last Modified**
      </td>

      <td style={{ textAlign: "left" }}>
        Represents the exact date, time, and the name of the user who last modified the information provided in the table.
      </td>
    </tr>

    <tr>
      <td style={{ textAlign: "center" }}>
        Actions
      </td>

      <td style={{ textAlign: "left" }}>
        Select **View** to open a new screen, where you can manage the Hurricane services for that country. Additionally, from that page, you can also delete the country, if applicable.
      </td>
    </tr>
  </tbody>
</Table>

> 💡 *Tip*
>
> *You can also add a new country to the list by selecting the**Add Country** button and configure the desired hurricane services for it on the fly*.

    ***
  </ToggleListItem>
</ToggleList>

1. Log in to the SAPIENT platform using your credentials.

<Image align="center" alt="Logging into SAPIENT" border={true} caption="Logging into SAPIENT" src="https://files.readme.io/9d01c43822f6ea8e09f2dcc827a191c1d319511fdbf63e40e4a779b72ec3c46d-Sapient_Login_window.png" width="500px" />

2. On the **Home** page that opens, in the left navigation panel, select **Integrations**.

<Image align="center" alt="Accessing integrations" border={true} caption="Accessing integrations" src="https://files.readme.io/9edbbe0f060a9821348b7a077aae6171ab9fde12fd7b6d2ffdbe5d215b463f3a-Sapient_home_page.png" />

> 🚧 _Important_
>
> _Before you configure the Hurricane service, please note that this is a chargeable service, you will be invoiced directly and any associated usage fees will be applied going forwards. Only approved personnel from your company should be given permission to access these pages and activate this service._

3. On the **Integrations** page that opens, in the **Hurricane** block, select **CUSTOMS** .

<Image align="center" alt="Accessing hurricane service" border={true} caption="Accessing hurricane service" src="https://files.readme.io/6ab95a5c1c86ae354fef99d35a7bc44c455705c6ff7e56217a30a01f58b9a29a-Accessing_hurricane_customs_service.png" />

4. On the page that opens, view the services and features provided by Hurricane in their respective blocks, and if you wish to proceed, select **CONFIGURE**.

<Image align="center" alt="Selecting option to configure hurricane service" border={true} caption="Selecting option to configure hurricane service" src="https://files.readme.io/9617de8bf0d49838392c05d0184155859865df5391536e1b03685863fe928ef9-Selection_option_to_configure_HS.png" />

5. On the **Configure Hurricane** page that opens, next to each available service, turn on the toggle for the service that you wish to configure.

<Image align="center" alt="Selecting hurricane services" border={true} caption="Selecting Hurricane services" src="https://files.readme.io/3aaa4e5db150ef6800d6595f71b05fa7c207d4ac67d041c4180af7a4bb3b1e6e-Selecting_hurricane_service.png" />

6. If you wish to select the **Enable Prohibited Items check on shipment creation** or **Enable Denied Parties check on shipment creation** options, then a **DENIED PARTIES AND PROHIBITED ITEMS COUNTRIES[CONTER]** table is displayed with the following columns.

<Image align="center" alt="Configuring hurricane services" border={true} caption="Configuring Hurricane services" src="https://files.readme.io/034f4680d679a260821c6edc87a787cbb97887a401cb96e3ceb7904a811b6b1d-Configuring_hurricane_services.png" />

<Table align={["center","left"]}>
  <thead>
    <tr>
      <th>
        Column
      </th>

      <th>
        Description
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        **Country Name**
      </td>

      <td>
        Represents the name of the country for which the service is being configured.
      </td>
    </tr>

    <tr>
      <td>
        **Alpha-2 Code**
      </td>

      <td>
        Represents the country code (initials) of the country for which the service is being configured.
      </td>
    </tr>

    <tr>
      <td>
        **Require Check for Denied Parties**
      </td>

      <td>
        Represents whether the service needs to check for <Glossary>denied parties</Glossary> for this country. Typical values are **Yes** and **No**.
      </td>
    </tr>

    <tr>
      <td>
        **Denied Party Score**
      </td>

      <td>
        Represents the threshold value above which the country is identified as denied.

        _Note: this value is set to 75 by default. You cannot change this value._
      </td>
    </tr>

    <tr>
      <td>
        **Require Check for Prohibited Items**
      </td>

      <td>
        Represents whether the service needs to check for prohibited items. Typical values are **Yes** and **No**.
      </td>
    </tr>

    <tr>
      <td>
        **Last Modified**
      </td>

      <td>
        Represents the exact date, time, and the name of the user who last modified the information provided in the table.
      </td>
    </tr>

    <tr>
      <td>
        Actions
      </td>

      <td>
        Select **View** to open a new screen, where you can manage the Hurricane services for that country. Additionally, from that page, you can also delete the country, if applicable.
      </td>
    </tr>
  </tbody>
</Table>

<Callout icon="💡" theme="default">
  ### _Tip_

  _You can also add a new country to the list by selecting the**Add Country** button and configure the desired hurricane services for it on the fly_.
</Callout>
