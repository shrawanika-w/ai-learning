# 12 - Prompt Versioning and Change History

**Read time:** 7 minutes  
**Audience:** Developers and AI Leads

## Why version prompts

A production prompt is part of application behavior.

Changing:

```text
"Summarize the risk"
```

to:

```text
"Return only material risks with supporting evidence"
```

can materially change system output.

Prompt changes should therefore be traceable.

## Treat prompts as code

For reusable prompts use:

```text
Edit → Commit → Review → Test → Evaluate → Release
```

Git provides:

- Change history
- Pull requests
- Review
- Branching
- Tags
- Rollback

## Suggested metadata

```yaml
name: payment-code-review
version: 1.3.0
owner: architecture-team
status: approved
updated: 2026-08-10
```

## Semantic versioning idea

This is optional but useful.

**PATCH**
Small wording change with no intended behavior change.

**MINOR**
New review rule, output field or supported scenario.

**MAJOR**
Material change to expected behavior or output contract.

## Keep a change history

```text
v1.0
Initial review prompt.

v1.1
Added idempotency checks.

v1.2
Added sensitive-data logging checks.

v2.0
Changed output schema and severity definitions.
```

Record **why** the prompt changed.

## Version more than the prompt

For reproducibility also track:

- Model name or version
- Model parameters
- Context source version
- Tool version
- Evaluation dataset
- Evaluation result

A prompt can behave differently when the model or context changes.

## Release principle

Do not promote a prompt because it "looks better" on one example.

Compare versions against a stable evaluation set.

## Further reading

- https://developers.openai.com/api/docs/guides/evaluation-best-practices
- https://developers.openai.com/api/docs/guides/model-optimization
