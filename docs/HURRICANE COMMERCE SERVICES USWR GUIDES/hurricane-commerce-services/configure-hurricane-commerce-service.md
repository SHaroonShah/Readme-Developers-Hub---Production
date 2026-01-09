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

    <Image align="center" border={true} src="https://files.readme.io/9edbbe0f060a9821348b7a077aae6171ab9fde12fd7b6d2ffdbe5d215b463f3a-Sapient_home_page.png" alt="Accessing integrations" />

    > 🚧 *Important*
    >
    > *Before you configure the Hurricane service, please note that this is a chargeable service, you will be invoiced directly and any associated usage fees will be applied going forwards. Only approved personnel from your company should be given permission to access these pages and activate this service.*

    ***
  </ToggleListItem>

  <br />

  <ToggleListItem title={<strong>2. Accessing customs option</strong>} icon="fa-rocket">
    <br />

    On the **Integrations** page that opens, in the **Hurricane** block, select **CUSTOMS** .

    <Image align="center" border={true} src="https://files.readme.io/6ab95a5c1c86ae354fef99d35a7bc44c455705c6ff7e56217a30a01f58b9a29a-Accessing_hurricane_customs_service.png" alt="Accessing hurricane service" />

    ***
  </ToggleListItem>

  <br />

  <ToggleListItem title={<strong>3. Accessing option to configure Hurricane services </strong>} icon="fa-rocket">
    <br />

    On the page that opens, view the services and features provided by Hurricane in their respective blocks, and if you wish to proceed, select **CONFIGURE**.

    <Image align="center" border={true} src="https://files.readme.io/9617de8bf0d49838392c05d0184155859865df5391536e1b03685863fe928ef9-Selection_option_to_configure_HS.png" alt="Selecting option to configure hurricane service" />

    ***
  </ToggleListItem>

  <br />

  <ToggleListItem title={<strong>4. Configure Hurricane services  </strong>} icon="fa-rocket">
    <br />

    On the **Configure Hurricane** page that opens, next to each available service, turn on the toggle for the service that you wish to configure.

    <Image
      align="center"
      border={true}
      src="https://files.readme.io/3aaa4e5db150ef6800d6595f71b05fa7c207d4ac67d041c4180af7a4bb3b1e6e-Selecting_hurricane_service.png"
      alt=">
Selecting Hurricane services"
    />
  </ToggleListItem>

  <br />

  <ToggleListItem title={<strong>5. Enable Hurricane services </strong>} icon="fa-rocket">
    <br />

    If you wish to select the **Enable Prohibited Items check on shipment creation** or **Enable Denied Parties check on shipment creation** options, then a **DENIED PARTIES AND PROHIBITED ITEMS COUNTRIES \[COUNTER]** table is displayed with the following columns.

    <Image
      align="center"
      border={true}
      src="https://files.readme.io/034f4680d679a260821c6edc87a787cbb97887a401cb96e3ceb7904a811b6b1d-Configuring_hurricane_services.png"
      alt=">
Configuring Hurricane services"
    />

    <br />

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

            *Note: this value is set to 75 by default. You cannot change this value.*
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

    <br />

    <Callout icon="💡" theme="default">
      ### *Tip*

      *You can also add a new country to the list by selecting the**Add Country** button and configure the desired hurricane services for it on the fly*.
    </Callout>

    ***
  </ToggleListItem>
</ToggleList>

***

### See also

<Cards columns={3}>
  <Card title="Commodity Code Validations" href="https://docs.intersoftsapient.net/docs/harmonized-system-codes-hs-codes" icon="fa-solid fa-barcode">
    Learn more about how Hurricane services validate commodity codes.
  </Card>

  <Card title="Quoted Landed Cost" href="https://docs.intersoftsapient.net/docs/brexituknorthernirelandandeurope" icon="fa-solid fa-money-bill-wave">
    Understand the quoted landed cost in cross-border e-commerce.
  </Card>

  <Card title="Prohibited and Restricted Items" href="https://docs.intersoftsapient.net/docs/prohibited-and-restricted-items" icon="fa-solid fa-ban">
    Check the list of prohibited and restricted items.
  </Card>

  <Card title="Export Codes Details" href="https://docs.intersoftsapient.net/docs/prohibited-and-restricted-codes-and-explanation" icon="fa-solid fa-file-export">
    Explore export codes for prohibited and restricted items.
  </Card>

  <Card title="Import Code Details" href="https://docs.intersoftsapient.net/docs/prohibited-and-restricted-codes-and-explanation-1" icon="fa-solid fa-file-import">
    Discover import codes for prohibited and restricted items.
  </Card>
</Cards>