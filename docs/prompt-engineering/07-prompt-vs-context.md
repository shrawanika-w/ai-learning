# 07 - Prompt vs Context

**Read time:** 6 minutes  
**Audience:** Everyone

## The difference

A **prompt** tells the AI what to do.

**Context** gives the AI information needed to do it.

Example:

```text
Prompt:
Add idempotency handling to the payment API.
```

Useful context might include:

```text
PaymentController.java
PaymentService.java
PaymentRepository.java
Database schema
API specification
Retry behavior
Existing coding standards
Existing tests
```

## Why prompts fail without context

The model may otherwise invent or assume:

- The database technology
- The idempotency-key format
- The transaction boundary
- Error responses
- Retention period
- Existing utilities

## More context is not always better

Bad context can be:

- Irrelevant
- Outdated
- Duplicated
- Contradictory
- Too broad

The objective is **relevant context**, not maximum context.

## Context sources

A modern AI coding workflow may use:

- Current file
- Selected code
- Open files
- Repository search
- Custom instructions
- Prompt files
- Conversation history
- Retrieved documentation
- Tools or MCP servers

## Prompt engineering vs context engineering

```text
Prompt engineering
How should I ask?

Context engineering
What should the model know, see and access?
```

For enterprise AI systems context engineering often has more impact than repeatedly rewriting the user prompt.

## Practical question

When an answer is weak ask:

> Is the instruction unclear or is important information missing?

Those are different problems.

## Further reading

- https://docs.github.com/en/copilot/how-tos/provide-context
- https://docs.github.com/en/copilot/get-started/best-practices
