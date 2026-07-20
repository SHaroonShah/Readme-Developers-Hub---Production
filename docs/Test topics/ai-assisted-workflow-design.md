---
title: AI-Assisted Workflow Design
deprecated: false
hidden: false
metadata:
  robots: index
---
You will use this workflow to create, review, validate, and publish AI-assisted documentation while keeping humans responsible for technical accuracy and final approval.

<Callout icon="📘" theme="info">
  ### AI is a writing assistant, not a source of truth

  A designated reviewer must review and approve every AI-generated output before deployment.
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

Generate a first documentation draft from the attached reference documentation.

#### Inputs

- Product specification
- Engineering notes
- API specification (OpenAPI or Swagger)
- Release notes

#### Outputs

- Markdown documentation
- Example requests
- Example responses
- Suggested headings and glossary terms

<Accordion title="Draft-generator prompt" icon="file-lines">

```text
You are a Senior Technical Writer.
Generate documentation in Markdown.

Requirements:
- Write for software developers.
- Use clear, concise language.
- Include prerequisites.
- Include request examples.
- Include response examples.
- Add troubleshooting if applicable.
- Never invent endpoints.
- Never invent parameters.
- If information is missing, write "Information Required" instead of guessing.
```

</Accordion>

#### Human review

Confirm the following before approval:

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

***

### 2. Style guide reviewer

Review documentation against the stored company style guide V1.0 without changing its technical meaning.

#### Inputs

- Markdown documentation

#### Outputs

- Style corrections only

<Accordion title="Style-reviewer prompt" icon="pen-to-square">

```text
Review this documentation against the style guide.

Check:
- Grammar
- Tone
- Active voice
- Consistent headings
- Consistent terminology
- Concise paragraphs
- Bullet list formatting
- Procedures in numbered steps

Do not change technical meaning.
```

</Accordion>

#### Human review

The Technical Writer approves all suggested edits before merging.

#### Risks mitigated

- Inconsistent terminology
- Poor readability
- Formatting issues

***

### 3. Terminology checker

Identify inconsistent product terminology across the documentation repository.

#### Inputs

- Entire documentation repository

#### Outputs

- A list of inconsistent terms

For example, the checker can identify competing terms such as **Building**, **Facility**, and **Site**, then recommend one preferred term.

<Accordion title="Terminology-checker prompt" icon="magnifying-glass">

```text
Scan every Markdown file.
Identify inconsistent terminology.

List:
- Current term
- Preferred term
- Affected files

Do not rewrite documentation.
```

</Accordion>

#### Human review

The Product Manager confirms the official terminology before updates are applied.

#### Risks mitigated

- Conflicting terminology
- Duplicate concepts
- Customer confusion

***

### 4. Documentation quality checker

Validate the documentation repository before publication and return only the issues that require attention.

#### Inputs

- Entire repository

#### Outputs

- Quality report

#### Validation checks

- Broken links
- Broken tables
- Missing headings
- Empty sections
- Missing image captions
- Missing code blocks
- Missing examples
- Duplicate content

<Accordion title="Quality-checker prompt" icon="list-check">

```text
Review the documentation repository.
Return only issues.

Check for:
- Broken links
- Missing examples
- Duplicate sections
- Broken tables
- Formatting issues
- Markdown code errors

Do not rewrite content.
```

</Accordion>

#### Human review

The Technical Writer resolves all reported issues before approving the pull request.

#### Risks mitigated

- Publishing incomplete documentation
- Broken navigation
- Missing content

<br />
