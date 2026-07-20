---
title: Hazmat label generation
excerpt: >-
  A _hazardous (hazmat) material_ is any substance that poses a risk to health,
  safety, or property due to its chemical nature. These materials can be solids,
  liquids, or gases and are categorised based on their specific physical and
  chemical characteristics that make them dangerous to human health or the
  environment. Proper handling, transportation, and disposal of hazardous
  materials are crucial in logistics to ensure safety and compliance with
  regulations.
deprecated: false
hidden: false
icon: fad fa-fire
metadata:
  robots: index
---
Expand the following sections to learn how to generate the Hazmat label for class 9 hazardous goods, as well as for other classes, including their approved UN codes.

<Accordion title="Generate hazmat (ID8000) label for Class 9 hazardous goods">
  *Class 9 hazardous goods* encompass a variety of materials that, while not covered by the other eight hazardous material classes, still pose risks in transport. This category includes items that may be subject to specific regulations but do not fit the criteria for flammable, explosive, or otherwise dangerous materials. Class 9 goods include substances that may be environmentally hazardous or have other regulatory considerations.

  In SAPIENT, you can specify the class 9 hazardous goods [via the UI](https://docs.intersoftsapient.net/docs/add-product#/) or in the [Create Shipment request](https://docs.intersoftsapient.net/reference/post_v4-shipments-rm#/).

  As part of the Royal Mail integration into the Sapient system, an *ID8000 label* is to be generated alongside the standard shipping label for Class 9 hazardous goods. This is done to ensure that customers have all necessary documentation for compliant shipping practices.

  The ID8000 label can only be printed under the following conditions:

  1. **Class determination**: The ID8000 label is exclusively generated for \**Class 9* shipments; no other classes apply.

  2. **ID8000Category field**: When creating the shipping request, the **Id8000Category** field in the API must be populated to match existing values.

  3. **PrintId8000Label field**: The Create Shipment API response will include the ID8000 label only if the **PrintId8000Label** field is populated with "yes."

  4. **Multiple items**: For shipments containing multiple Class 9 items, a single ID8000 label will be produced with all relevant categories checked on the label.

  5. **Item selection**: The items associated with the ID8000Category provided in the request will be pre-selected on the label. If the submitted category does not match an accepted value, the label will still be generated, but no item will be pre-checked, requiring manual entry by the customer. For instance, if a shipment contains both “Medicines” and “Nail Varnish,” both corresponding items will be marked on the label.

  6. **Label format**: Both the ID8000 label and the shipping label can only be generated as <Glossary>PDF</Glossary>s for hazmat shipments.

  > 🚧 *Important*
  >
  > *The ID8000 labels are valid only within the UK; hence, if a Class 9 shipment's destination is outside of UK, the ID8000 label will not be generated.*

  The following are the accepted Values for ID8000Category:

  * Medicine
  * Perfume/Aftershave
  * Nail Varnish
  * Toiletry or Medicinal Aerosols

  <Image align="center" src="https://files.readme.io/aa4ac259770b0d327a8cd43d0e47c31f8af7b5b1b10cb41fd7c141830787b4e7-Hazmat_label_example_1.png" width="300px" caption="ID8000 label example" />

  <br />
</Accordion>

<Accordion title="Generate hazardous LQDG label">
  Limited Quantities Dangerous Goods (LQDG) are items that, althought classifies as dangerous under transport regulations, such as flammable liquids, aerosols, and so on, can be trasnsported with flexible packaging and label requirements when shipped in small quantities.

  Shipments with such items must display a LQDG, often a DO NOT FLY banner on the label to indicate limitattions on air transport.

  To use the Royal Mail LQDG template with the **DO NOT FLY** banner, you must adhere to the following:

  * The hazmat element must be provided in the API request
  * LQD in your OBA contracts must be specified
  * The service used in the shipment request must be allowed to create hazardous shipment.
  * The PC District and PC Sector of the destination postcode must support hazardous shipment.
  * The total shipment weight must not exceed the LQDG Max Weight limit.
  * The UN codes must match the list of approved UN codes - [Approved UN codes](https://view.officeapps.live.com/op/view.aspx?src=https%3A%2F%2Fkb.intersoft.co.uk%2Fhubfs%2FUn%2520Numbers%2520that%2520can%2520be%2520utilised%2520in%2520Sapient.xlsx%3FhsLang%3Den\&wdOrigin=BROWSELINK)

  For more information on the supported hazmat classes, refer to the following table:

  | Class | Type of material                                                                                                                                   |
  | :---- | :------------------------------------------------------------------------------------------------------------------------------------------------- |
  | 1     | Explosive substances and articles                                                                                                                  |
  | 2.1   | Flammable gas (for example butane)                                                                                                                 |
  | 2.2   | Non-flammable and non-toxic gases which could cause asphyxiation, for example, nitrogen, helium, carbon dioxide) or oxidisers, for example, oxygen |
  | 2.3   | Toxic gases, for example, chlorine, phosgene, and so on                                                                                            |
  | 3     | Flammable liquids, for example, lighter fluid, petrol, and others                                                                                  |
  | 4.1   | Flammable solids, self-reactive substances and solid desensitised explosives                                                                       |
  | 4.2   | Substances liable to spontaneous combustion                                                                                                        |
  | 4.3   | Substances which, in contact with water, emit flammable gases                                                                                      |
  | 5.1   | Oxidising substances                                                                                                                               |
  | 5.2   | Organic peroxides                                                                                                                                  |
  | 6.1   | Toxic substances                                                                                                                                   |
  | 6.2   | Infectious substances                                                                                                                              |
  | 7     | Radioactive material                                                                                                                               |
  | 8     | Corrosive substances                                                                                                                               |
  | 9     | Miscellaneous dangerous substances and articles                                                                                                    |

  <br />

  > 🚧 *Important*
  >
  > *For any queries on the prerequisites for hazmat label generation, please contact your Royal Mail account manager*.
</Accordion>

<br />
