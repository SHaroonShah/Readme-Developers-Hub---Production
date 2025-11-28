---
title: Recall shipment
excerpt: >-
  Learn how to recall cancelled shipments in SAPIENT through both UI and API
  methods to resume shipment processing.
deprecated: false
hidden: false
icon: fad fa-circle-arrow-left
link:
  new_tab: false
metadata:
  title: ''
  description: >-
    Recalling a shipment refers to the process of reinstating or resuming the
    shipment that was previously cancelled.
  robots: index
---
After you have [cancelled](https://docs.intersoftsapient.net/docs/view-cancelled-shipments) the <Glossary>shipment</Glossary> in SAPIENT, you can anytime recall it and proceed with its processing. This might involve taking necessary actions to fulfil the order again after addressing the reasons for its cancellation.

> 💡 *Tip*
>
> *You can recall the shipments both via UI and the API. For more information on how to recall shipments via API, refer to the [API References](https://docs.intersoftsapient.net/reference/put_v4-shipments-status) section.*

To recall shipment(s), follow the steps as explained in the following procedure.

1. In the side navigation panel, select the **Shipment Processing** > **Cancelled** option.

<Image align="center" alt="Accessing shipments" border={true} caption="Accessing canceled shipments" src="https://files.readme.io/3c65a988ba9ce65069de9aaffb097b351b1fc930b55dcb341690a1f3e178322d-Accessing_cancelled_shipments.png" />

2. In the **Cancelled Shipments** page that opens, select the checkboxes next to the shipments you want to recall, and then select ![alt text](https://files.readme.io/79126340250abbe6f8c76ada767569f8015d1010731e0f45f0c35b2ea8e59fbd-Recall_shipments_button.png).

<Image align="center" alt="Recalling shipment" border={true} caption="Recalling shipments" src="https://files.readme.io/7dd1d2279a2b79ecebfd8ec87b54829eed58a38965b0bbc8c851a26d7b97f86e-Recall_shipments_option.png" />

3. In the confirmation dialog that appears, select **Yes**.

<Image align="center" alt="Confirming shipment recalling" border={false} caption="Confirming shipment recalling" src="https://files.readme.io/19f0b9332e273ee9df9bf4c94083980f8361c7ec4df29feb79081577da31ed54-Confirming_shipment_recalling.png" width="350px" />

3. Once confirmed, the shipment(s) is removed from the **Cancelled Shipments** list and goes back to its previous status and is ready for manifesting.

> 📘 *Note*
>
> *If the shipment was canceled while it was held and was recalled, then the recalled shipment goes back to the held status—and if you wish to manifest it, then you must release it.*