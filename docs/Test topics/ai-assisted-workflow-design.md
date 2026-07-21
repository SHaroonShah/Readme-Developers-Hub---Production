---
title: AI-Assisted Workflow Design
deprecated: false
hidden: true
metadata:
  robots: index
---
# AI-Assisted Workflow Design

You will use this workflow to create, review, validate, and publish AI-assisted documentation while keeping humans responsible for technical accuracy and final approval.

<Callout icon="📘" theme="info">
  ### _Note_

  _Bear in mind that AI is a writing assistant, not a source of truth. A designated reviewer must review and approve every AI-generated output before deployment._
</Callout>

## Workflow

Follow these stages for every documentation change:

1. **Engineering change** — Capture the change that affects the product or its integration.
2. **Product requirements** — Gather the requirements and supporting technical context.
3. **AI draft generation** — Generate a first documentation draft from the available source material.
4. **AI style and terminology review** — Check the draft against the style guide and approved terminology.
5. **Human technical review** — Verify that the content is technically accurate.
6. **Documentation validation** — Check formatting, links, examples, and completeness.
7. **Pull request approval** — Obtain approval for the documentation change.
8. **Publication** — Publish the approved documentation as the single source of truth.

## Responsibilities

<Columns layout="auto">
  <Column>

### AI responsibilities

| Activity | Responsibility |
| --- | --- |
| Drafting | Generate a first draft from engineering notes. |
| Editing | Improve grammar and readability. |
| Consistency | Enforce approved terminology and style-guide rules. |
| Review | Identify missing sections. |
| Quality | Detect broken formatting and inconsistencies. |

  </Column>
  <Column>

### Human responsibilities

| Activity | Responsibility |
| --- | --- |
| Drafting | Verify technical accuracy. |
| Editing | Approve wording. |
| Consistency | Approve exceptions to terminology and style guidance. |
| Review | Confirm completeness. |
| Quality | Provide final approval. |

  </Column>
</Columns>

## AI agent use cases

### 1. Documentation draft generator

The Draft generator agent is responsible for generating the initial version of the documentation from trusted technical sources, such as product requirements, user stories, engineering notes, or API specifications. Its goal is to accelerate content creation while ensuring the output is clear, structured, and written in Markdown. The prompt explicitly instructs the AI not to invent technical details and to flag missing information for human review.

#### Purpose

Generate a first draft from the provided information.&#x20;

#### Inputs

- Product specification
- Engineering notes
- API specification (OpenAPI or Swagger)
- User Stories

#### Outputs

- Markdown documentation
- Example request payload
- Example response payload
- Suggested headings

#### Prompt

```text
You are a Senior Technical Writer at SmartBuilding. Generate documentation in Markdown condisering the following guidelines:

Guidelines:
- Write for software developers.
- Use clear, concise language.
- Include prerequisites.
- Include request payload.
- Include response payload.
- Add troubleshooting if applicable.
- Do not invent endpoints.
- Do not invent parameters.
- If any information is missing, write "Information Required" instead of guessing.
```

#### Human review

The reviewer confirms:

- Endpoint names
- Parameters
- Request bodies
- Response examples
- Product terminology

#### Risks mitigated

- Hallucinated endpoints
- Fake request examples
- Incorrect parameters
- Missing prerequisites

### 2. Style guide reviewer

The Review generator agent serves as an editorial assistant by reviewing the initial draft documentation for grammar, readability, formatting, and compliance with the ingested documentation style guide. It focuses on improving the quality and consistency of the writing without altering the underlying technical meaning. All suggested changes are reviewed and approved by a Technical Writer before publication.

#### Purpose

Ensure all documentation follows the company style guide and standards.

#### Inputs

- Markdown documentation

#### Outputs

- Style corrections only

#### Prompt

```text
Review this documentation against the ingested style guide, keeping in view the following checks:

Checks:
- Grammar
- Tone
- Active voice
- Consistent headings
- Consistent terminology
- Short paragraphs
- Bullet list formatting

Do not change technical meaning.
```

#### Human review

The Technical Writer approves all suggested edits before merging.

#### Risks mitigated

- Inconsistent terminology
- Poor readability
- Formatting issues

### 3. Terminology checker

The Terminology checker agent ensures that product terminology remains consistent across the entire documentation repository. It scans all Markdown files and glossary to identify inconsistent naming, outdated terms, or duplicate terminology and generates a report with recommended corrections. This helps maintain a single source of truth and prevents confusion for users as the product evolves.

#### Purpose

Ensure consistent product terminology across all documentation.

#### Inputs

- Entire documentation repository

#### Outputs

- List of inconsistent terms

For example, the checker can identify competing terms such as **Building**, **Facility**, and **Site**, then recommend one preferred term.

#### Prompt

```text
Scan every Markdown file.
Identify inconsistent terminology.

List:
- Current term
- Preferred term
- Affected files

Do not rewrite documentation.
```

#### Human review

The Product Manager confirms the official terminology before updates are applied by the Technical Writer.

#### Risks mitigated

- Conflicting terminology
- Duplicate concepts
- Customer confusion

### 4. Documentation quality checker

The Quality Check agent performs a final validation of the documentation before publication. It checks for issues such as broken links, missing sections, broken tables, formatting errors, duplicate content, and incomplete code examples. Instead of rewriting content, it generates an audit report that allows the Technical Writer to resolve issues before the documentation is merged and published.

#### Purpose

Validate documentation before publication.

#### Inputs

- Entire repository

#### Outputs

- Audit report

#### Validation checks

- Broken links
- Missing headings
- Empty sections
- Broken tables
- Missing code blocks
- Missing examples
- Duplicate content

#### Prompt

```text
Review the documentation repository.
Return only issues.

Check for:
- Broken links
- Missing examples
- Duplicate sections
- Boken tables
- Formatting problems
- Markdown errors

Do not rewrite content.
```

#### Human review

The Technical Writer resolves all reported issues before approving the pull request.

#### Risks mitigated

- Publishing incomplete documentation
- Broken navigation
- Missing content

<br />
