---
title: Set up manifest webhook (coming soon)
excerpt: >-
  A _Webhook_ is a tool used particularly in API integrations, to receive
  real-time updates or notifications whenever specific events occur in the
  system (such as shipping updates, status changes, and so on). It is commonly
  used in shipping software to keep track of shipments and their statuses
  without the need for constant polling or manual checking.
deprecated: false
hidden: false
icon: fad fa-spider-web
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
The manifest webhook feature has several purposes:

* **Real-time Updates**: to receive immediate notifications about shipment activities or status changes, ensuring that the information is up-to-date.
* **Integration**: to better integration with various services and APIs by providing a mechanism to push data and initiate workflows based on shipping events.
* **Error Handling**: to notify systems about issues or failures in manifest processing, allowing for timely corrections.

The Manifests webhook is developed as an alternative to the Get Manifest Status endpoint. Instead of
calling to retrieve the manifest status and details, you can set up the webhook to receive the manifest details when the manifest request has finished processing.

> 🚧 _Important_
>
> _The manifest webhook is only used if you are using the **Manifest Shipments Async** endpoint to manifest asynchronously._

To set up the manifest webhook connection in SAPIENT, follow the instructions as explained in the following procedure.

1. On the SAPIENT **Home** page, in the left navigation panel, select **API** > **Webhooks**. In the page that opens,  select the **Manifest Webhook** tab.

<Image align="center" alt="Accessing tracking webhook" border={true} caption="Accessing tracking webhook" src="https://files.readme.io/2e9bf0ceab366ca1de8ba425c319222ec683bf3338c285a74952d5d9baae6c05-Manifest_webhook_tab.png" />

2. In the **WEBHOOK DETAILS** block of the **Tracking Webhook** tab, enter the necessary information as described in the following table.

<Image align="center" border={true} width="500px" src="https://files.readme.io/f1b9e78c168e83ad35f8c5df9fccd857c57a045811daba57e58b2512f11b42f6-Manifest_webhook_details_block.png" className="border" />

<AsteridkForMandatoryElements />

<Table align={["center","left","left"]}>
  <thead>
    <tr>
      <th>
        Element
      </th>

      <th>
        Basic authentication
      </th>

      <th>
        OAuth2 authentication
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        **Authentication type***
      </td>

      <td>
        From the dropdown menu, if applicable, select the **Basic** authentication type.

        Basic is a simple authentication type built into the HTTP protocol. It involves sending the user's credentials (username and password) in an encoded format (Base64) within an HTTP header.
      </td>

      <td>
        From the dropdown menu, if applicable, select the **OAuth2** authentication type.

        oAuth2 is a specific protocol used for authorisation that allows third-party applications to access the user's data without exposing their credentials.
      </td>
    </tr>

    <tr>
      <td>
        **Endpoint URL***
      </td>

      <td>
        Enter your endpoint URL. This is the URL that we use to connect for identification purposes.
      </td>

      <td>
        Enter your endpoint URL. This is the URL that we use to connect for identification purposes.
      </td>
    </tr>

    <tr>
      <td>
        **Username***
      </td>

      <td>
        Enter your username to identify and authenticate the INTERSOFT payload.
      </td>

      <td>
        ❌ Not applicable
      </td>
    </tr>

    <tr>
      <td>
        **Password***
      </td>

      <td>
        Enter the password for the username you entered to identify and authenticate the INTERSOFT payload.
      </td>

      <td>
        ❌ Not applicable
      </td>
    </tr>

    <tr>
      <td>
        **Token URL***
      </td>

      <td>
        ❌ Not applicable
      </td>

      <td>
        Enter your token URL. This is an endpoint we use to connect and get the security token.
      </td>
    </tr>

    <tr>
      <td>
        **Client ID***
      </td>

      <td>
        ❌ Not applicable
      </td>

      <td>
        Enter your client ID  to identify and authenticate the INTERSOFT payload.
      </td>
    </tr>

    <tr>
      <td>
        **Secret***
      </td>

      <td>
        ❌ Not applicable
      </td>

      <td>
        Enter your secret to identify and authenticate the INTERSOFT payload
      </td>
    </tr>
  </tbody>
</Table>

