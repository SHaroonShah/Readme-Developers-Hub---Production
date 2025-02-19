---
title: Cancel shipment
excerpt: >-
  A shipment can be set to *Cancelled* when it has been officially stopped and
  is not going to be delivered. Cancellations may occur for various reasons,
  including customer requests or logistical issues.
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
In SAPIENT, you can cancel the <Glossary>shipments</Glossary> to ensure that resources can be reallocated and allow users to manage customer expectations. The shipment can be canceled if it has been confirmed by being manifested.

> 💡 *Tip*
>
> *You can cancel the shipments both via UI and the API. For more information on how to cancel shipments via API, refer to the[API References](https://docs.intersoftsapient.net/reference/put_v4-shipments-status) section.*

To cancel shipment(s), follow the steps as explained in the following procedure.

1. In the side navigation panel, select the **Shipment Processing** > **Manifesting** option.

<Image alt="Accessing shipments" align="center" border={true} src="https://files.readme.io/43b41b65377780fd19531fd2378483c9b0c7d99c88b2c5242e584ef4225c5dae-Accessing_manifesting_option.png">
  Accessing manifesting option
</Image>

2. In the **Manifesting** page that opens, you can sort the list either by <Glossary>carrier</Glossary> or <Glossary>shipping account</Glossary>. You can also change the <Glossary>shipping location</Glossary> by selecting the **Change Location** button. 

<Image alt="Specifying filters" align="center" border={true} src="https://files.readme.io/41603935fe204b0f21f146742408bd60584a5659ebb2a31c9302a475d93d24cf-sorting_and_changing_location.png">
  Sorting list and changing location
</Image>

3. Additionally, you can filter the table data with the shipment status or carrier service by selecting the needed statuses and carrier service codes provided in the **Narrow by Status** and **Narrow by Service** blocks, respectively. 

<Image alt="Viewing shipments" align="center" border={true} src="https://files.readme.io/4f3b0dfcf1502b52e1c71c7448e95814a0afee4d9d9b865ba27082f2acbde5ed-Narrowing_manifesting.png">
  Viewing filtered shipments
</Image>

4. After you have filtered your desired shipments, next to the shipment that you want to cancel, select ![alt text](https://files.readme.io/ade8694f40f0b89e1cfab543051a5b77f7a307552c22b1c0105f7f2439dd065e-View_button.png). 
5. On the page that opens, next to the shipment, select the checkbox and then click  ![alt text](https://files.readme.io/ce57b2272ffff135c3c09d4b532c2cbff21b8ffeaaacb4bb668edcbd00c2e67c-Cancel_shipments_button.png). 

<Image alt="Accessing option to cancel shipments" align="center" border={true} src="https://files.readme.io/1b5ebf0996d78e8b255de85c8da7e377d6f19524f9899bc8155d4b48f34ea0d0-Canceling_shipments.png">
  Accessing option to cancel shipments
</Image>

4. In the confirmation dialog that appears, enter the reason for canceling the shipment, and then select **Yes**. 

<Image alt="Confirming shipment cancellation" align="center" width="350px" border={true} src="https://files.readme.io/add229243a38970d994d96735c0f6ad74a1ca4404fa57475b6c9fc2a85b038ad-Confirming_shipment_cancellation.png">
  Confirming shipment cancellation
</Image>

Once confirmed, the shipment(s) is removed from the current list and is displayed in the list of cancelled shipments. If needed, you can [recall the cancel shipments](https://docs.intersoftsapient.net/docs/recall-shipment) and work with them accordingly. 

> 💡 *Tip*
>
> *You can access the canceled shipments directly from this page by selecting the**View Cancelled Shipments** option or by accessing the **Shipment Processing** > **Cancelled** option from the side navigation panel.* 
>
> <Image alt="Accessing canceled shipments" align="center" border={true} src="https://files.readme.io/98bb78638eb05e979777dfd34b1a13605cab5520fa6017f7a980a02fc38a0602-Canceled_shipments_option.png">
>   Accessing cancelled shipments
> </Image>
