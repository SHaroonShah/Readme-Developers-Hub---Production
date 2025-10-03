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

<HTMLBlock>{`
<!-- Include this script tag or install \`@tailwindplus/elements\` via npm: -->
<!-- <script src="https://cdn.jsdelivr.net/npm/@tailwindplus/elements@1" type="module"></script> -->
<button command="show-modal" commandfor="drawer" class="rounded-md bg-gray-950/5 px-2.5 py-1.5 text-sm font-semibold text-gray-900 hover:bg-gray-950/10">Open drawer</button>
<el-dialog>
  <dialog id="drawer" aria-labelledby="Hello" class="fixed inset-0 size-auto max-h-none max-w-none overflow-hidden bg-transparent not-open:hidden backdrop:bg-transparent">
    <el-dialog-backdrop class="absolute inset-0 bg-gray-500/75 transition-opacity duration-500 ease-in-out data-closed:opacity-0"></el-dialog-backdrop>

    <div tabindex="0" class="absolute inset-0 pl-10 focus:outline-none sm:pl-16">
      <el-dialog-panel class="group/dialog-panel relative ml-auto block size-full max-w-md transform transition duration-500 ease-in-out data-closed:translate-x-full sm:duration-700">
        <!-- Close button, show/hide based on slide-over state. -->
        <div class="absolute top-0 left-0 -ml-8 flex pt-4 pr-2 duration-500 ease-in-out group-data-closed/dialog-panel:opacity-0 sm:-ml-10 sm:pr-4">
          <button type="button" command="close" commandfor="drawer" class="relative rounded-md text-gray-300 hover:text-white focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-indigo-600">
            <span class="absolute -inset-2.5"></span>
            <span class="sr-only">Close panel</span>
            <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5" data-slot="icon" aria-hidden="true" class="size-6">
              <path d="M6 18 18 6M6 6l12 12" stroke-linecap="round" stroke-linejoin="round" />
            </svg>
          </button>
        </div>

        <div class="relative flex h-full flex-col overflow-y-auto bg-white py-6 shadow-xl">
          <div class="px-4 sm:px-6">
            <h2 id="drawer-title" class="text-base font-semibold text-gray-900">Panel title</h2>
          </div>
          <div class="relative mt-6 flex-1 px-4 sm:px-6">
            <!-- Your content -->
          </div>
        </div>
      </el-dialog-panel>
    </div>
  </dialog>
</el-dialog>
`}</HTMLBlock>

<br />
