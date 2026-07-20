---
title: Dynamic Update Scenarios
deprecated: false
hidden: true
metadata:
  robots: index
---
# <br />Overview

Documentation must evolve alongside the product, not at the end of the development process so that it is not outdated or inconsistent.&#x20;

This section demonstrates how the documentation system responds to different types of product changes during the SDLC while maintaining accuracy, consistency across the documentation.

# Scenario 1 – Minor UI Terminology Change

## Product Change

The user interface renames _Building Groups_ to _Spaces_.
No backend functionality changes.
---------------------------------

## Documentation Impact

Affected pages:

- Introduction
- Quick Start
- API Reference
- Troubleshooting

***

## AI Workflow

### AI Agent

Terminology Checker

### Tasks

- Scan every Markdown file
- Find occurrences of "Buildings"
- Recommend replacing with "Commercial Sites"
- Generate a change report

***

## Human Review

Product Manager verifies that "Spaces" is the approved product term.
Technical Writer reviews each change to ensure the new term fits naturally within the content.
----------------------------------------------------------------------------------------------

## Quality Checks

- Terminology consistency
- Broken internal links
- Navigation labels
- Screenshot references

***

## Approval

Technical Writer approves the Pull Request.
Documentation Owner merges changes.
-----------------------------------

# Scenario 2 – Major Feature Launch

## Product Change

A new _Energy Analytics Dashboard API_ is introduced.
New endpoints include:

- Energy consumption
- Carbon emissions
- Historical trends
- Forecast data

***

## Documentation Impact

New documentation required:

- New API Reference pages
- New Quick Start tutorial
- Authentication updates
- New troubleshooting section
  Navigation must also be updated.

***

## AI Workflow

### AI Draft Generator

Creates initial Markdown pages using:

- OpenAPI specification
- Product requirements
- Engineering design notes

***

### Style Guide Reviewer

## Ensures all new pages follow the documentation standards.

### Quality Checker

Confirms:

- Request examples
- Response examples
- Code formatting
- Internal links

***

## Human Review

Software Engineer validates:

- Endpoints
- Parameters
- Payloads
- Response examples
  Product Manager confirms feature descriptions.
  Technical Writer edits for clarity and usability.

***

## Approval

## All reviewers approve the Pull Request before publication.

# Scenario 3 – Conflicting or Outdated Information

## Product Change

## A support engineer reports that authentication tokens now expire after _30 minutes, but the documentation still states60 minutes_.

## Documentation Impact

Affected pages:

- Authentication
- Quick Start
- API Reference

***

## AI Workflow

### AI Quality Checker

Flags conflicting values across documentation.
Produces a report showing:
Authentication.md
Quick-Start.md
API Reference.md
----------------

### AI Terminology Checker

## Ensures only one approved value remains after updates.

## Human Review

Backend Engineer confirms the correct token expiration.
Technical Writer updates every affected page.
---------------------------------------------

## Validation

Automated checks confirm:

- No conflicting values remain.
- No duplicated guidance exists.
- Internal links still work.

***

## Approval

Pull Request approved by:

- Software Engineer
- Technical Writer
  Documentation is published with the next release.

***

# Summary

| Scenario                            | AI Role                                            | Human Review                                         | Outcome                                          |
| ----------------------------------- | -------------------------------------------------- | ---------------------------------------------------- | ------------------------------------------------ |
| UI terminology change               | Terminology detection and update suggestions       | Product Manager and Technical Writer                 | Consistent terminology across all documentation  |
| Major feature launch                | Draft generation, style checks, quality validation | Software Engineer, Product Manager, Technical Writer | New documentation published with product release |
| Outdated or conflicting information | Conflict detection and repository-wide validation  | Backend Engineer and Technical Writer                | Single source of truth restored                  |

***

# Key Principles

These scenarios demonstrate several important documentation practices:

- Documentation changes are version-controlled through Git.
- AI accelerates repetitive tasks but never replaces human validation.
- Product changes automatically trigger documentation updates.
- Documentation is treated as part of the software development lifecycle.
- Human reviewers remain responsible for technical accuracy and final approval.
  By combining Docs-as-Code practices with AI-assisted workflows and structured review gates, the documentation remains accurate, scalable, and aligned with the evolving product.

<br />