3. After entering all the necessary details, select ![](https://files.readme.io/dcabcea774e82fdcf39f03bfcdcd2d95520a6aead65cb9bd47e7ccc32a8c085c-Test_button.png) to check if the setup is configured correctly. Once the test has been completed, and the setup configuration is correct, the webhook is activated and the following success response is displayed:

<Image align="center" alt="Success response" border={true} caption="Success response" src="https://files.readme.io/0994fa6-image.png" width="660px" />

If for some reason, the connectivity test fails, the following message is displayed:

<Image align="center" alt="Failed connection response" border={true} caption="Failed connection response" src="https://files.readme.io/65a4983-image.png" width="660px" />

4. After, turn on the **Active** toggle if you wany to activate the manifest webhook.

<Image align="center" alt="Activating tracking webhook" border={true} caption="Activating manifest webhook" src="https://files.readme.io/a76feb6-image.png" width="660px" />

> 🚧 _Important_
>
> _The webhook only works if it is in the**Active** state. Any changes made to the webhook configuration deactivates it. Therefore, make sure the toggle is set to **Active** whenever the configuration is updated._

5. Select ![](https://files.readme.io/2f9b4304c20f01f6272a39bbdeef71a6abc9242aec6337ed7c3926401517f2f1-save_changes_button_2.png) to confirm the setup completion.

The webhook payload will be sent for manifest requests with a status of both `COMPLETE` and
`FAILED`.

* If the **manifestStatus** = `COMPLETE`, the webhook payload will be the same as the **Get Manifest Status**
  endpoint detailed response.

**Example payload**

```
{
  "ManifestRequestId": "3a0c17c5-0ca4-455c-ac65-a20d95e656bc",
  "ManifestRequestStatus": "COMPLETE",
  "ManifestCount": 1,
    "Manifests": [
      {
        "CarrierCode": "RM",
        "CreatedDateUtc": "2024-06-17T10:36:20.072Z",
        "ManifestDate": "2024-06-17",
        "ManifestImage": "jVBERw0KGgoAAAANSUhEUgAA.....A4QAAAXcCAYAAAB6Q0CbAAAAAXNSR0IArs4",
        "ManifestNumber": "ISH2802532",
        "Service": "CRL1",
        "ShippingAccount": {
          "AccountAlias": "Account 1",
          "AccountName": "AB VideoGames",
          "AccountNumber": "0123456789",
          "ShippingAccountId": "3fa85f64-5717-4562-b3fc-2c963f66afa6"
        },
        "ShippingLocation": {
          "LocationAlias": "Main Warehouse",
          "LocationCountry": "GB",
          "LocationPostcode": "TW20 0HJ",
          "ShippingLocationId": "3fa85f64-5717-4562-b3fc-2c963f66afa6"
        },
        "TotalItems": 562,
        "TotalShipments": 562,
        "TotalWeight": 545.612,
        "WeightUnitOfMeasure": "KG"
      }
    ],
  }
```

* If the **manifestStatus** = `FAILED`, the webhook payload will be the same as the **Get Manifest Status**
  endpoint FailedStatus response – that is, it will contain a FailureReason and error details.

**Failed request example**

```
 {
       "ManifestRequestId": "3a0c17c5-0ca4-455c-ac65-a20d95e656bc",  
 "ManifestRequestStatus": "FAILED",  
 "ManifestCount": 10,  
 "FailedReason": "Reason for failure",{  
 "Message": "Error message ",   
 "Errors": "list of errors",[  
       }
   }
```

> 🚧 _Important_
>
> _If the webhook call is not sent successfully, SAPIENT will retry sending the webhook at the following
> intervals:_
>
> * _5 mins_
> * _15 mins_
> * _60 mins_
>
> _If the retry attempts are all unsuccessful, the webhook call will fail and SAPIENT will no longer send it again. In this case the Webhook will be suspended. For more information on how to handle the webhook suspension, refer to the [Webhook suspension](https://docs.intersoftsapient.net/docs/webhook-suspension#/) section._

**See also**

* <Anchor label="Manifest shipments asynchronously" target="_blank" href="https://docs.intersoftsapient.net/docs/manifest-shipment-asychronously#/">Manifest shipments asynchronously</Anchor>
* [Manifest shipment from UI](https://docs.intersoftsapient.net/docs/manifesting-shipments#/)
* [View manifest history](https://docs.intersoftsapient.net/docs/manifest-history#/)

<KeyPress keyCombo="Alt+T">You hit control + d. GREAT JOB!!!!</KeyPress>

<br />
