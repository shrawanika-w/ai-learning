# Reasoning Prompts

**Read time:** 6 minutes  
**Audience:** Developers

## Why this topic changed

Older prompt tutorials often recommend phrases such as:

```text
Think step by step and show all reasoning.
```

That is not a universal best practice.

Modern reasoning models can perform internal reasoning and often work well with short direct instructions.

## Prefer clear objectives

Example:

```text
Determine whether this Kafka consumer can process the same payment twice.

Return:
1. Conclusion
2. Important assumptions
3. Evidence from the code
4. Failure scenario
5. Recommended tests
```

This asks for useful evidence without requiring a hidden reasoning trace.

## Ask for decomposition when useful

For complex engineering work:

```text
Analyze the problem before proposing code.
First identify failure modes and constraints.
Then recommend an implementation.
```

## Ask for alternatives

```text
Propose three ways to implement idempotency.
Compare correctness, operational complexity and failure behavior.
Recommend one for this architecture.
```

This reduces premature commitment to the first plausible solution.

## Ask for counterarguments

Instead of:

```text
Explain why this design is correct.
```

Use:

```text
Try to find failure scenarios that would make this design unsafe.
```

## Separate reasoning from validation

A detailed explanation is not proof.

Validation may require:

- Compilation
- Unit tests
- Integration tests
- Load testing
- Security scanning
- Architecture review
- Official documentation

## Key lesson

Prompt for the **decision, evidence, assumptions and validation**, not for a theatrical reasoning transcript.

## Further reading

- https://developers.openai.com/api/docs/guides/reasoning-best-practices
