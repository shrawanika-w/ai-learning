# Anatomy of a Good Prompt

**Read time:** 7 minutes  
**Audience:** Everyone

## Why it matters

Weak prompts force the model to make assumptions. Useful prompts reduce unnecessary ambiguity.

## A practical structure

Use five sections when the task needs them:

```text
TASK
CONTEXT
CONSTRAINTS
OUTPUT
VALIDATION
```

## 1. Task

Say exactly what should be done.

Weak:

```text
Check this code.
```

Better:

```text
Review this service for reliability and concurrency defects.
```

## 2. Context

Provide information required to interpret the task.

```text
This consumer processes payment events from Kafka.
Multiple pods can process partitions concurrently.
The producer may retry delivery.
```

## 3. Constraints

State boundaries.

```text
Do not change the public API.
Do not add a new database.
Use Java 21.
Use existing project dependencies only.
```

## 4. Output

Specify what a useful result looks like.

```text
Return a table with:
- finding
- severity
- evidence
- recommended change
```

## 5. Validation

Ask how the result should be checked.

```text
For each recommendation identify the test that would prove the change works.
```

## Optional components

Use when useful:

- Role or perspective
- Definitions
- Examples
- Source material
- Edge cases
- Assumptions
- Required citations

## Full example

```text
Task:
Review PaymentService.process() for duplicate-payment risk.

Context:
The method consumes Kafka events and may receive duplicate messages.
The service runs across multiple pods.

Constraints:
Do not propose distributed locking.
Prefer the existing PostgreSQL database.

Output:
For each issue provide severity, evidence and recommended fix.

Validation:
Include one test scenario for every high-severity finding.
```

## Remember

A prompt should contain enough information to remove important ambiguity but no irrelevant detail.

## Further reading

- https://developers.openai.com/api/docs/guides/prompt-engineering
- https://docs.github.com/en/copilot/get-started/best-practices
