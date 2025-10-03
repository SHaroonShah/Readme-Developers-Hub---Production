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
<HTMLBlock>{`
Ctrl K
Docs
Blog
Showcase
Sponsor
Plus
July 25, 2025
Vanilla JavaScript support for Tailwind Plus

Philipp Spiess
@PhilippSpiess

Adam Wathan
@adamwathan
Tailwind Plus Elements
There are a lot of UI blocks in Tailwind Plus that need JavaScript to really be useful, like dialogs, dropdowns, command palettes, and more. And unless you're a React or Vue user, using those UI blocks has always meant writing all of that tricky JavaScript yourself.

Well today that finally changes — every UI block in Tailwind Plus is now fully functional, accessible, and interactive, including the plain HTML examples.

Now you can use any dropdown, command palette, dialog, drawer, and more in any project you're working on — no JavaScript framework required.

No framework required
To pull this off, we built @tailwindplus/elements — a library we're releasing exclusively for Tailwind Plus customers.

Elements is a collection of headless custom elements that wrap up all of the complex behavior needed to build custom interactive UIs using just HTML, and can be styled any way you like using utility classes or custom CSS.

Instead of being coupled to a specific JavaScript framework, these custom elements work anywhere you can use a <script> tag:

index.html
<script src="https://cdn.jsdelivr.net/npm/@tailwindplus/elements@1" type="module"></script>
Here's what it look like to build a custom dropdown menu with Elements:

<el-dropdown class="relative inline-block text-left">
  <button class="inline-flex w-full justify-center gap-x-1.5 rounded-md bg-white px-3 py-2 text-sm font-semibold text-gray-900 shadow-xs ring-1 ring-gray-300 ring-inset hover:bg-gray-50">
    Options
    <svg viewBox="0 0 20 20" fill="currentColor" aria-hidden="true" class="-mr-1 size-5 text-gray-400">
      <path d="M5.22 8.22a.75.75 0 0 1 1.06 0L10 11.94l3.72-3.72a.75.75 0 1 1 1.06 1.06l-4.25 4.25a.75.75 0 0 1-1.06 0L5.22 9.28a.75.75 0 0 1 0-1.06Z" clip-rule="evenodd" fill-rule="evenodd" />
    </svg>
  </button>
  <el-menu anchor="bottom end" popover class="w-56 origin-top-right rounded-md bg-white shadow-lg ring-1 ring-black/5 transition transition-discrete [--anchor-gap:--spacing(2)] focus:outline-hidden data-closed:scale-95 data-closed:transform data-closed:opacity-0 data-enter:duration-100 data-enter:ease-out data-leave:duration-75 data-leave:ease-in">
    <div class="py-1">
      <a href="#" class="block px-4 py-2 text-sm text-gray-700 focus:bg-gray-100 focus:text-gray-900 focus:outline-hidden">Account settings</a>
      <a href="#" class="block px-4 py-2 text-sm text-gray-700 focus:bg-gray-100 focus:text-gray-900 focus:outline-hidden">Support</a>
      <a href="#" class="block px-4 py-2 text-sm text-gray-700 focus:bg-gray-100 focus:text-gray-900 focus:outline-hidden">License</a>
      <form action="#" method="POST">
        <button type="submit" class="block w-full px-4 py-2 text-left text-sm text-gray-700 focus:bg-gray-100 focus:text-gray-900 focus:outline-hidden">Sign out</button>
      </form>
    </div>
  </el-menu>
</el-dropdown>
`}</HTMLBlock>

<br />

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
