# Prompt Engineering Quick Reference

## Simple prompt structure

```text
ROLE
Who should the model act as?

TASK
What should it do?

CONTEXT
What does it need to know?

CONSTRAINTS
What boundaries apply?

INPUT
What information should it work on?

OUTPUT
What should the answer look like?

VALIDATION
How should correctness be checked?
```

Not every prompt needs every section.

## Example

```text
You are a senior Java engineer reviewing a payment service.

Task:
Review the retry implementation for duplicate-processing risk.

Context:
The operation is not automatically idempotent.

Constraints:
Do not change the public API.
Do not introduce new dependencies.

Output:
For each issue return severity, evidence and recommended fix.

Validation:
Base every finding on the supplied code.
State when evidence is insufficient.
```

## Prompt review checklist

- Is the task clear?
- Is important context included?
- Are boundaries explicit?
- Is the output format clear?
- Are examples needed?
- Is irrelevant context removed?
- Does the model need tools?
- Does it know when to act?
- Is there a way to validate the result?
- Has the prompt been tested on multiple examples?

## Use few-shot examples when

- classification boundaries are difficult
- formatting must be consistent
- tone matters
- behavior is easier to demonstrate than explain

## Consider prompt chaining when

- intermediate results need approval
- stages have different evaluation criteria
- the workflow must be auditable

## Agentic task checklist

Add:

- goal
- scope
- prohibited actions
- tools
- verification
- completion criteria
- escalation conditions

## Model migration checklist

Re-test:

- answer quality
- response length
- reasoning effort
- token usage
- tool calls
- scope adherence
- formatting
- subagent behavior
- latency
- cost

## Final rule

> Prompt engineering is an engineering activity. Define success, test behavior and version important prompts.
