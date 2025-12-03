---
title: Delete product
excerpt: >-
  Deleting a product involves removing items from the shipping inventory that
  are no longer being offered or that are discontinued. This helps streamline
  inventory management
deprecated: false
hidden: false
icon: fad fa-circle-trash
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
In SAPIENT, you can delete a product to cleanup the database, preventing confusion with outdated products. This process potentially improves system performance, as fewer entries can lead to faster processing and operations.

## How to delete product

<Tabs>
  <Tab title="Delete via SAPIENT UI">
    <br />

    To delete a product in SAPIENT, perform the steps as explained in the following procedure.

    <ToggleList>
      <ToggleListItem title={<strong>1. Access the products page</strong>} icon="fa-rocket">
        <br />

        In the left navigation panel, select **Products**.

        <Image align="center" border={true} src="https://files.readme.io/ec355529da5603569fe7c27204b1b58b5f7368185e1daa06e9836a6a0c4e855b-Acccessing_products_option.png" alt="Accessing shipping locations" />

        ***
      </ToggleListItem>

      <br />

      <ToggleListItem title={<strong>2. Select product to delete</strong>} icon="fa-rocket">
        <br />

        On the **Products** page that appears, from the list, select the product that you want to delete.

        <Image align="center" border={true} src="https://files.readme.io/a1a7bc27c6253ce0355cb87cc2f549c247ac33518acf56a929598df85fda5882-Selecting_products_to_edit.png" />

        ***
      </ToggleListItem>

      <br />

      <ToggleListItem title={<strong>3. Delete product</strong>} icon="fa-rocket">
        <br />

        In the **Edit Product** form that opens, start updating the necessary information as explained in the [Add product](https://docs.intersoftsapient.net/docs/aclick ![](https://files.readme.io/63292b906edfcaf8554e4c4b9385b1ba483ec4ada1541955dde6ff5a78cc55fe-Delete_product_button.png).

        <Image align="center" alt="Selecting option to add shipping location" border={true} caption="Deleting product" src="https://files.readme.io/c84f99786468144347b5039b2c1bde7322000a27e08f78cb070a4fbd17dbd9f0-Delete_product_option.png" />

        ***
      </ToggleListItem>

      <br />

      <ToggleListItem title={<strong>4. Confirm deletion </strong>} icon="fa-rocket">
        <br />

        In the confirmation dialog that appears, select **Yes** to confirm your action.

<Image align="center" alt="Confirming product deletion" border={true} caption="Confirming product deletion" src="https://files.readme.io/2c4dc02c1409b059556e92db227a058f328c7cfb5de80c36e95021287647f311-Confirming_product_deletion.png" width="350px" />

Once confirmed, the product is deleted successfully and no longer displays in the **Product** list.

        ***
      </ToggleListItem>
    </ToggleList>
  </Tab>

  <Tab title="Delete via API">
    <br />

    To delete a product via our API, refer to the following endpoint:

    <Cards>
      <Card title="Delete Product" href="https://docs.intersoftsapient.net/v4.02_Coding/reference/delete_v4-products-skucode#/" icon="fa-solid fa-code">
        Complete API reference for deleting products
      </Card>
    </Cards>
  </Tab>
</Tabs>

***

### See also

<br />
