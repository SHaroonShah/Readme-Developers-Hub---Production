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

<ToggleList>
  <ToggleListItem title="1. Documentation draft generator">

### Purpose

Generate a first draft from engineering notes.

### Inputs

- Product specification
- Engineering notes
- API specification (OpenAPI or Swagger)
- Release notes

### Outputs

- Markdown documentation
- Example requests
- Example responses
- Suggested headings

### Prompt

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

### Human review

The reviewer confirms:

- Endpoint names
- Parameters
- Request bodies
- Response examples
- Product terminology

### Risks mitigated

- Hallucinated endpoints
- Fake request examples
- Incorrect parameters
- Missing prerequisites

  </ToggleListItem>
  <ToggleListItem title="2. Style guide reviewer">

### Purpose

Ensure all documentation follows the team's writing standards.

### Inputs

- Markdown documentation

### Outputs

- Style corrections only

### Prompt

```text
Review this documentation against the style guide.

Check:
- Grammar
- Tone
- Active voice
- Consistent headings
- Consistent terminology
- Short paragraphs
- Bullet list formatting

Do not change technical meaning.
```

### Human review

The Technical Writer approves all suggested edits before merging.

### Risks mitigated

- Inconsistent terminology
- Poor readability
- Formatting issues

  </ToggleListItem>
  <ToggleListItem title="3. Terminology checker">

### Purpose

Ensure consistent product terminology across all documentation.

### Inputs

- Entire documentation repository

### Outputs

- List of inconsistent terms

For example, the checker can identify competing terms such as **Building**, **Facility**, and **Site**, then recommend one preferred term.

### Prompt

```text
Scan every Markdown file.
Identify inconsistent terminology.

List:
- Current term
- Preferred term
- Affected files

Do not rewrite documentation.
```

### Human review

The Product Manager confirms the official terminology before updates are applied.

### Risks mitigated

- Conflicting terminology
- Duplicate concepts
- Customer confusion

  </ToggleListItem>
  <ToggleListItem title="4. Documentation quality checker">

### Purpose

Validate documentation before publication.

### Inputs

- Entire repository

### Outputs

- Quality report

### Validation checks

- Broken links
- Missing headings
- Empty sections
- Placeholder text
- Missing code blocks
- Missing examples
- Duplicate content

### Prompt

```text
Review the documentation repository.
Return only issues.

Check for:
- Broken links
- Missing examples
- Duplicate sections
- Placeholder text
- Formatting problems
- Markdown errors

Do not rewrite content.
```

### Human review

The Technical Writer resolves all reported issues before approving the pull request.

### Risks mitigated

- Publishing incomplete documentation
- Broken navigation
- Missing content

  </ToggleListItem>
</ToggleList>

<br />
