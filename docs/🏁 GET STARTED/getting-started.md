---
title: Welcome to SAPIENT Developers Hub
excerpt: >-
  Welcome to Intersoft SAPIENT, a scalable carrier management platform designed
  to facilitate seamless integration with various shipping carriers, third-party
  logistics provider, and other eCommerce platforms. By leveraging APIs, SAPIENT
  enhances its adaptability and user friendliness, providing a simple, reliant
  shipping API to easily create and manage shipments, generate labels, and more.
deprecated: false
hidden: false
icon: fad fa-diagram-lean-canvas
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
  pages:
    - type: basic
      slug: integration-activation
      title: Integration Activation
---
# Introduction

APIs play a crucial role in the SAPIENT system by facilitating seamless integration with various shipping carriers, third party logistics providers, and other eCommerce platforms. This connectivity allows businesses to automate data exchange, streamline workflows, and ensure real-time updates on shipping performance.

<Image align="center" border={true} src="https://files.readme.io/82fb0cbe41a890f07d419cd0f39a19ec47336cd51e97fe6969efdb6b26a4d82d-Sapient.png" className="border" />

If you are looking to build an integration, then our API solution will help you incorporate the intelligence of Intersoft SAPIENT into your software with minimal integration effort.

The Intersoft SAPIENT Developers Hub provides both new and current users with a step-by-step guide on how to set up a <Glossary>shipping account</Glossary> , <Glossary>shipments</Glossary> , and get started as a new user. Furthermore, this section covers the vital processes on how the business clients can utilise the API to carry out shipping activities with available carriers, as well as the technical details required to build this integration.

## Getting started

This section outlines the essential information on our APIs and steps to begin utilising the SAPIENT APIs, including setup instructions, authentication processes, and key functionalities that can be accessed through the API and SAPIENT's UI. Whether you are a developer or a business user, this section offers the necessary resources to seamlessly connect and optimise your processes within the SAPIENT platform.

**Intersoft SAPIENT API** enables you to create and manage shipments, produce labels and customs documentation, generate and print collection manifests. The API also allows you to retrieve reference data such as carriers supported by the platform and the countries where shipments can be sent, maintain your own data required for these, such as adding and managing shipping accounts and <Glossary>shipping location</Glossary> details.

**Intersoft API**is a fully RESTful service implemented using JSON messaging. You, as the customer, are responsible for sending JSON messages and for maintaining the capability of receiving JSON messages in the format described in this documentation.

<Image align="center" border={false} width="500px" src="https://files.readme.io/c388f57ddfed471dccc9c49befdedf8da79a14260f9ffbbc5e7f5996226f2022-Intersoft_api_art.png" />

### Seamless integration awaits: Get started with SAPIENT

Get ready to integrate our powerful API into your existing systems. Whether you are looking to streamline shipping management, monitor performance metrics, or customise your logistics workflows, our APIs provide the flexibility and scalability you need to succeed.

Let us dive in and explore how to get started on SAPIENT

