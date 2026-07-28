---
title: Edit product
excerpt: >-
  Editing a product is necessary for updating existing product information to
  reflect changes such as new dimensions, weights, pricing, or handling
  instructions.
deprecated: false
hidden: false
icon: fad fa-pen-circle
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
In SAPIENT, you can edit the <Glossary>product</Glossary>, ensuring that any changes in product specifications are accurately communicated throughout the shipping and logistics processes. This process eventually reduces the risk of shipping errors, delays, or issues related to regulatory compliance.

## How to edit product

<Tabs>
  <Tab title="Edit via SAPIENT UI">
   

    To edit a product in SAPIENT, perform the steps as explained in the following procedure.

    <ToggleList>
      <ToggleListItem title={<strong>1. Access the products page</strong>} icon="fa-rocket">
        <br />

        In the left navigation panel, select **Products**.

        <Image align="center" border={true} src="https://files.readme.io/ec355529da5603569fe7c27204b1b58b5f7368185e1daa06e9836a6a0c4e855b-Acccessing_products_option.png" alt="Accessing shipping locations" />

        ***
      </ToggleListItem>

      <br />

      <ToggleListItem title={<strong>2. Select product to edit</strong>} icon="fa-rocket">
        <br />

        On the **Products** page that appears, from the list, select the product that you want to edit.

        <Image align="center" border={true} src="https://files.readme.io/a1a7bc27c6253ce0355cb87cc2f549c247ac33518acf56a929598df85fda5882-Selecting_products_to_edit.png" />

        ***
      </ToggleListItem>

      <br />

      <ToggleListItem title={<strong>3. Edit product</strong>} icon="fa-rocket">
        <br />

        In the **Edit Product** form that opens, start updating the necessary information as explained in the [Add product](https://docs.intersoftsapient.net/docs/add-product) section.

        <Image src="https://files.readme.io/d760e18eaeb4a1335ff421ba262ab5c700e7b3330a47ce768e89a31b726bbb61-Editing_product.png" align="center" caption="Editing product details" border={true} />

        ***
      </ToggleListItem>

      <br />

      <ToggleListItem title={<strong>4. Save changes </strong>} icon="fa-rocket">
        <br />

        After entering all the relevant information, select ![](https://files.readme.io/44d2859089ab3d4ffcb5341e904f29d383f25f9fa79e210a09482d2a26998248-Save_changes_button.png).

        Once done, the product is updated successfully. You can now manage it as per your business needs and use them in your <Glossary>shipment</Glossary> requests.

        ***
      </ToggleListItem>
    </ToggleList>
  </Tab>

  <Tab title="Edit via API">
    

    To edit a product via our API, refer to the following endpoint:

    <Cards>
      <Card title="Update Product" href="https://docs.intersoftsapient.net/v4.02_Coding/reference/put_v4-products-skucode#/" icon="fa-solid fa-code">
        Complete API reference for editing products
      </Card>
    </Cards>
  </Tab>
</Tabs>

***

### See also

<Cards columns={2}>
  <Card title="Add Product" href="https://docs.intersoftsapient.net/docs/add-product" icon="fa-solid fa-plus-circle">
    Create new product entries in your system with all necessary details and shipping requirements.
  </Card>

  <Card title="Delete Product" href="https://docs.intersoftsapient.net/docs/delete-product" icon="fa-solid fa-trash-alt">
    Remove products from your system that are no longer needed.
  </Card>
</Cards>