# What is Prompt Engineering?

**Read time:** 5 minutes  
**Audience:** Everyone

## Why it matters

Generative AI models can produce very different results depending on how a task is described and what information is available. Prompt engineering is the practice of designing instructions and inputs so the model produces useful output consistently.

It is not about finding magic words. It is about communicating a task clearly.

## Core idea

A prompt may contain:

- The task
- Relevant context
- Constraints
- Examples
- Expected output format
- Validation criteria

Example:

```text
Review this Java method for concurrency defects.

Context:
The service runs across multiple Kubernetes pods.

Check:
- race conditions
- duplicate processing
- idempotency
- transaction boundaries

Return:
1. Findings
2. Severity
3. Recommended change
```

## Prompt engineering vs context engineering

**Prompt engineering** focuses on how the task is expressed.

**Context engineering** focuses on supplying the information, instructions, tools and state needed to complete the task.

Example:

```text
Prompt:
Implement createPayment().

Context:
PaymentService.java
PaymentRepository.java
API contract
Architecture rules
Security rules
Existing tests
```

A better prompt cannot compensate for missing business rules.

## What prompt engineering cannot guarantee

A good prompt does not guarantee:

- Correct facts
- Correct code
- Secure code
- Complete business logic
- Current knowledge
- Compliance with internal standards

Model output still requires validation.

## Remember

> The goal is not the perfect prompt. The goal is a reliable outcome.

## Quick checklist

Before sending a prompt ask:

- Is the task clear?
- Is important context available?
- Are constraints explicit?
- Is the expected output clear?
- How will I validate the result?

## Further reading

- https://developers.openai.com/api/docs/guides/prompt-engineering
- https://docs.github.com/en/copilot/get-started/best-practices
