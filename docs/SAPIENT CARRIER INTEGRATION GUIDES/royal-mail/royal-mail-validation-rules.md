---
title: Royal Mail validation rules
excerpt: >-
  To support seamless parcel shipping and delivery, Royal Mail has implemented a
  set of validation rules that ensure all required data is accurately provided
  to the carrier.
deprecated: false
hidden: false
icon: far fa-shield-check
link:
  new_tab: false
metadata:
  robots: index
---
These validation rules are defined in the Royal Mail _Master Data File (MDF)_, which lists all the available services , destination coverage, and mandatory data fields for each destination. Required fields include—but are not limited to shipment content, business transaction type, and item information.

When creating a shipment, these validation rules verify that all necessary information is present and correctly formatted for each shipping scenario, reducing errors and streamlining the delivery process.

## Scope of validations

The following sections summarises the MDF validation rules, their respective shipment scenarios, and the mandatory fields for each rule. The field are mapped to their typical names for clarity and reference.

> 🚧 _Important_
>
> _The Royal Mail validation rules may change overtime. For the most accurate and up-to-date validation rules, please contact your Royal Mail account manager._

<Accordion title="Ruleset A" icon="fa-solid fa-shield-check">

**Scenario example**: Domestic <Glossary>DOX</Glossary>, <Glossary>NDX</Glossary>, and international DOX shipments.

  
| API object | Mandatory fields |
| --- | --- |
| Shipper > Address | ContactName |
| Shipper > Address | Line 1 |
| Shipper > Address | Town |
| Shipper > Address | Postcode |
| Shipper > Address | CountryCode |
| Destination > Address | ContactName |
| Destination > Address | Line 1 |
| Destination > Address | Town |
| Destination > Address | CountryCode |

</Accordion>

<Accordion title="Ruleset B" icon="fa-solid fa-shield-check">

**Scenario example**: International non-document (<Glossary>NDX</Glossary>) shipments using <Glossary>DDU</Glossary> incoterm.

  
| API object | Mandatory fields |
| --- | --- |
| Shipper > Address | ContactName |
| Shipper > Address | Line 1 |
| Shipper > Address | Town |
| Shipper > Address | PostCode |
| Shipper > Address | CountryCode |
| Destination > Address | ContactName |
| Destination > Address | Line 1 |
| Destination > Address | Town |
| Destination > Address | CountryCode |
| Items | Quantity |
| Items | Description |
| Items | Value |
| Items | Weight |

</Accordion>

<Accordion title="Ruleset C" icon="fa-solid fa-shield-check">

**Scenario example**: International non-document (<Glossary>NDX</Glossary>) shipments using <Glossary>DDU</Glossary> incoterm, with additional item information.

  
| API object | Mandatory fields |
| --- | --- |
| Shipper > Address | ContactName |
| Shipper > Address | Line 1 |
| Shipper > Address | Town |
| Shipper > Address | PostCode |
| Shipper > Address | CountryCode |
| Destination > Address | ContactName |
| Destination > Address | Line 1 |
| Destination > Address | Town |
| Destination > Address | CountryCode |
| Items | Quantity |
| Items | Description |
| Items | Value |
| Items | Weight |
| Items | HSCode |
| Items | CountryOfOrigin |

</Accordion>

<Accordion title="Ruleset D" icon="fa-solid fa-shield-check">

**Scenario example**: International non-document (<Glossary>NDX</Glossary>) shipments using <Glossary>DDU</Glossary>, with extra customs data and mandatory receiver contact details.

  
| API object | Mandatory fields |
| --- | --- |
| Shipper > Address | ContactName |
| Shipper > Address | Line 1 |
| Shipper > Address | Town |
| Shipper > Address | PostCode |
| Shipper > Address | CountryCode |
| Destination > Address | ContactName |
| Destination > Address | Line 1 |
| Destination > Address | Town |
| Destination > Address | CountryCode |
| Destination > Address | ContactEmail |
| Destination > Address | ContactPhone |
| Items | Quantity |
| Items | Description |
| Items | Value |
| Items | Weight |
| Items | HSCode |
| Items | CountryOfOrigin |

</Accordion>

<Accordion title="Ruleset E" icon="fa-solid fa-shield-check">

**Scenario example**: International non-document (<Glossary>NDX</Glossary>) shipments using <Glossary>DDP</Glossary> incoterm, sent to non-EU destinations, that is Rest of the World (<Glossary>ROW</Glossary>).

  
| API object | Mandatory fields |
| --- | --- |
| Shipper > Address | ContactName |
| Shipper > Address | Line 1 |
| Shipper > Address | Town |
| Shipper > Address | PostCode |
| Shipper > Address | CountryCode |
| Destination > Address | ContactName |
| Destination > Address | Line 1 |
| Destination > Address | Town |
| Destination > Address | CountryCode |
| Destination > Address | ContactEmail |
| Destination > Address | ContactPhone |
| Items | Quantity |
| Items | Description |
| Items | Value |
| Items | Weight |
| Items | HSCode |
| Items | CountryOfOrigin |
| Customs | QuotedLandedCost |

