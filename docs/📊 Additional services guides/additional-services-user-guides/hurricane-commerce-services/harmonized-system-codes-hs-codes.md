---
title: Commodity Code Validations
excerpt: >-
  Commodity code validation involves verifying the Harmonised System (HS) codes
  used for products are accurate and compliant with the international trade
  regulations. Correct HS codes are crucial for customs clearance and helps in
  determining tariffs and taxes.
deprecated: false
hidden: false
icon: fad fa-input-numeric
link:
  new_tab: false
metadata:
  title: ''
  description: ''
  robots: index
---
<Image align="center" className="border" border={true} src="https://files.readme.io/1c67b5bfcde800b140388aef21b072010032929380b40bc2652f36fc7a5388cc-HS_code.png" />

<Columns layout="auto">
  <Column>
    As the world of eCommerce progresses, customs in countries around the globe are insisting on good quality data to facilitate simple clearance of goods being shipped. Many destinations now require electronic pre-advice data which includes Harmonised System commodity codes (<Glossary>HS Code</Glossary>).
  </Column>
</Columns>

<Accordion title="Hurricane Commerce Service" icon="fa-shipping-fast">
  Hurricane commerce service checks and identifies the HS code and their descriptions, ensuring they are correct and compliant with customs regulations, preventing delays and penalties.
</Accordion>

<Cards columns={2}>
  <Card title="Validate and Match" icon="fa-check-circle">
    Validate and match HS code and description
  </Card>
  <Card title="Export Codes" icon="fa-file-export">
    Provide “most likely” or “suitable” 10-digit export codes
  </Card>
  <Card title="Import Codes" icon="fa-file-import">
    Provide “most likely” or "suitable" 10-digit import codes
  </Card>
  <Card title="Generate Description" icon="fa-file-alt">
    Generate a suitable description based on provided HS6
  </Card>
  <Card title="Generate HS6" icon="fa-code">
    Generate “most likely” or “suitable” HS6 based on provided description
  </Card>
</Cards>

> 📘 *Note*
>
> *For more information on how to use this API service, refer to the [Commodity Code Validation](https://docs.intersoftsapient.net/reference/post_v4-getcommoditycodevalidations) block of the **API References** section.*