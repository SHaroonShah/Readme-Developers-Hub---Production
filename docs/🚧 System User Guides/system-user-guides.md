---
title: System user guides
deprecated: false
hidden: false
icon: fad fa-user-shield
link:
  new_tab: false
metadata:
  robots: index
---
# System User Guides

<Cards columns={2}>
  <Card title="Getting Started" href="#overview" icon="rocket">
    Transform complex concepts into clear, engaging documentation that helps developers succeed with your API.
  </Card>
  <Card title="Content Management" href="#creating-and-managing-guides" icon="edit">
    Create, organize, and publish documentation in real-time with our intuitive editor.
  </Card>
  <Card title="Structure & Organization" href="#structuring-your-documentation" icon="sitemap">
    Design logical content flows that guide developers through your API journey.
  </Card>
  <Card title="Best Practices" href="#best-practices-for-writing-guides" icon="star">
    Learn proven techniques for creating guides developers actually want to read.
  </Card>
</Cards>

## Overview

Think of Guides as your API's instruction manual. This is where you'll transform complex concepts into clear, engaging documentation that helps developers succeed with your API. Whether you're documenting authentication flows or walking through common use cases, we've got the tools to make your docs shine.

## Creating and Managing Guides

<Tabs>
  <Tab title="Editor Features">
    Writing great documentation shouldn't feel like rocket science. Our editing experience brings documentation creation right to your hub, where you can:

    * Create and organize documentation in real-time
    * Preview changes exactly as your users will see them
    * Collaborate with your team seamlessly
    * Publish updates with confidence

    Your docs live where you do – right in the hub. Spot something that needs updating? Just click, edit, and publish. No more context-switching between different interfaces!
  </Tab>
  <Tab title="MDX Components">
    With our MDX-powered editor, you can take your guides beyond static text:

    * Add interactive code samples that developers can test right in your docs
    * Create expandable sections for complex topics
    * Insert diagrams and visualizations to explain complex concepts
    * Build custom components to showcase your API's unique features
  </Tab>
</Tabs>

## Structuring Your Documentation

Great documentation tells a story. Some developers will want to dive straight into code samples, while others might need more background. Our structure lets you cater to both by helping you organize your content in a way that makes sense for your API:

<Columns layout="auto">
  <Column>
    ### Content Organization
    * **Categories**: Group related content together
    * **Pages**: Create standalone guides or multi-page tutorials
    * **Sections**: Break down complex topics into digestible chunks
    * **Custom Navigation**: Design a flow that guides developers through your API journey
  </Column>
  <Column>
    ### URL Structure
    The URL structure of your site will be `subdomain/docs/page-slug`. Only the subdomain and the page-slug can be changed. The docs and reference paths cannot be changed.
  </Column>
</Columns>

<Accordion title="Guides Structure Configuration" icon="cog">
Page order and navigation are controlled by `_order.yaml` files:

```yaml
- welcome-page
- getting-started
- advanced-topics
  - feature-one
  - feature-two
```

The organization includes:
* The organization of your documentation (guides, API reference, recipes, etc.)
* Version information to ensure AI models reference the most current documentation
* Important terminology specific to your API
* Hierarchical structure of your content
</Accordion>

## Best Practices for Writing Guides

The most effective guides combine clear explanations with practical examples. Here are some tips to make your guides more helpful:

<Cards columns={2}>
  <Card title="Content Strategy" icon="lightbulb">
    * **Start with the why**: Explain the purpose and benefits before diving into implementation
    * **Use progressive disclosure**: Begin with basic concepts before introducing advanced topics
    * **Show, don't just tell**: Include code examples that developers can copy and adapt
  </Card>
  <Card title="User Experience" icon="users">
    * **Consider different learning styles**: Some developers learn by reading, others by doing
    * **Keep it scannable**: Use headings, lists, and callouts to make information easy to find
    * **Update regularly**: Keep your guides in sync with your API as it evolves
  </Card>
</Cards>

## 🔄 Reusing Content Across Guides

> 📘 **Business Tier Feature**
>
> Reusable Content is available on our Enterprise plan. Want to level up your documentation? Reach out to our team to learn more about Enterprise features that can supercharge your docs!

Why write the same explanation twice? With reusable content blocks, you can:

* Create consistent explanations for common concepts
* Update information in one place and see it change everywhere
* Maintain a unified voice across your entire documentation
* Save time and reduce the risk of outdated information

## Advanced Configuration

<Accordion title="First Page Settings" icon="home">
In this drop-down menu, you can select the first page that is shown when your users visit the site.

<Image align="center" className="border" border={true} src="https://files.readme.io/aef201d-Screen_Shot_2020-10-20_at_4.37.37_PM.png" />
</Accordion>

<Accordion title="Section Names" icon="tags">
The section names such Documentation can be changed here and it will propagate throughout your entire instance.

![](https://files.readme.io/c697a7b-Screen_Shot_2023-04-20_at_12.35.19_PM.png)
</Accordion>

## Next Steps

Ready to create guides that your developers will actually want to read? Here's how to get started:

<Cards columns={1}>
  <Card title="Get Started with Your First Guide" href="doc:creating-and-managing-guides#/creating-your-first-guide" icon="play">
    Create your first guide with our intuitive editor and see how easy documentation can be.
  </Card>
  <Card title="Organize Your Content" href="doc:structuring-your-docs" icon="folder-tree">
    Structure your documentation into a logical hierarchy that makes sense for your users.
  </Card>
  <Card title="Add Interactive Elements" href="doc:mdx" icon="code">
    Enhance your guides with MDX components for a richer developer experience.
  </Card>
  <Card title="Set Up Reusable Content" href="doc:reusable-content" icon="recycle">
    Maintain consistency across your docs with reusable content blocks.
  </Card>
</Cards>