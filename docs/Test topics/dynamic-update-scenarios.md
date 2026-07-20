---
title: Dynamic Update Scenarios
deprecated: false
hidden: true
metadata:
  robots: index
---
You will use these scenarios to update documentation accurately when product terminology, features, or technical behavior changes.

## Overview

Documentation must evolve with the product so it does not become outdated or inconsistent. These scenarios show how the documentation process responds to common Software Development Lifecycle (SDLC) changes while maintaining accuracy and consistency.

<Callout icon="fa-solid fa-user-check" theme="info">
  ### _Note_

  _AI can identify inconsistencies, generate drafts, and validate formatting. Human reviewers remain responsible for approving product terminology and technical accuracy._
</Callout>

## Scenario overview

<Cards columns={3}>
  <Card title="Terminology change" href="#scenario-1--minor-ui-terminology-change" icon="fa-solid fa-tags">
    Update approved product language across affected documentation without changing backend behavior.
  </Card>
  <Card title="Feature launch" href="#scenario-2--major-feature-launch" icon="fa-solid fa-rocket">
    Create and validate new documentation for a product capability and its APIs.
  </Card>
  <Card title="Outdated information" href="#scenario-3--conflicting-or-outdated-information" icon="fa-solid fa-triangle-exclamation">
    Resolve conflicting technical values and restore a single source of truth.
  </Card>
</Cards>

## Scenario 1 – Minor UI terminology change

<Columns layout="auto">
  <Column>

### Product change

The user interface renames *Building Groups* to *Spaces*. No backend functionality changes.

  </Column>
  <Column>

### Documentation impact

Update the following pages:

- Introduction
- Quick Start
- API Reference
- Troubleshooting

  </Column>
</Columns>

### AI workflow

**AI agent:** Terminology Checker

1. Scan every Markdown file for occurrences of the previous terminology.
2. Recommend replacements using the approved term, _Spaces_.
3. Generate a change report for review.

### Human review

The Product Manager confirms that _Spaces_ is the approved product term. The Technical Writer reviews each suggested replacement to ensure it fits naturally in context.

### Quality checks

- Verify terminology consistency.
- Test internal links.
- Review navigation labels.
- Check screenshot references.

### Approval

The Technical Writer approves the pull request, and the Documentation Owner merges the changes.

## Scenario 2 – Major feature launch

<Columns layout="auto">
  <Column>

### Product change

A new *Energy Analytics Dashboard API* is introduced with endpoints for:

- Energy consumption
- Carbon emissions
- Historical trends
- Forecast data

  </Column>
  <Column>

### Documentation impact

Create or update:

- API Reference pages
- A Quick Start tutorial
- Authentication guidance
- A troubleshooting section
- Navigation for the new content

  </Column>
</Columns>

### AI workflow

**AI Draft Generator** creates initial Markdown pages from:

- The OpenAPI specification
- Product requirements
- Engineering design notes

**Style Guide Reviewer** checks that new pages follow documentation standards.

**Quality Checker** verifies:

- Request examples
- Response examples
- Code formatting
- Internal links

### Human review

The Software Engineer validates endpoints, parameters, payloads, and response examples. The Product Manager confirms feature descriptions, and the Technical Writer edits for clarity and usability.

### Approval

All reviewers approve the pull request before publication.

## Scenario 3 – Conflicting or outdated information

<Columns layout="auto">
  <Column>

### Product change

A support engineer reports that authentication tokens now expire after *30 minutes*, while the documentation still states *60 minutes*.

  </Column>
  <Column>

### Documentation impact

Update the following pages:

- Authentication
- Quick Start
- API Reference

  </Column>
</Columns>

### AI workflow

**AI Quality Checker** identifies conflicting values across the documentation and produces a report for the affected pages:

- `Authentication.md`
- `Quick-Start.md`
- `API Reference.md`

**AI Terminology Checker** verifies that one approved value remains after the update.

### Human review

The Backend Engineer confirms the correct token expiration. The Technical Writer updates every affected page.

### Validation

Automated checks confirm that:

- No conflicting values remain.
- No duplicated guidance exists.
- Internal links still work.

### Approval

The Software Engineer and Technical Writer approve the pull request. Documentation is published with the next release.

## Summary

| Scenario                            | AI role                                                | Human review                                             | Outcome                                              |
| ----------------------------------- | ------------------------------------------------------ | -------------------------------------------------------- | ---------------------------------------------------- |
| UI terminology change               | Terminology detection and update suggestions           | Product Manager and Technical Writer                     | Consistent terminology across documentation          |
| Major feature launch                | Draft generation, style checks, and quality validation | Software Engineer, Product Manager, and Technical Writer | New documentation published with the product release |
| Outdated or conflicting information | Conflict detection and repository-wide validation      | Backend Engineer and Technical Writer                    | A single source of truth is restored                 |

## Key principles

- Version-control documentation changes through Git.
- Use AI to accelerate repetitive work, not to replace human validation.
- Trigger documentation updates when product changes occur.
- Treat documentation as part of the software development lifecycle.
- Hold human reviewers accountable for technical accuracy and final approval.

Together, Docs-as-Code practices, AI-assisted workflows, and structured review gates keep documentation accurate, scalable, and aligned with the evolving product.