* [ ] [Create API credentials](https://docs.intersoftsapient.net/docs/create-api-credentials)
* [ ] [Activate integration](doc:integration-activation)
* [ ] [Add users](doc:add-users-to-your-organisation-to-begin-collaborating-with-your-team)
* [ ] [Add shipping location(s)](https://docs.intersoftsapient.net/docs/add-a-shipping-location)
* [ ] [Add shipping account(s)](https://docs.intersoftsapient.net/docs/add-a-shipping-account)

> 🚧 _Important_
>
> _The API requires the user to provide a[Bearer token](https://docs.intersoftsapient.net/docs/bearer-token-generation-1). To learn more about the bearer token and its generation, refer to the [Authentication](https://docs.intersoftsapient.net/docs/authentication) section._

***

## Further reading

This section provides you with the complimentary information that you might find useful for further insights into the SAPIENT system.

* [User guides](https://docs.intersoftsapient.net/docs/maintenance-guides)
* [Shipment creation and manifesting](https://docs.intersoftsapient.net/docs/shipment-creation-and-manifesting)
* [Additional services](https://docs.intersoftsapient.net/docs/additional-services-user-guides)
* [Carrier specific guides](https://docs.intersoftsapient.net/docs/carrier-specific-user-guides)
* [Glossary](https://docs.intersoftsapient.net/docs/glossary-1)
* [Archived release notes](https://docs.intersoftsapient.net/docs/archived-release-notes)

<br />

| MDF Validations |                                                                                                                                |                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| :-------------- | :----------------------------------------------------------------------------------------------------------------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Rule            | Scenario Description                                                                                                           | Mandatory Fields                                                                                                                                                                                                                                                                                                                                                                                                                       |
| ------          | ---------------------                                                                                                          | -------------------------------------------------------------------------------------------                                                                                                                                                                                                                                                                                                                                            |
| **A**           | All domestic shipments (within the same country) and international document shipments (letters, paperwork)                     | Sender Name, Sender Address 1, Sender Town, Sender Postcode, Sender Country, Destination Name, Destination Address 1, Destination Town, Destination Country                                                                                                                                                                                                                                                                            |
| **B**           | International non-document shipments (goods) using DDU (buyer pays duties/taxes)                                               | Sender Name, Sender Address 1, Sender Town, Sender Postcode, Sender Country, Destination Name, Destination Address 1, Destination Town, Destination Country, Item Quantity, Item Description, Item Value, Item Weight                                                                                                                                                                                                                  |
| **C**           | International non-document shipments (goods) using DDU, with extra customs data                                                | Sender Name, Sender Address 1, Sender Town, Sender Postcode, Sender Country, Destination Name, Destination Address 1, Destination Town, Destination Country, Item Quantity, Item Description, Item Value, Item Weight, Item HS Code, Item Country of Origin                                                                                                                                                                            |
| **D**           | International non-document shipments (goods) using DDU, with extra customs data and mandatory recipient contact details        | Sender Name, Sender Address 1, Sender Town, Sender Postcode, Sender Country, Destination Name, Destination Address 1, Destination Town, Destination Country, Item Quantity, Item Description, Item Value, Item Weight, Item HS Code, Item Country of Origin, Recipient Contact Phone Number, Recipient Email                                                                                                                           |
| **E**           | International non-document shipments (goods) using DDP (seller pays duties/taxes), sent to non-EU destinations (Rest of World) | Sender Name, Sender Address 1, Sender Town, Sender Postcode, Sender Country, Destination Name, Destination Address 1, Destination Town, Destination Country, Item Quantity, Item Description, Item Value, Item Weight, Item HS Code, Item Country of Origin, Recipient Contact Phone Number, Recipient Email, Customs Quoted Landed Cost                                                                                               |
| **F**           | International non-document shipments (goods) using DDP, sent to EU destinations                                                | Sender Name, Sender Address 1, Sender Town, Sender Postcode, Sender Country, Destination Name, Destination Address 1, Destination Town, Destination Country, Item Quantity, Item Description, Item Value, Item Weight, Item HS Code, Item Country of Origin, Recipient Contact Phone Number, Recipient Email, Customs Quoted Landed Cost, Shipper EORI Number                                                                          |
| **G**           | International non-document shipments (goods) with IOSS registration (EU VAT scheme for e-commerce)                             | Sender Name, Sender Address 1, Sender Town, Sender Postcode, Sender Country, Destination Name, Destination Address 1, Destination Town, Destination Country, Item Quantity, Item Description, Item Value, Item Weight, Item HS Code, Item Country of Origin, Recipient Contact Phone Number, Recipient Email, IOSS Preregistration Type, IOSS Preregistration Number                                                                   |
| **H**           | International non-document shipments (goods) with other preregistration schemes (PRS)                                          | Sender Name, Sender Address 1, Sender Town, Sender Postcode, Sender Country, Destination Name, Destination Address 1, Destination Town, Destination Country, Item Quantity, Item Description, Item Value, Item Weight, Item HS Code, Item Country of Origin, Recipient Contact Phone Number, Recipient Email, Non-IOSS Preregistration Type, Non-IOSS Preregistration Number                                                           |
| **K**           | Business-to-business (B2B) shipments                                                                                           | Sender Name, Sender Address 1, Sender Town, Sender Postcode, Sender Country, Destination Name, Destination Address 1, Destination Town, Destination Country, Item Quantity, Item Description, Item Value, Item Weight, Item HS Code, Item Country of Origin, Recipient EORI Number, Shipper EORI Number                                                                                                                                |
| **L**           | International non-document shipments (goods) using DDP, with importer details required                                         | Sender Name, Sender Address 1, Sender Town, Sender Postcode, Sender Country, Destination Name, Destination Address 1, Destination Town, Destination Country, Shipper EORI Number, Recipient Email, Recipient Contact Phone Number, Item Quantity, Item Description, Item Value, Item Weight, Item HS Code, Item Country of Origin, Customs Quoted Landed Cost, Importer Name, Importer Address 1, Importer Country Code, Importer Town |

<HTMLBlock>{`
 <table>
   <thead>
     <tr>
       <th> Mandatory Fields </th>
     </tr>
   </thead>
   <tbody>
     <tr>
       <td colspan="1"> <b>Address</b> </td>
     </tr>
     <tr>
       <td colspan="1">Town</td>
     </tr>
     <tr>
       <td colspan="1">PostCode</td>
     </tr>
     <tr>
       <td> County </td>
       
     </tr>
     <tr>
       <td colspan="2"> <b>Packages</b> </td>
     <tr>
       <td> Town </td>
     
     </tr>     <tr>
       <td> City </td>
    
</tr>

   </tbody>
</table>
`}</HTMLBlock>

<Accordion title="Rule A" icon="fa-info-circle">
  <HTMLBlock>{`
           <table>
             <thead>
               <tr>
                 <th> API Object </th>
                 <th> API Field Name </th>
               </tr>
             </thead>
             <tbody>
               <tr>
                 <td colspan="2"> <b>Sender > Address</b> </td>
               </tr>
               <tr>
                 <td colspan="2">Town</td>
               </tr>
               <tr>
                 <td colspan="2">PostCode</td>
               </tr>
               <tr>
                 <td> County </td>
                 <td> Surrey </td>
               </tr>
               <tr>
                 <td colspan="2"> <b>Packages</b> </td>
               <tr>
                 <td> Town </td>
                 <td> ABB </td>
               </tr>     <tr>
                 <td> City </td>
                 <td> Aberdeen </td>
          </tr>

             </tbody>
          </table>
  `}</HTMLBlock>
</Accordion>