</Accordion>

<Accordion title="Ruleset F" icon="fa-solid fa-shield-check">

**Scenario example**: International non-document (<Glossary>NDX</Glossary>) shipments using <Glossary>DDP</Glossary> incoterm, sent to EU destinations.

  
| API object | Mandatory fields |
| --- | --- |
| Shipper > Address | ContactName |
| Shipper > Address | Line 1 |
| Shipper > Address | Town |
| Shipper > Address | PostCode |
| Shipper > Address | CountryCode |
| Shipper | EoriNumber |
| Destination > Address | ContactName |
| Destination > Address | Line 1 |
| Destination > Address | Town |
| Destination > Address | CountryCode |
| Destination > Address | ContactEmail |
| Destination > Address | ContactPhone |
| Items | Quantity |
| Items | Description |
| Items | Value |
| Items | Weight |
| Items | HSCode |
| Items | CountryOfOrigin |
| Customs | QuotedLandedCost |

</Accordion>

<Accordion title="Ruleset G" icon="fa-solid fa-shield-check">

**Scenario example**: International non-document (<Glossary>NDX</Glossary>) shipments with an <Glossary>IOSS</Glossary> <Glossary>Pre-registration number</Glossary>, shipped to EU destinations.

  
| API object | Mandatory fields |
| --- | --- |
| Shipper > Address | ContactName |
| Shipper > Address | Line 1 |
| Shipper > Address | Town |
| Shipper > Address | PostCode |
| Shipper > Address | CountryCode |
| Destination > Address | ContactName |
| Destination > Address | Line 1 |
| Destination > Address | Town |
| Destination > Address | CountryCode |
| Destination > Address | ContactEmail |
| Destination > Address | ContactPhone |
| Items | Quantity |
| Items | Description |
| Items | Value |
| Items | Weight |
| Items | HSCode |
| Items | CountryOfOrigin |
| Customs | PreRegistrationNumber populated with the IOSS number |
| Customs | PreRegistrationType defined as IOSS |

</Accordion>

<Accordion title="Ruleset H" icon="fa-solid fa-shield-check">

**Scenario example**: International non-document (<Glossary>NDX</Glossary>) shipments with <Glossary>Pre-registration number</Glossary>.

  
| API object | Mandatory fields |
| --- | --- |
| Shipper > Address | ContactName |
| Shipper > Address | Line 1 |
| Shipper > Address | Town |
| Shipper > Address | PostCode |
| Shipper > Address | CountryCode |
| Destination > Address | ContactName |
| Destination > Address | Line 1 |
| Destination > Address | Town |
| Destination > Address | CountryCode |
| Destination > Address | ContactEmail |
| Destination > Address | ContactPhone |
| Items | Quantity |
| Items | Description |
| Items | Value |
| Items | Weight |
| Items | HSCode |
| Items | CountryOfOrigin |
| Customs | PreRegistrationNumber |
| Customs | PreRegistrationType |

</Accordion>

<Accordion title="Ruleset K" icon="fa-solid fa-shield-check">

**Scenario example**: Shipment with B2B <Glossary>business transaction type</Glossary>.

  
| API object | Mandatory fields |
| --- | --- |
| Shipper | ContactName |
| Shipper | Line 1 |
| Shipper | Town |
| Shipper | PostCode |
| Shipper | CountryCode |
| Shipper | EoriNumber |
| Destination | ContactName |
| Destination | Line 1 |
| Destination | Town |
| Destination | CountryCode |
| Destination | EoriNumber |
| Items | Quantity |
| Items | Description |
| Items | Value |
| Items | Weight |
| Items | HSCode |
| Items | CountryOfOrigin |

</Accordion>

<Accordion title="Ruleset L" icon="fa-solid fa-shield-check">

**Scenario example**: International non-document (<Glossary>NDX</Glossary>) shipments using <Glossary>DDP</Glossary> incoterm, with importer details required.

  
| API object | Mandatory fields |
| --- | --- |
| Shipper > Address | ContactName |
| Shipper > Address | Line1 |
| Shipper > Address | Town |
| Shipper > Address | PostCode |
| Shipper > Address | CountryCode |
| Shipper | EoriNumber |
| Destination > Address | ContactName |
| Destination > Address | Line 1 |
| Destination > Address | Town |
| Destination > Address | CountryCode |
| Destination > Address | ContactPhone |
| Destination | EoriNumber |
| Items | Quantity |
| Items | Description |
| Items | Value |
| Items | Weight |
| Items | HSCode |
| Items | CountryOfOrigin |
| Customs | QuotedLandedCost |
| CarrierSpecifics > Importer > Address | ContactName |
| CarrierSpecifics > Importer > Address | CompanyName |
| CarrierSpecifics > Importer > Address | Line1 |
| CarrierSpecifics > Importer > Address | Town |
| CarrierSpecifics > Importer > Address | CountryCode |
| CarrierSpecifics > Importer | EoriNumber |

</Accordion>

<br />