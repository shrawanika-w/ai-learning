# Zero-Shot, One-Shot and Few-Shot Prompting

**Read time:** 6 minutes  
**Audience:** Everyone

## Zero-shot

Ask the model to perform the task without examples.

```text
Classify this production incident as Security, Reliability, Performance or Functional.

Incident:
Database credentials were committed to source control.
```

Use zero-shot when the task and expected output are obvious.

## One-shot

Provide one example.

```text
Example:
Incident: API latency increased from 100 ms to 3 seconds.
Classification: Performance

Now classify:
Database credentials were committed to source control.
```

Useful when one example communicates the expected behavior clearly.

## Few-shot

Provide multiple examples.

```text
Incident: API latency increased to 3 seconds.
Classification: Performance

Incident: A Kafka message was processed twice.
Classification: Reliability

Incident: Access token appeared in application logs.
Classification: Security

Incident: Refund amount is calculated incorrectly.
Classification: Functional

Incident: Database credentials were committed to source control.
Classification:
```

## Why examples help

Examples can communicate:

- Classification boundaries
- Expected wording
- Output structure
- Domain terminology
- Edge-case behavior

## Good examples

Examples should be:

- Correct
- Relevant
- Representative
- Diverse enough to show boundaries
- Consistent in format

## Common mistake

Do not provide examples containing mistakes unless the task explicitly teaches the model to identify those mistakes.

The model may imitate the pattern you demonstrate.

## Rule of thumb

Start simple. Add examples when they materially improve consistency or clarify behavior.

## Further reading

- https://ai.google.dev/gemini-api/docs/prompting-strategies
- https://docs.anthropic.com/en/docs/build-with-claude/prompt-engineering/overview
