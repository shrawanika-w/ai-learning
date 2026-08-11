# 11 - Prompt Templates and Reuse

**Read time:** 7 minutes  
**Audience:** Developers

## Why templates matter

If a prompt is useful repeatedly it should not live only in someone's chat history.

A prompt template makes the task reusable and reviewable.

## Example template

```text
Review the following {{language}} code.

Purpose:
{{business_purpose}}

Architecture constraints:
{{architecture_constraints}}

Review for:
- correctness
- security
- reliability
- maintainability

Code:
{{code}}

Return findings with severity, evidence and recommendation.
```

## Good template characteristics

A reusable template should have:

- Clear purpose
- Named inputs
- Required and optional fields
- Stable instructions
- Explicit output format
- Validation criteria
- Owner

## Separate static and dynamic content

Static:

```text
Never log complete payment account numbers.
Return severity as Critical, High, Medium or Low.
```

Dynamic:

```text
{{source_code}}
{{requirement}}
{{service_name}}
```

## Validate variables

Do not assume every variable will be present.

Application code should validate required prompt inputs before invoking the model.

## Prompt file example

```text
.github/prompts/security-review.prompt.md
```

A source-controlled prompt file can be reviewed and evolved like code.

## When not to use a prompt template

Do not force every task into a template. Ad hoc exploration can remain conversational.

Templates are most valuable for repeated tasks where consistency matters.

## Suggested metadata

```yaml
name: security-code-review
owner: platform-engineering
version: 1.2
purpose: Review application changes for common security risks
```

## Further reading

- https://docs.github.com/en/copilot/tutorials/customization-library/prompt-files/your-first-prompt-file
- https://developers.openai.com/api/docs/guides/prompt-engineering
