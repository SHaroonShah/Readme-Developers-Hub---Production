---
title: Add product
excerpt: >-
  Adding a product enables businesses to introduce new items into their shipping
  inventory. This process often involves providing essential details about the
  product, such as dimensions, weight, value, handling instructions, and any
  specific shipping requirements.
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
In SAPIENT, you can add as many products as you want and use them in your <Glossary>shipment</Glossary> request. This helps ensuring accurate data for pricing, labeling, and compliance.

To add a new <Glossary>product</Glossary> in SAPIENT, follow the steps as explained in the following procedure. 

1. In the left navigation panel, select **Products**. 

<Image alt="Accessing shipping locations" align="center" border={true} src="https://files.readme.io/ec355529da5603569fe7c27204b1b58b5f7368185e1daa06e9836a6a0c4e855b-Acccessing_products_option.png">
  Accessing products
</Image>

2. On the **Products** page that appears, select ![alt text](https://files.readme.io/551c1450e733a95bd452603ef5b85d1a7117a44a87b0689da3cd7b09b6351023-Add_product_button.png).

<Image alt="Selecting option to add shipping location" align="center" border={true} src="https://files.readme.io/dc08b7bdd1de178e0ec7835267721eea82af919b8f983ac89e33bcfdcb7ddef4-Add_product_option.png">
  Selecting option to add product
</Image>

3. On the **Add Product** form that opens, in the **PRODUCT DETAILS** block, enter the necessary information as explained in the following table.

<Image alt="Entering location details" align="center" border={true} src="https://files.readme.io/3a7afb46d19e9ed7a9c70e204c3a8abfbc168b76acc5bd3c6bad4737f9734ce9-Product_details_form.png">
  Entering product details
</Image>

<AsteridkForMandatoryElements />

<Table align={["center","left"]}>
  <thead>
    <tr>
      <th style={{ textAlign: "center" }}>
        Element
      </th>

      <th style={{ textAlign: "left" }}>
        Description
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td style={{ textAlign: "center" }}>
        **SKU Code\***
      </td>

      <td style={{ textAlign: "left" }}>
        Enter the <Glossary>stock keeping unit</Glossary> of the product you are adding.
      </td>
    </tr>

    <tr>
      <td style={{ textAlign: "center" }}>
        **HS Code**
      </td>

      <td style={{ textAlign: "left" }}>
        Enter the <Glossary>HS Code</Glossary> for the product you are adding.  

        *Note: A minimum of 6 alpha numeric code is required when the HS Code is provided (some services/destinations may require 8). Additionally, this information is required by some carriers for dutiable shipments.*
      </td>
    </tr>

    <tr>
      <td style={{ textAlign: "center" }}>
        **Description\***
      </td>

      <td style={{ textAlign: "left" }}>
        Enter a detailed description of the product you are adding.
      </td>
    </tr>

    <tr>
      <td style={{ textAlign: "center" }}>
        **Country of Origin**
      </td>

      <td style={{ textAlign: "left" }}>
        From the dropdown menu, select the country where the product you are adding was manufactured.  

        *Note: This information is required by some carriers for dutiable shipments.*
      </td>
    </tr>

    <tr>
      <td style={{ textAlign: "center" }}>
        **Value\***
      </td>

      <td style={{ textAlign: "left" }}>
        Enter the monetary value of the product you are adding.
      </td>
    </tr>

    <tr>
      <td style={{ textAlign: "center" }}>
        **Currency\***
      </td>

      <td style={{ textAlign: "left" }}>
        From the dropdown menu, select the currency code in which the value of the product is set.  

        *Note: This information is required if any monetary values other than zero are provided.*
      </td>
    </tr>

    <tr>
      <td style={{ textAlign: "center" }}>
        **Weight (kg)\***
      </td>

      <td style={{ textAlign: "left" }}>
        Enter the weight of the product you are adding. The unit of measure is set to **Kg** by default and can be a maximum of 1000 kg.  

        *Note: This information is required for dutiable shipments and must be a minimum of 1 g.*
      </td>
    </tr>

    <tr>
      <td style={{ textAlign: "center" }}>
        **Hazardous Product**
      </td>

      <td style={{ textAlign: "left" }}>
        This toggle is turned off by default. If the product you are adding is a hazardous material, then turn on this toggle and enter the necessary information as explained in step 4.
      </td>
    </tr>
  </tbody>
</Table>

4. If the product you are adding is a hazardous material, then turn on ![alt text](https://files.readme.io/efe8272f619daf8eb5e78d9b1c0e910a406242d6d5a9ced9a84d013216a8521c-Hazardous_product_toggle.png) toggle. In the **HAZARDOUS INFORMATION** form that opens, enter the necessary information as explained in the following table. 

<Image alt="Entering address details" align="center" border={true} src="https://files.readme.io/81567e5b0718c10f9e6955ed1b44915b5f824ddc836d0c1243b598f03225d20a-Hazardous_information_form.png">
  Entering hazardous product information
</Image>

<AsteridkForMandatoryElements />

<Table align={["center","left"]}>
  <thead>
    <tr>
      <th style={{ textAlign: "center" }}>
        Element
      </th>

      <th style={{ textAlign: "left" }}>
        Description
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td style={{ textAlign: "center" }}>
        **UN Code\***
      </td>

      <td style={{ textAlign: "left" }}>
        Enter the unique four digit number assigned by the United Nations to identify hazardous substances. It helps in recognising the hazardous product during shipping.
      </td>
    </tr>

    <tr>
      <td style={{ textAlign: "center" }}>
        **Proper Shipping Name**
      </td>

      <td style={{ textAlign: "left" }}>
        Enter the official name of the hazardous product as specified in the transport regulations, which clearly describes the substance and its potential hazards.
      </td>
    </tr>

    <tr>
      <td style={{ textAlign: "center" }}>
        **Quantity\***
      </td>

      <td style={{ textAlign: "left" }}>
        Enter total amount of the hazardous product being shipped.
      </td>
    </tr>

    <tr>
      <td style={{ textAlign: "center" }}>
        **Unit of Measure\***
      </td>

      <td style={{ textAlign: "left" }}>
        Enter the measurement unit (such as kilograms, litres, pounds, and so on) used to quantify the quantity of the hazardous product.
      </td>
    </tr>

    <tr>
      <td style={{ textAlign: "center" }}>
        **Class\***
      </td>

      <td style={{ textAlign: "left" }}>
        Enter the classification number that reflects the type of hazard posed by the product (for example, inflammable, toxic, corrosive) which is crucial for determining the appropriate handling and transportation measures. 
      </td>
    </tr>

    <tr>
      <td style={{ textAlign: "center" }}>
        **ID8000 Category**
      </td>

      <td style={{ textAlign: "left" }}>
        This field is only available if the class of the hazardous product is 9.  

        From the dropdown menu, select the category of the dangerous goods identified under ID8000 regulations.
      </td>
    </tr>

    <tr>
      <td style={{ textAlign: "center" }}>
        **Emergency Action Code**
      </td>

      <td style={{ textAlign: "left" }}>
        Enter the code that indicates necessary emergency response actions to take in the event of of an incident involving the hazardous product during transport.
      </td>
    </tr>

    <tr>
      <td style={{ textAlign: "center" }}>
        **Hazchem Number**
      </td>

      <td style={{ textAlign: "left" }}>
        Enter the number assigned to the hazardous material that indicates the specific firefighting and emergency response measures required, ensuring that responders have quick access to critical information.
      </td>
    </tr>

    <tr>
      <td style={{ textAlign: "center" }}>
        **Specialist Advice Contact Number**
      </td>

      <td style={{ textAlign: "left" }}>
        Enter the telephone number for reaching an expert or specialist who can provide guidance on handling the hazardous product in case of emergencies or specific inquiries regarding its transport.
      </td>
    </tr>
  </tbody>
</Table>

5. After entering all the relevant information, select ![alt text](https://files.readme.io/cbbd6f41c2af58489811253c7a470ba0541bace30346d7d0e2f0fd2c222348fa-Add_product_button_2.png).

Once done, a new product is added successfully and appears in the **Products** table. You can now manage it as per your business needs and use them in your shipment requests. 

> 📘 *Note*
>
> *Products can be added and managed via API. To learn more on how to add a product via API, refer to the[API References](https://docs.intersoftsapient.net/reference/post_v4-products) section.*
