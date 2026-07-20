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
  > *The[Get Carrier](https://docs.intersoftsapient.net/reference/get_v4-carriers-carriercode) and [Get Carrier Services](https://docs.intersoftsapient.net/reference/get_v4-carriers-carriercode-services) endpoints in our **SAPIENT CORE API** block can also be utilised to look for the carrier and its available services.*

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

<Accordion title="SAPIENT release notes - February 24, 2026" icon="">
  ## Royal Mail Windsor Framework updates

  The following changes have been made for Royal Mail shipments sent from Great Britain to Northern Ireland (addresses with a GB country code and postcode beginning BT):

  1. The shipment declaredValue must equal the sum of the item values within the shipment. The declaredValue cannot be less than or greater than the sum of the item values.
  2. For B2B shipments where a pre-registration number with pre-registration type UKIMS is provided, previous logic that treated Item HS Code as optional has now been removed. Royal Mail’s standard reference data will now be used to determine whether Item HS Code is mandatory or optional. B2B shipments are validated against Ruleset K, which is documented in the <Anchor label="Royal Mail Validation Rules" target="_blank" href="https://docs.intersoftsapient.net/docs/royal-mail-validation-rules">Royal Mail Validation Rules</Anchor> guide.

  ## Royal Mail Express 10 Service - Local Collect label templates added

  Local Collect label templates have been added for the Express 10 service, so that labels for this service can now be generated containing the Local Collect text label.

  The following variations of the Express 10 label have been added:
  •	Express 10 service with Local Collect
  •	Express 10 service with Local Collect and ‘Do Not Fly’ statement (for LQDG)
  •	Express 10 service with Local Collect and signature
  •	Express 10 service with Local Collect, signature and ‘Do Not Fly’ statement

  See an example label below:

  <Image align="center" src="https://files.readme.io/276e195454950b2caaa49aab4621fdc819e177a9ce0244cc1ddee32f948813df-Label.png" width="45% " />

  ## Royal Mail Collections API updates

  The following updates have been made to the Royal Mail Book Collection API:

  * New field added CollectionSafePlace – allows a designated safe place to be provided for the collection address that Royal Mail can securely collect the parcel from.
  * New field added OptOutFromRmNotifications – provides the option to choose whether or not collection notifications are sent to the consignee by Royal Mail.

  > 📘 *Note*
  >
  > *For more details on these changes, refer to the Royal Mail he<Anchor label="Book Collections API" target="_blank" href="https://docs.intersoftsapient.net/reference/post_v4-collections-rm-shipmentid">Book Collections API</Anchor> endpoint*

  ## Hazardous Item updates

  The validation rules applied to hazardous items have been updated. The fields UNCode, Quantity and UnitofMeasure have changed from mandatory to conditional. These fields do not need to be provided for hazardous items, but if any of these fields is provided then all three must be. This change applies to the Royal Mail Create Shipment Request, Add Product and Update Product API requests, Get Product and Get Products API responses, and the Products UI.

  > 📘 *Note*
  >
  > *For more details on the API updates, refer to the the<Anchor label="API References" target="_blank" href="https://docs.intersoftsapient.net/reference/">API References</Anchor> page.*

  ## New integration - Amazon

  The Amazon integration has been added to the SAPIENT system. This integration supports shipping via Amazon domestically within the UK for both orders created via Amazon and outside of Amazon.

  With this addition, the following information has been added to the swagger documentation:

  **New API endpoints**. A new **AMAZON** block has been added to our carrier-specific APIs. This block includes the following API endpoints:

  * **Shipping Account**
    * **Get Accounts**: Retrieve a list of the Amazon shipping accounts.
    * **Add Account**: Add a new Amazon shipping account.
    * **Get Account**: Retrieve details of a specific Amazon shipping account.
    * **Update Account**: Update details of an existing Amazon shipping account.
    * **Link Locations**: Link shipping locations to an Amazon shipping account.
    * **Get Associated Locations**: Retrieve locations linked to the Amazon shipping account.
    * **Get Associated Location**: Retrieve details for a specific Amazon associated location.
  * **Shipments**
    * **Create Shipment**: Create a new Amazon shipment request.
    * **Print Label**: Generate a label for the Amazon shipment.
  * **Amazon shipping account screen**. As part of the new integration, customer users and Carrier Account Administrators can now configure the Amazon shipping account via the SAPIENT UI for creating shipments.  The **Add Shipping Account** screen will now include Amazon as a carrier for selection, with mandatory fields required for configuration.

  > 📘 *Note*
  >
  > *For more information on how to set up an Amazon shipping account, refer to the<Anchor label="Add Amazon Shipping Account" target="_blank" href="https://docs.intersoftsapient.net/docs/add-amazon-shipping-account">Add Amazon Shipping Account</Anchor> user guide.*

  ## New integration - FedEx International Connect

  The FedEx International Connect integration has been added to the SAPIENT system. This integration supports shipping domestically within the UK, and to EU and Rest of World destinations. With this addition, the following information has been added to the swagger documentation:

  **New API endpoints**. A new **FEDEX INTERNATIONAL CONNECT** block has been added to our carrier-specific APIs. This block includes the following API endpoints:

  * **Shipping Account**
    * **Get Accounts**: Retrieve a list of the FedEx International Connect shipping accounts.
    * **Add Account**: Add a new FedEx International Connect shipping account.
    * **Get Account**: Retrieve details of a specific FedEx International Connect shipping account.
    * **Update Account**: Update details of an existing FedEx International Connect shipping account.
    * **Link Locations**: Link shipping locations to an FedEx International Connect shipping accounts.
    * **Get Associated Locations**: Retrieve locations linked to the FedEx International Connect shipping account.
    * **Get Associated Location**: Retrieve details for a specific FedEx International Connect associated location.
  * **Shipments**
    * **Create Shipment**: Create a new FedEx International Connect shipment request.
    * **Print Label**: Generate a label for the FedEx International Connect shipment.
  * **FedEx International Connect shipping account screen**. As part of the new integration, customer users and Carrier Account Administrators can now configure the FedEx International Connect shipping account via the SAPIENT UI for creating shipments.  The **Add Shipping Account** screen will now include FedEx International Connect as a carrier for selection, with mandatory fields required for configuration. Additionally, carrier-specific fields for the FedEx International Connect integration include a mandatory **Shipper Website URL** and  an **API Key** (to be provided by the carrier).

  > 📘 *Note*
  >
  > *For more information on how to set up a FedEx International Connect shipping account, refer to the<Anchor label="Add FedEx International Connect Shipping Account" target="_blank" href="https://docs.intersoftsapient.net/docs/add-fedex-international-shipping-account">Add FedEx International Connect Shipping Account</Anchor> user guide.*

  ## Swagger documentation updates

  The AnPost Create Shipment swagger has been updated to contain notes on some additional validation rules that apply to shipments to USA. The fields that have been updated are:

  * **Destination** > **Address** object
  * **Items** object > **HSCode**

  > 📘 *Note*
  >
  > *For more information on these updates, refer to the<Anchor label="An Post Create Shipment API swagger" target="_blank" href="https://docs.intersoftsapient.net/reference/post_v4-shipments-anpost">An Post Create Shipment API swagger</Anchor> documentation.*
</Accordion>

<Accordion title="SAPIENT release notes - March 18, 2026" icon="">
  ## Download API spec from Developers Hub

  A new Download API Spec feature has been added to the SAPIENT Developers Hub. Each block in the left navigation pane of the [API References](https://docs.intersoftsapient.net/reference/get_v4-carriers) tab now includes a dedicated page with a **Download API Spec** button.

  With this feature added, users can now easily download the API specification for each set of carrier and SAPIENT CORE endpoints directly to their local computer, improving accessibility and offline reference.

  <Image align="center" border={true} src="https://files.readme.io/0e5ba8b8966556456295fb4f0433c30423d1195a4d14a1168955a915644a976e-image.png" />

  ## System maintenence

  Routine back-end work and minor UI improvements were addressed and deployed.
</Accordion>

<Accordion title="SAPIENT release notes - April 08, 2026" icon="">
  ## Multi-Factor Authentication (MFA) for SAPIENT

  Multi‑Factor Authentication (MFA) has been added to the SAPIENT user interface to enhance account security. When enabled at customer account level, all users are required to complete a two‑step verification during login. After entering their username and password, a one‑time verification code is sent to the user’s registered SAPIENT email address, which must be entered to access the platform. Additionally, users can choose to snooze the MFA prompt for up to 14 days.

  > 📘 *Note*
  >
  > *Please note that the MFA feature will not be enforced upon deployment. By default, it will be disabled for all customer accounts unless it is activated by a Customer Administrator with the**User Administrator** permission*.
  >
  > *For more information on the MFA process, refer to the following guides:*
  >
  > * *[Enable Multi-Factor Authentication on SAPIENT](https://docs.intersoftsapient.net/docs/enable-multi-factor-authentication-on-sapient)*
  > * *[Log in to SAPIENT](https://docs.intersoftsapient.net/docs/log-in)*

  ## Handle invalid tracking numbers

  The SAPIENT's **Trackings** API  has been enhanced to improve visibility and handling of invalid tracking numbers submitted in batch requests.

  The API now accepts and processes all tracking numbers supplied in a single request (up to 1,000), without failing the entire batch when invalid entries are present. Valid tracking numbers are registered as normal, while invalid tracking numbers are identified and excluded from registration with Royal Mail.

  Invalid tracking numbers are automatically marked as "DO NOT TRACK," and a corresponding tracking event is generated and sent to the customer via the Intersoft tracking webhook. This event provides clear feedback without impacting the processing of valid tracking numbers.

  > 📘 *Note*
  >
  > *For more information, refer to the[Handle invalid tracking numbers](https://docs.intersoftsapient.net/docs/handling-invalid-tracking-numbers) guide.*

  ## Tracking Webhook setup - UI enhancements

  A new mandatory **Notification Email** field has been added to the **Tracking Webhook** setup screen in SAPIENT. This email address will be used to receive webhook suspension notifications and replaces the previous behaviour where notifications were sent to the primary user email on the customer account.

  > 📘 *Note*
  >
  > *Customers who already have a tracking webhook configured on SAPIENT, the new email field will be pre‑populated with the primary user email. Customers can review and update the email at any time.*

  ## New integration - DPD Netherlands (NL)

  The DPD Netherlands (NL) integration has been added to the SAPIENT system. This integration supports shipping domestically within the Netherlands, and to EU, GB, and Rest of World destinations. With this addition, the following information has been added to the swagger documentation:

  **New API endpoints**. A new **DPD NETHERLANDS** block has been added to our carrier-specific APIs. This block includes the following API endpoints:

  * **Shipping Account**
    * **Get Accounts**: Retrieve a list of the DPD Netherlands shipping accounts.
    * **Add Account**: Add a new DPD Netherlands shipping account.
    * **Get Account**: Retrieve details of a specific DPD Netherlands shipping account.
    * **Update Account**: Update details of an existing DPD Netherlands shipping account.
    * **Link Locations**: Link shipping locations to a DPD Netherlands shipping accounts.
    * **Get Associated Locations**: Retrieve locations linked to the DPD Netherlands shipping account.
    * **Get Associated Location**: Retrieve details for a specific DPD Netherlands associated location.
  * **Shipments**
    * **Create Shipment**: Create a new DPD Netherlands shipment request.
    * **Print Label**: Generate a label for the DPD Netherlands shipment.
  * **DPD Netherlands shipping account screen**. As part of the new integration, customer users and Carrier Account Administrators can now configure the DPD Netherlands shipping account via the SAPIENT UI for creating shipments.  The **Add Shipping Account** screen now includes DPD Netherlands as a carrier for selection, with mandatory fields required for configuration.

  ## Swagger updates

  The query and response field descriptions for our following CORE API endpoints have been updated to improve clarity and support correct usage of the API:

  * **Get Products**
  * **Add Product**
  * **Delete Product**
  * **Get Product**
  * **Update Product**
</Accordion>

<Accordion title="SAPIENT release notes - April 28, 2026" icon="">
  ## New integration - DHL Germany

  The DHL Germany (DE) integration has been added to the SAPIENT system. This integration supports shipping domestically within Germany, and to EU, GB, and Rest of World destinations. With this addition, the following information has been added to the swagger documentation:

  **New API endpoints**. A new **DHL GERMANY** block has been added to our carrier-specific APIs. This block includes the following API endpoints:

  * **Shipping Account**
    * **Get Accounts**: Retrieve a list of the DHL Germany shipping accounts.
    * **Add Account**: Add a new DHL Germany shipping account.
    * **Get Account**: Retrieve details of a specific DHL Germany shipping account.
    * **Update Account**: Update details of an existing DHL Germany shipping account.
    * **Link Locations**: Link shipping locations to a DHL Germany shipping accounts.
    * **Get Associated Locations**: Retrieve locations linked to the DHL Germany shipping account.
    * **Get Associated Location**: Retrieve details for a specific DHL Germany associated location.
  * **Shipments**
    * **Create Shipment**: Create a new DHL Germany shipment request.
    * **Print Label**: Generate a label for the DHL Germany shipment.
  * **DHL Germany shipping account screen**. As part of the new integration, customer users and Carrier Account Administrators can now configure the DHL Germany shipping account via the SAPIENT UI for creating shipments.  The **Add Shipping Account** screen now includes DHL Germany as a carrier for selection, with mandatory fields required for configuration.
  * **Tracking**: Enables customers to receive tracking updates through their integration with the SAPIENT tracking webhook.
  * **Manifest shipment**: Enable customers to retrieve information about shipment manifests created by the system and track when shipments have been successfully manifested with DHL Germany.

  > 📘 *Note*
  >
  > *For more information on this integration, refer to the[DHL Germany](https://docs.intersoftsapient.net/docs/dhl-germany-de) user guides.*

  ## Domestic Royal Mail Tracked Returns label updates

  The footer text on the following domestic Royal Mail Tracked Returns label templates has been updated to provide clear guidance on where to drop off the return parcels.

  | Product Code | Product Name              |
  | :----------- | :------------------------ |
  | **ITA**      | Import Tracked Returns 24 |
  | **TSN**      | Tracked Returns 24        |
  | **ITB**      | Import Tracked Returns 48 |
  | **TSS**      | Tracked Returns 48        |

  <Image align="center" border={true} src="https://files.readme.io/4df4a1f719b1868b12444eaf998f41da8fbff6864fd2b3914f04ec84e0e0065b-Tracked_Returns_24_Label.png" width="350px" />

  ## System maintenance

  Routine back-end work, minor UI enhancements, and technical improvements were addressed and deployed.
</Accordion>

<Accordion title="SAPIENT release notes - May 19, 2026" icon="">
  ## Royal Mail - Parcelforce dimension validation update

  The dimension validation for Royal Mail - Parcelforce International non‑Consumer shipments has been removed. The system will now allow shipments where parcel dimensions exceed stored format limits, ensuring valid shipments are not rejected due to restricted validation.

  ## Tracking Webhook retry logic updates

  INTERSOFT Tracking Webhook delivery continues to follow the existing retry policy. Previously, certain errors caused the webhook to be suspended immediately, resulting in failed delivery attempts. This behaviour has been updated so that all delivery errors now enter the retry process rather than triggering immediate suspension. Once the retry limit is exhausted and the webhook becomes suspended, it remains suspended and no further delivery attempts or retries are performed.

  ## Royal Mail swagger documentation updates

  ## Miscellaneous enhancements

  The following enhancements have been made to the **SAPIENT ROYAL MAIL API** endpoints.

  * **Create Shipment**:  The following two new categories have been added to the **Customs** > **ReasonForExport** field in addition to the existing categories:
    * **ECommerce Sale of Goods** - for B2C or D2C shipments, such as goods sold directly to consumers via online retail.
    * **Commercial Sale of Goods** - for B2B shipments, covering business to business commercial sales.

  This is done so that the shipments are correctly classified as e-commerce or commercial sales, ensuring compliance with Royal Mail's latest specification.

  > 📘 *Note*
  >
  > *Please keep in mind the following:*
  >
  > * *If the existing**Sale of Goods** value is selected as the reason for export, the system automatically determines whether the shipment is **Ecommerce (B2C or D2C)** or **Commercial (B2B)** based on the value provided in the **BusinessTransactionType** field in the create shipment request.*
  > * *If any of the new reason for export values are requested in the**Print Document** API, they will be displayed in the generated CN23 document.*
  > * *This enhancement will be live starting 1st June 2026.*
  >
  > *For more information, refer to the<Anchor label="Create Shipment" target="_blank" href="https://docs.intersoftsapient.net/reference/post_v4-shipments-rm">Create Shipment</Anchor> and [Print Document](https://docs.intersoftsapient.net/reference/post_v4-shipments-printdocument-carriercode-shipmentid) API endpoints.*

  * **Get Carrier Services**. A new **Services** > **Get Carrier Services** endpoint has been added to the **SAPIENT ROYAL MAIL API** block, allowing users to retrieve the service levels associated with each requested service code.

  ```curl
  [
    {
      "ServiceCode": "CRL1",
      "Description": "Royal Mail 24 Standard/Signed For (Parcel - Daily Rate Service)",
      "CarrierSpecifics": {
        "ServiceLevels": [
          "01",
          "02"
        ]
      }
    }
  ]
  ```

  <p style={{ textAlign: "center" }}>
    <em>Response payload example</em>
  </p>

  ## Field description updates

  The query and response field descriptions for the following SAPIENT ROYAL MAIL API endpoints have been updated to improve clarity and support correct usage of the API:

  <Columns layout="fixed">
    <Column>
      * **Shipping Accounts**
        * Get Accounts
        * Add Account
        * Get Account
        * Update Account
        * Link Locations
        * Get Associated Locations
        * Get Associate Location
        * Update Associated Location
    </Column>

    <Column>
      * **Shipments**
        * Create Shipment
        * Print Label
        * Print My Label QR Code
        * Pre Allocate Tracking Number
    </Column>

    <Column>
      * **Collections**
        * Book Collection
        * Cancel Collection
        * Get Collection Timeslots
    </Column>

    <Column>
      * **Offline Barcode Range**
        * Get Barcode Range
    </Column>
  </Columns>

  <Columns layout="auto">
    <Column>
      * **International Arrivals Containers**
        * Add Container
        * Get Containers
        * Update Containers
        * Add/Remove Shipments
        * Delete Containers
        * Get Containers
    </Column>
  </Columns>

  ## DX Freight swagger documentation updates

  The query and response field descriptions for the following SAPIENT DX FREIGHT API endpoints have been updated to improve clarity and support correct usage of the API:

  * **Shipments**
    * Create Shipment
    * Print Label
  * **Shipping Accounts**
    * Get Accounts
    * Add Account
    * Get Account
    * Update Account
    * Link Locations
    * Get Associated Locations
    * Get Associate Location
    ## DPD UK swagger documentation updates

  A new **CarrierDetails** > **Barcode** field has been added at the **Packages** level in the **Create Shipment** endpoint response, allowing users to scan and track shipments and match them against the stored barcode information.

  ```curl
  "LabelFormat": "PDF",
      "Packages": [
          {
              "CarrierDetails": {
                  "Barcode": "%BT370QB15501999000067812826"
              },
              "PackageOccurrence": 1,
              "TrackingNumber": "15501999000067",
              "CarrierTrackingUrl": "https://track.dpd.co.uk/search?reference=15501999000067"
          }
      ]

  ```

  <p style={{ textAlign: "center" }}>
    <em>Response payload example</em>
  </p>

  ## SAPIENT CORE API swagger documention updates

  A new **CarrierSpecifics** object has been added to the **Get Carrier Services** endpoint response to include a **ServiceLevels** field, allowing users to retrieve the service levels associated with each requested service code (if available).
</Accordion>
<Accordion title="SAPIENT release notes - June 09, 2026" icon="">
  ## New integration - DHL Express
The DHL Express integration has been added to the SAPIENT system. This integration supports shipping domestically within UK, to EU and Rest of World destinations. With this addition, the following information has been added to the swagger documentation:

**New API endpoints**. A new **DHL EXPRESS** block has been added to our carrier-specific APIs. This block includes the following API endpoints:

* **Shipping Account**
  * **Get Accounts**: Retrieve a list of the DHL Express shipping accounts.
  * **Add Account**: Add a new DHL Express shipping account.
  * **Get Account**: Retrieve details of a specific DHL Express shipping account.
  * **Update Account**: Update details of an existing DHL Express shipping account.
  * **Link Locations**: Link shipping locations to a DHL Express shipping accounts.
  * **Get Associated Locations**: Retrieve locations linked to the DHL Express shipping account.
  * **Get Associated Location**: Retrieve details for a specific DHL Express associated location.
* **Shipments**
  * **Create Shipment**: Create a new DHL Express shipment request.
  * **Print Label**: Generate a label for the DHL Express shipment.
* **DHL Express shipping account screen**. As part of the new integration, customer users and Carrier Account Administrators can now configure the DHL Express shipping account via the SAPIENT UI for creating shipments.  The **Add Shipping Account** screen now includes DHL Express as a carrier for selection, with mandatory fields required for configuration, along with options to configure Archive Labels and Paperless Trade (PLT).
* **Tracking**: Enables customers to receive tracking updates through their integration with the SAPIENT tracking webhook.
* **Manifest shipment**: Enable customers to retrieve information about shipment manifests created by the system and track when shipments have been successfully manifested with DHL Express.

> 📘 _Note_
>
  > _For more information on this integration, refer to the <Anchor label="DHL Express" target="_blank" href="https://docs.intersoftsapient.net/docs/dhl-express">DHL Express</Anchor> section._

  ## Handling Pre-registration number
For Royal Mail international shipments, pre-registration values (such as IOSS or PRS) sourced from Customs Settings are now applied only when supported by the selected service and destination. If the selected route does not support the preregistration type, the value is no longer applied and the shipment is processed without validation errors.

This update prevents valid shipments from being rejected due to unsupported preregistration data and ensures successful shipment creation where applicable.
</Accordion>

<br />
