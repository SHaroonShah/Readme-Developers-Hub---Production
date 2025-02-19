---
title: Delete shipping location
excerpt: >-
  Deleting a shipping location means removing it from the system completely when
  it is no longer required.
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
Deleting the <<glossary:shipping location>> could occur due to various reasons, such as: 

- **Closure**: if a shipping facility is closed or no longer in use, deleting it helps avoid confusion in future shipping operations.
- **Account changes**: When a business relocates or decides to consolidate shipping operations to fewer locations.

In SAPIENT, you can delete the shipping location to keep the shipping database clean and manageable, preventing clutter from inactive or obsolete entries. It also improves the system performance and avoids potential confusion by ensuring only current and relevant shipping locations are available for selection or operation.

To delete a shipping location, follow the steps as explained in the following procedure.

1. In the left navigation panel, select **Shipping Locations**. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/a84f50bafad4110e2244fa56d73b34787cf197d6a4e3de326ad287880d85e835-Shipping_locations_option.png",
        "",
        "Accessing shipping locations"
      ],
      "align": "center",
      "border": true,
      "caption": "Accessing shipping locations"
    }
  ]
}
[/block]


2. On the **Shipping Locations** page that appears, select the shipping location that you want to delete and on the **View Shipping Location [location name]** form that opens, select ![alt text](https://files.readme.io/545bdf744dcdbe039cd62675b409647c20469e8cede3709f2e1b7ebf2c65b675-Edit_shippig_location_button.png).

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/0ffbf35c04a6aa2b82329f91bca4df861fae2511cfbe07feeee4d9e97827d8c5-Edit_shippig_location_option.png",
        "",
        "Selecting option to add shipping location"
      ],
      "align": "center",
      "border": true,
      "caption": "Selecting option to delete shipping location"
    }
  ]
}
[/block]


3. On the **Edit Shipping Location [location name]** form that opens, on the right corner, select  ![alt text](https://files.readme.io/98795b945ef9e3b4440d5c52afd923cc5bf13990bd1125f578d131871f4bfc54-Delete_location_button.png).

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/bd3538aec38b70a7d69715426fca677ddc2922db2b942448fce828b6357e2cad-Deleting_shipping_location.png",
        "",
        "Entering location details"
      ],
      "align": "center",
      "border": true,
      "caption": "Deleting shipping location"
    }
  ]
}
[/block]


4. In the confirmation dialog that appears, select **Yes** to confirm your action.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/a6e38fbaadee4529ebe22646e35a12534d4a944a8bfb768a243d02380f082af2-Confirming_account_deletion.png",
        "",
        "Confirming deletion"
      ],
      "align": "center",
      "sizing": "350px",
      "border": true,
      "caption": "Confirming deletion"
    }
  ]
}
[/block]


Once done, the shipping location is deleted successfully. 

> 📘 _Note_
> 
> _Shipping locations can also be deleted via API. To learn more on how to delete your shipping locations via API, refer to the [API References](https://docs.intersoftsapient.net/reference/delete_v4-shippinglocations-shippinglocationid) section._

## See also

- [Add shipping location](https://docs.intersoftsapient.net/docs/add-a-shipping-location)