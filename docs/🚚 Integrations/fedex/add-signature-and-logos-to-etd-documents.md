---
title: 'Configure ETD for FedEx shipping account '
excerpt: >-
  This setting enables the FexEx customers to add the letterhead image and
  signatures, which can be included on their Electronic Trade Document (ETD)
  related to the shipments.
deprecated: false
hidden: false
icon: fad fa-file-doc
metadata:
  robots: index
---
In SAPIENT, you can add letterhead images and signatures to your ETDs to ensure that all shipping documents are consistent with the company’s branding, providing authentic and trustworthy representation of the business, particularly when dealing with customers and partners.

During the [FedEx shipping account creation process](https://docs.intersoftsapient.net/v4.04/docs/add-fedex-shipping-account), if you have selected the **Enable Electronic Trade Documents (ETD)** checkbox, then you can configure the ETD data via the **Signatures and Logos** feature of SAPIENT.

## How to configure ETD for a FedEx shipping account

To add letterhead image and signature to your ETDs in SAPIENT, perform the steps as explained in the following procedure.

<Callout icon="🚧" theme="warn">
  ### _Important_

  _The&#x20;_**_ELECTRONIC TRADE DOCUMENTS_**_&#x20;block is only available if the&#x20;_**_Shipping Location_**_&#x20;field is set to&#x20;_**_All_**_&#x20;and ETD is enabled for your shipping account._
</Callout>

<ToggleList>
  <ToggleListItem title="1. Select the Signatures and Logos page">
    In the left navigation panel, select **Customs Settings** > **Signatures and Logos**.

    <Image align="center" border={true} src="https://files.readme.io/00c81ec3f8935f700829d2ec2e8ed30d0fa0bd6fc0a5d658684f8609202fab93-Signatures_and_logos_option.png" caption="Accessing signatures and logos" />

    Alternatively, select the link that was displayed with your successful FedEx account creation notification, directing you to the **Signatures and Logos** page for ETD configuration.

    <Image align="center" border={true} src="https://files.readme.io/1b876fd165eaa4b02e5b3b5f93d838fdcb8cdad9798ebd58c6f7ed45a01b92e4-ETD_config_notification.png" />

    ***
  </ToggleListItem>

  <br />

  <ToggleListItem title="2. Select option to add signature and logo">
    In the **Signatures and Logos** page that opens, select ![](https://files.readme.io/2e03049feb3d93343e3c10aeb0958e95489136884c6fea556824482504e36176-Add_sign_and_logo_button.png).

    <Image align="center" border={true} src="https://files.readme.io/af0587aafff2921d2ae9f21523162ad00f35e5b667c43e7d98d5c5844644d248-Add_sign_and_logo_option.png" caption="Accessing option to add signature and logo" />

    ***
  </ToggleListItem>

  <br />

  <ToggleListItem title="3. Select the FedEx shipping account">
    In the **Add Signature and Logo** form that opens, in the **SHIPPING ACCOUNT** block, from the dropdown menu, select your FedEx <Glossary>shipping account</Glossary> for which you want to add the ETD documents.

    <Image align="center" border={true} src="https://files.readme.io/2a35a1f372f43c2ca5e3fb4e861cdaff59b039a5d61a870f882cdee2c37629bd-Selecting_FedEx_shipping_account_for_Logos.png" caption="Selecting shipping account" />

    ***
  </ToggleListItem>

  <br />

  <ToggleListItem title="4. Add electronic trade documents">
    In the **ELECTRONIC TRADE DOCUMENTS** block that opens, enter the necessary information as explained in the following table.

    <Image align="center" border={true} src="https://files.readme.io/e91ef385e6f0f934f5eb9b32ca72cf0e6a1b9cc2a636daf98659d25f7b655c36-FedEx_Logo_screen.png" caption="Entering signature, logo, and their details" />

    <br />

    <Table align={["center","left"]}>
      <thead>
        <tr>
          <th>
            Element
          </th>

          <th>
            Description
          </th>
        </tr>
      </thead>

      <tbody>
        <tr>
          <td>
            **Letterhead Image**
          </td>

          <td>
            Select **Choose File**, follow the prompts of your computer, and then select the letterhead image that you want to upload.

            Alternatively, drag the desired logo file to this field.
          </td>
        </tr>

        <tr>
          <td>
            **ETD Signature Image**
          </td>

          <td>
            Select **Choose File**, follow the prompts of your computer, and then select the ETD signature image file that you want to upload.

            Alternatively, drag the desired logo file to this field.
          </td>
        </tr>

        <tr>
          <td>
            **ETD Declaration Statement**
          </td>

          <td>
            Carefully read the ETD declaration statement before proceeding.

            *`Note`: This field is editable and if needed, you can modify this statement as per your business requirements.*
          </td>
        </tr>

        <tr>
          <td>
            **Add Documents & Images**
          </td>

          <td>
            Select ![](https://files.readme.io/f7ceba9e8e14a6f791412024b91067a8b8d456a409caa520dd553eec1af3ed42-Add_documents_and_images_button.png) to save your documents.
          </td>
        </tr>

        <tr>
          <td>
            **Cancel**
          </td>

          <td>
            Select ![](https://files.readme.io/866310e4fa14cf86a31a827c203da1fa0b2f7dbd5f52e868b6d96692fc223f3d-Cancel_button.png) to discard the changes and close the form. No changes are saved in this case.
          </td>
        </tr>
      </tbody>
    </Table>

    <br />

    > 📘 *Note*
    >
    > *The **SIGNATURES & LOGO** block is not mandatory, if you do not want to configure it, then skip this section and select ![](https://files.readme.io/57defd548ada4f381b9968a291bb45d55b435feab09408e30266126b303228fc-Add_documents_and_images_button.png) to save your uploaded ETD documents. You may want to configure this block, for example, in cases where some destinations do not support ETD, and you wish to attach a <Glossary>commercial invoice</Glossary> to the parcel. To configure this block, refer to the [Add Signatures and Logos](https://docs.intersoftsapient.net/docs/add-signature-and-logo#/) section.*

    ***
  </ToggleListItem>

  <br />

  <ToggleListItem title="5. Start using the ETD documents">
    Once saved, the letterhead image and signatures are added successfully and appear in the **Signatures and Logos** list. These can now be used in any relevant ETDs.

    <Callout icon="💡" theme="default">
      ### *Tip*

      If you want to remove a specific ETD configuration, then in the **Signatures and Logos** list, next to the one you want to delete, select ![](https://files.readme.io/0979c7211f5ae99308ba3f765bd083d41949895562626a4f0cc33acd80b30762-Trash_icon.png).

      <Image align="center" border={true} src="https://files.readme.io/18854da926a99e35b6280bbb19445cac623a73a7f01d8cb9df4c99cd2a6fe6e9-Removing_item.png" caption="Deleting pre-registration number" />

      *Please be advised that the delete option only removes the ETD documents from the SAPIENT system, not the FedEx system. In order to update your ETD documents, you must replace them with the new ones so that they are replaced in the FedEx system next time when you call the create shipment API.*

      Alternatively, if you do not want to use any documents, simply [clear the Electronic Trade Documents (ETD) checkbox](https://docs.intersoftsapient.net/docs/specify-shipping-account-details#/).
    </Callout>
  </ToggleListItem>
</ToggleList>

***

### See also

<Cards columns={2}>
  <Card title="Add FedEx shipping account" icon="fa-truck-fast" href="https://docs.intersoftsapient.net/v4.04/docs/add-fedex-shipping-account">
    Enable ETD while specifying the FedEx shipping account details.
  </Card>

  <Card title="Add signatures and logos" icon="fa-file-signature" href="https://docs.intersoftsapient.net/docs/add-signature-and-logo#/">
    Configure signatures and logos for cases where you need to attach a commercial invoice to the parcel.
  </Card>
</Cards>

<br />