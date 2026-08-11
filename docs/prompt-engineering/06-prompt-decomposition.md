# 06 - Prompt Decomposition and Chaining

**Read time:** 7 minutes  
**Audience:** Developers

## Why it matters

Large requests often contain several different cognitive tasks. Breaking them apart makes the workflow easier to inspect and validate.

## Decomposition

Instead of:

```text
Analyze, redesign, implement and test this payment service.
```

Use stages:

```text
1. Understand the existing design.
2. Identify problems.
3. Propose alternatives.
4. Select an approach.
5. Implement the change.
6. Generate tests.
7. Review the result.
```

## Prompt chaining

Prompt chaining passes the output of one focused task into another.

```text
Requirements extraction
        ↓
Gap analysis
        ↓
Implementation plan
        ↓
Code generation
        ↓
Code review
        ↓
Test generation
```

## Example workflow

### Step 1

```text
Extract the functional and non-functional requirements from this story.
Do not propose implementation yet.
```

### Step 2

```text
Using the extracted requirements identify ambiguities and missing acceptance criteria.
```

### Step 3

```text
Using the approved requirements propose an implementation plan for the current repository.
```

## Benefits

- Easier validation
- Clearer intermediate artifacts
- Less accidental scope expansion
- Better human checkpoints
- Easier debugging when the AI workflow fails

## Do not over-decompose

Ten unnecessary prompts can create more complexity than one clear prompt.

Decompose when subtasks have different goals, context or validation criteria.

## Developer pattern

```text
UNDERSTAND → PLAN → CHANGE → TEST → REVIEW
```

This is especially useful for AI-assisted software engineering because it keeps code generation from starting before the requirement and design are understood.

## Further reading

- https://docs.github.com/en/copilot/get-started/best-practices
- https://docs.anthropic.com/en/docs/test-and-evaluate/strengthen-guardrails/increase-consistency
