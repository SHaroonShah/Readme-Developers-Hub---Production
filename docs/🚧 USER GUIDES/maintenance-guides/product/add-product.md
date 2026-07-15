---
title: Add product
excerpt: >-
  Adding a product enables businesses to introduce new items into their shipping
  inventory. This process often involves providing essential details about the
  product, such as dimensions, weight, value, handling instructions, and any
  specific shipping requirements.
deprecated: false
hidden: false
icon: fad fa-square-plus
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
In SAPIENT, you can add as many products as you want and use them in your <Glossary>shipment</Glossary> request. This helps ensuring accurate data for pricing, labeling, and compliance.

<Cards columns={2}>
  <Card title="Regular Products" icon="fa-solid fa-box">
    Standard items with basic product information like dimensions, weight, and value.
  </Card>

  <Card title="Hazardous Materials" icon="fa-solid fa-radiation">
    Special products requiring additional safety information and compliance details.
  </Card>
</Cards>

## How to add product

<Tabs>
  <Tab title="Add via SAPIENT UI">
    

    To add a product in SAPIENT, perform the steps as explained in the following procedure.

    <ToggleList>
      <ToggleListItem title={<strong>1. Access the products page</strong>} icon="fa-rocket">
        <br />

        In the left navigation panel, select **Products**.

        <Image align="center" border={true} src="https://files.readme.io/ec355529da5603569fe7c27204b1b58b5f7368185e1daa06e9836a6a0c4e855b-Acccessing_products_option.png" alt="Accessing shipping locations" />

        ***
      </ToggleListItem>

      <br />

      <ToggleListItem title={<strong>2. Select option to add product</strong>} icon="fa-rocket">
        <br />

        On the **Products** page that appears, select ![alt text](https://files.readme.io/551c1450e733a95bd452603ef5b85d1a7117a44a87b0689da3cd7b09b6351023-Add_product_button.png).

        <Image align="center" border={true} src="https://files.readme.io/da5be64375756a300994c03536bf33b18d2b0cc962e5e7089d0342f299816021-image.png" alt="Selecting option to add shipping location" />

        ***
      </ToggleListItem>

      <br />

      <ToggleListItem title={<strong>3. Enter product details </strong>} icon="fa-rocket">
        <br />

        On the **Add Product** form that opens, in the **PRODUCT DETAILS** block, enter the necessary information as explained in the following table.

        <Tabs>
          <Tab title="Basic product details">
            On the **Add Product** form that opens, in the **PRODUCT DETAILS** block, enter the necessary information.

            <Image align="center" border={true} src="https://files.readme.io/bb154e33c4ce1aac13fcc54301465da2cec7a83940ffbfd1379c2aac3101d9e5-image.png" alt="Entering location details" />

            <br />

            <AsteridkForMandatoryElements />

            <table>
              <thead>
                <tr>
                  <th align="center">Element</th>
                  <th align="left">Description</th>
                </tr>
              </thead>
              <tbody>
                <tr>
                  <td align="center"><strong>SKU Code</strong>&#42;</td>
                  <td align="left">Enter the stock keeping unit of the product you are adding.</td>
                </tr>
                <tr>
                  <td align="center"><strong>HS Code</strong></td>
                  <td align="left">Enter the HS Code for the product you are adding.<br /><br /><em><code>Note</code></em>: A minimum of 6 alpha-numeric code is required when the HS Code is provided (some services/destinations may require 8). Additionally, this information is required by some carriers for dutiable shipments.</td>
                </tr>
                <tr>
                  <td align="center"><strong>Description</strong>&#42;</td>
                  <td align="left">Enter a detailed description of the product you are adding.</td>
                </tr>
                <tr>
                  <td align="center"><strong>Country of Origin</strong></td>
                  <td align="left">From the dropdown menu, select the country where the product you are adding was manufactured.<br /><br /><em><code>Note</code></em>: This information is required by some carriers for dutiable shipments.</td>
                </tr>
                <tr>
                  <td align="center"><strong>Manufacture Product Id</strong></td>
                  <td align="left">Enter the unique identifier used to reference the product you are adding.</td>
                </tr>
                <tr>
                  <td align="center"><strong>Value</strong>&#42;</td>
                  <td align="left">Enter the monetary value of the product you are adding.</td>
                </tr>
                <tr>
                  <td align="center"><strong>Currency</strong>&#42;</td>
                  <td align="left">From the dropdown menu, select the currency code in which the value of the product is set.<br /><br /><em><code>Note</code></em>: This information is required if any monetary values other than zero are provided.</td>
                </tr>
                <tr>
                  <td align="center"><strong>Weight (kg)</strong>&#42;</td>
                  <td align="left">Enter the weight of the product you are adding. The unit of measure is set to <strong>Kg</strong> by default and can be a maximum of 1000 kg.<br /><br /><em><code>Note</code></em>: This information is required for dutiable shipments and must be a minimum of 1 g.</td>
                </tr>
                <tr>
                  <td align="center"><strong>Category</strong>&#42;</td>
                  <td align="left">Enter the category of the product you are adding.</td>
                </tr>
                <tr>
                  <td align="center"><strong>Standardised Product Id</strong></td>
                  <td align="left">Enter the product identifier used for standardised item identification and to support your carrier-specific requirements for customs and risk assessment.</td>
                </tr>
                <tr>
                  <td align="center"><strong>Hazardous Product</strong></td>
                  <td align="left">This toggle is turned off by default. If the product you are adding is a hazardous material, then turn on this toggle and enter the necessary information as explained in the Hazardous product details tab.</td>
                </tr>
                <tr>
                  <td align="center"><strong>This product cannot be returned</strong></td>
                  <td align="left">This toggle is turned off by default. Turn on the toggle if the product you are adding is non-returnable.</td>
                </tr>
              </tbody>
            </table>
          </Tab>

          <Tab title="Hazardous product details">
            If the product you are adding is a hazardous material, then turn on ![alt text](https://files.readme.io/efe8272f619daf8eb5e78d9b1c0e910a406242d6d5a9ced9a84d013216a8521c-Hazardous_product_toggle.png) toggle and enter the necessary information as explained in the following table.

            <Image align="center" border={true} src="https://files.readme.io/81567e5b0718c10f9e6955ed1b44915b5f824ddc836d0c1243b598f03225d20a-Hazardous_information_form.png" alt="Entering address details" />

            <br />

            <AsteridkForMandatoryElements />

            <table>
              <thead>
                <tr>
                  <th align="center">Element</th>
                  <th align="left">Description</th>
                </tr>
              </thead>
              <tbody>
                <tr>
                  <td align="center"><strong>UN Code</strong>&#42;</td>
                  <td align="left">Enter the unique four digit number assigned by the United Nations to identify hazardous substances. It helps in recognising the hazardous product during shipping.</td>
                </tr>
                <tr>
                  <td align="center"><strong>Proper Shipping Name</strong></td>
                  <td align="left">Enter the official name of the hazardous product as specified in the transport regulations, which clearly describes the substance and its potential hazards.</td>
                </tr>
                <tr>
                  <td align="center"><strong>Quantity</strong>&#42;</td>
                  <td align="left">Enter total amount of the hazardous product being shipped.</td>
                </tr>
                <tr>
                  <td align="center"><strong>Unit of Measure</strong>&#42;</td>
                  <td align="left">Enter the measurement unit (such as kilograms, litres, pounds, and so on) used to quantify the quantity of the hazardous product.</td>
                </tr>
                <tr>
                  <td align="center"><strong>Class</strong>&#42;</td>
                  <td align="left">Enter the classification number that reflects the type of hazard posed by the product (for example, inflammable, toxic, corrosive) which is crucial for determining the appropriate handling and transportation measures.</td>
                </tr>
                <tr>
                  <td align="center"><strong>ID8000 Category</strong></td>
                  <td align="left">This field is only available if the class of the hazardous product is 9.<br /><br />From the dropdown menu, select the category of the dangerous goods identified under ID8000 regulations.</td>
                </tr>
                <tr>
                  <td align="center"><strong>Emergency Action Code</strong></td>
                  <td align="left">Enter the code that indicates necessary emergency response actions to take in the event of of an incident involving the hazardous product during transport.</td>
                </tr>
                <tr>
                  <td align="center"><strong>Hazchem Number</strong></td>
                  <td align="left">Enter the number assigned to the hazardous material that indicates the specific firefighting and emergency response measures required, ensuring that responders have quick access to critical information.</td>
                </tr>
                <tr>
                  <td align="center"><strong>Specialist Advice Contact Number</strong></td>
                  <td align="left">Enter the telephone number for reaching an expert or specialist who can provide guidance on handling the hazardous product in case of emergencies or specific inquiries regarding its transport.</td>
                </tr>
              </tbody>
            </table>
          </Tab>
        </Tabs>

        ***
      </ToggleListItem>

      <br />

      <ToggleListItem title={<strong>4. Add product </strong>} icon="fa-rocket">
        <br />

        After entering all the relevant information, select ![](https://files.readme.io/cbbd6f41c2af58489811253c7a470ba0541bace30346d7d0e2f0fd2c222348fa-Add_product_button_2.png).

        Once done, a new product is added successfully and appears in the **Products** table. You can now manage it as per your business needs and use them in your shipment requests.
      </ToggleListItem>
    </ToggleList>
  </Tab>

  <Tab title="Add via API">
    

    To add a product via our API, refer to the following endpoint:

    <Cards>
      <Card title="Add Product" href="https://docs.intersoftsapient.net/v4.02_Coding/reference/post_v4-products#/" icon="fa-solid fa-code">
        Complete API reference for adding products
      </Card>
    </Cards>
  </Tab>
</Tabs>

***

### See also

<Cards columns={2}>
  <Card title="Edit Product" href="https://docs.intersoftsapient.net/docs/edit-product" icon="fa-solid fa-edit">
    Modify existing product information, update specifications, or change handling instructions.
  </Card>

  <Card title="Delete Product" href="https://docs.intersoftsapient.net/docs/delete-product" icon="fa-solid fa-trash-alt">
    Remove products from your system that are no longer needed.
  </Card>
</Cards>


