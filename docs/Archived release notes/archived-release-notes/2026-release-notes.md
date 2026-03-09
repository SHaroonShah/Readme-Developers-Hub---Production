---
title: 2026 release notes
excerpt: This section includes the archived release notes published in the year 2026.
deprecated: false
hidden: false
icon: fad fa-notes
metadata:
  robots: index
---
<Accordion title="SAPIENT release notes - January 20, 2026" icon="">
  ## DPD UK integration

  The DPD UK integration has been added to the SAPIENT system. This integration expands our shipping options, allowing our customers to utilise DPD UK for their shipping needs, improving overall service flexibility and efficiency.

  With this addition, the following information has been added to the swagger documentation:

  * **New API endpoints**. A new DPD UK block has been added to our carrier-specific APIs. This block includes the following API endpoints:
    * **Shipping Account**
      * **Get Accounts**: Retrieve a list of DPD UK shipping accounts.
      * **Add Account**: Add a new DPD UK shipping account.
      * **Get Account**: Retrieve details of a specific DPD UK shipping account.
      * **Update Account**: Update details of an existing DPD UK shipping account.
      * **Link Locations**: Link shipping locations to the DPD UK shipping accounts.
      * **Get Associated Locations**: Retrieve locations linked to the DPD UK shipping account.
      * **Get Associated Location**: Fetch details for a specific associated location.
    * **Shipments**
      * **Create Shipment**: Create a new DPD UK shipment request.
      * **Print Label**: Generate a label for the DPD UK shipment. This is only valid if the shipment is created with the action other than **Process**.

  > 📘 *Note*
  >
  > *The [Get Carrier](https://docs.intersoftsapient.net/reference/get_v4-carriers-carriercode) and [Get Carrier Services](https://docs.intersoftsapient.net/reference/get_v4-carriers-carriercode-services) endpoints in our **SAPIENT CORE API** block can also be utilised to look for the carrier and its available services.*

  ## InPost tracking webhook

  The InPost Tracking Webhook is now available via the Webhook integration on SAPIENT to enable real-time updates on parcel status changes. By leveraging InPost's webhook capabilities, our system will be able to automatically receive and process tracking events, reducing the need for manual polling and improving overall responsiveness of our delivery tracking features.

  ## Royal Mail shipment validation to Channel Islands

  The following updates have been made to the Royal Mail shipment validation to Channel Islands:

  * **Isle of Man shipment validation**. Royal Mail shipments from Great Britain to Isle of Man are classified as domestic, which means:

    * CN22/CN23 customs forms are not required
    * Mandatory customs details or email information are no longer needed
    * A 1D barcode is not required
    * Standard pre-advice rules apply
  * **Guernsey shipment validation**. Royal Mail shipments from Great Britain to Guernsey are now treated as international dutiable. When the destination postcode begins with GY and the country code is GB or GG, a CN23 customs declaration form will be automatically generated. To ensure compliance, customers will also be required to provide detailed item information, including the HS code and country of origin.

  ## 1D Barcode for Royal Mail Domestic Services to Guernsey

  Royal Mail shipments from GB to Guernsey using the following unsigned services will now include a 1D barcode on the labels:

  | Service Name | Service Codes             |
  | :----------- | :------------------------ |
  | RM24         | CRL1, PK1, PK3, FS1, PPF1 |
  | RM48         | CRL2, PK2, PK4, FS2, PPF2 |
  | 1st Class    | STL1                      |
  | 2nd Class    | STL2                      |

  <br />

  <Image align="center" src="https://files.readme.io/c39220c3e365dc6b73e85fb2222362ee9de492acadc1a2ab2085091ca4c0ac38-image.png" width="300px" />

  ## Royal Mail OBA registered billing address validation

  The SAPIENT platform now allows Royal Mail customers to enter any Registered Billing Postcode, including international formats, when creating, editing, or linking their Royal Mail Shipping Account. This update removes previous UK-only postcode validation in both the UI and API, ensuring that postcodes match exactly as recorded in the Royal Mail Online Business Account (OBA).

  ## Royal Mail Parcelforce international label templates

  The following Royal Mail Parcelforce international label templates have been updated to include the **Recipient telephone number** to conform with the overseas delivery partners and customs authorities:

  * **ChinaEconomy**
  * **GlobalPriorityEurope**
  * **EuroPriority**
  * **GlobalPriorityRow**
  * **GlobalExpress**
  * **IrelandExpress**

    <Image align="center" src="https://files.readme.io/4b190c2e721cece0621207dd17723861fa718a062c7ab1ff497407ee92ca9d94-image.png" width="300px" />

    ## Royal Mail firearms label templates

  The Royal Mail firearms **ExpressAM** and **ExpressAMFWeekend** label templates have been updated to align with Royal Mail’s latest standards. This helps prevent misrouting and ensure your deliveries remain secure and compliant.

  <Image align="center" src="https://files.readme.io/6ebb0b45816d49a909969f31991baf335508196ac578c379719ff169607c83df-image.png" width="300px" />

  ## SAPIENT cookie policy

  A new cookie consent functionality has been added to the SAPIENT user interface to ensure compliance with the UK Cookie Policy and the General Data Protection Regulation (GDPR). With this addition, a cookie banner is displayed upon the user's initial login, allowing them to accept or reject functional cookies that enhance their experience.

  <Image align="center" border={true} src="https://files.readme.io/ed33bcaebe7e851763bd98d0ed33d0d703ab2579b89b4e4e424fed59c5e8b150-image.png" />

  > 📘 *Note*
  >
  > *Users can manage their consent, with preferences retained for a duration of 13 months. The banner will reappear only if the preferences expire or if new cookies are introduced. Furthermore, all consent records will be preserved for a minimum of 13 months to ensure compliance, foster user trust, and enhance transparency and user control while adhering to legal obligations.*

  ## Website rate limiting enhancements

  The system’s rate limiting has been updated to align customer (TPS) settings with our tier structure. This change ensures fair resource allocation, improved performance consistency, and better scalability across all tiers.

  ## Technology upgrades

  Our technology architecture has been upgraded to **.NET 8**. This upgrade enhances performance, security, and developer productivity across our applications and services.

  > 📘 *Note*
  >
  > *Following the .NET upgrades, you may encounter the following error on your first login attempt:*
  >
  >   <Image align="center" src="https://files.readme.io/241c63cacd72870f298ea6e57e47df62c95f2972e79eae45082f365b23260a2c-image.png" width="500px" />
  >
  > *To resolve this issue, simply log out of the system and sign in again.*

  ## Swagger documentation updates

  The following updates have been made to our swagger documentation:

  * **Royal Mail Print Label response example**. The Royal Mail Datastream response example in the Print Label API endpoint has been updated to include new fields required for the new Royal Mail Parcelforce services.
  * **Shipping Locations endpoint**. The query and response field descriptions for our following CORE API endpoints have been updated to improve clarity and support correct usage of the API:

    * **Get Locations**
    * **Add Location**
    * **Get Location**
    * **Update Location**
    * **Delete Location**

  ## A fresh new look for our Developers Hub documentation

  We are excited to announce the first phase of our Developers Hub documentation redesign, bringing you a cleaner, more interactive experience to make finding information easier and faster.

  ## What's new?

  Our updated documentation now includes:

  * **Cards** – For quick access to key information at a glance. Most cards include embedded cross-reference links, allowing you to jump directly to related topics without extra navigation.

  <Image align="center" border={true} src="https://files.readme.io/5ea46a6bfce430ac396a7afccf0736ac5bbd88b569ed5ce8dcb6f3e46e0c781d-Cards.png" width="500px" />

  * **Tabs** – Easily switch between related topics without leaving the page

  <Image align="center" border={true} src="https://files.readme.io/cebfd6eae0756944c26c91111a46007f6ad83c3dddcc937367d23cad9fb7c8d8-Tabs.png" width="500px" />

  * **Accordions** – Expand and collapse sections for a clutter-free view

  <Image align="center" border={true} src="https://files.readme.io/9c447c90cb965053a020608bfda087a187ebd9b6d7a5b5b66840f80f260e05ab-Accordions.png" width="500px" />

  * **Toggle List** – Step-by-step instructions that you can reveal as needed

  <Image align="center" border={true} src="https://files.readme.io/297a1a252f240422ed11e345478ed9e632e2baaba70ebd7756779de177166558-Toggle_list.png" width="500px" />

  * **Banners** – Highlight important features

  <Image align="center" border={true} src="https://files.readme.io/b361863e5940780fdf8cd7bf0378f4da3ee1656dbd9e7ac238b5fb8d24ed06f9-Banner.png" width="500px" />

  * **Columns** – Better content organisation for improved readability

  <Image align="center" border={true} src="https://files.readme.io/aa7a74ba62a5b98bdac2dbbdba5576e61acf4961b6ab273426408453e4c2e8a5-Columns.png" width="500px" />

  * **Stepper** – A guided, sequential navigation component that walks you through multi-step processes in a clear, structured way. Perfect for complex workflows or setup instructions.

  <Image align="center" border={true} src="https://files.readme.io/27a93fff2ad64a171e2321e5dea00a0e8d28855c142d9cc31a49760a5f5841cb-Stepper.png" width="500px" />

  * **Theme** – The theme of our Developers Hub has been switched to **Dark Mode** to comply with our SAPIENT system standards.

  > 📘 *Note*
  >
  > *This is just the first phase of our redesign. The second phase is currently under development, which will introduce even more improvements, features, and upgrades to our documentation.*

  <br />
</Accordion>

<br />
