---
title: AI-Assisted Workflow Design
deprecated: false
hidden: false
metadata:
  robots: index
---
# <br />Overview

The documentation workflow combines generative AI with Docs-as-Code approach to improve efficiency, maintainability, and consistency, ensuring that the published content remains the single source of truth.

<Callout icon="📘" theme="info">
  ### _Note_

  _Please bear in mind that the AI is treated only as a writing assistant rather than a source of truth. Every AI-generated output is reviewed and approved by a designated human resource before deployment._
</Callout>

## <br />Workflow overview

Engineering Change<br />│<br />▼<br />Product Requirements<br />│<br />▼<br />Draft Content Generation by AI<br />│<br />▼<br />Style & Terminology Review by AI<br />│<br />▼<br />Human Technical Review<br />│<br />▼<br />Documentation Validation <br />│<br />▼<br />Pull Request Approval<br />│<br />▼<br />Documentation Published

***

# AI vs Human responsibilities

| Steps       | AI Responsibility                            | Human Responsibility      |
| ----------- | -------------------------------------------- | ------------------------- |
| Drafting    | Generate first draft from engineering notes  | Verify technical accuracy |
| Editing     | Improve grammar and readability              | Approve wording           |
| Consistency | Enforce terminology and style guide          | Approve exceptions        |
| Review      | Identify missing sections                    | Confirm completeness      |
| Quality     | Detect broken formatting and inconsistencies | Final approval            |

***

## Use cases

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