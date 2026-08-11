# Prompting Claude Fable 5

## What is different?

Claude Fable 5 is designed for difficult, long-running and ambiguous work. Anthropic highlights improvements in long-horizon autonomy, complex implementation, vision, enterprise workflows, debugging and multi-agent collaboration.

## 1. Give the complete outcome and boundaries

For long tasks, explain what success looks like and what must remain unchanged.

## 2. Explain why the task matters

```text
We are preparing this service for a regulated payment environment.
The goal is to reduce duplicate processing without changing the public API.
Review the implementation with that outcome in mind.
```

## 3. Ground progress in evidence

```text
Do not claim a task is complete unless a tool result, test or other evidence verifies it.
If verification failed, report the failure clearly.
```

## 4. Set action boundaries

```text
If I am asking for an assessment, provide the assessment only.
Do not change files unless I explicitly request implementation.
```

Ask for confirmation before destructive actions or real scope changes.

## 5. Use subagents deliberately

Use delegation for meaningful independent work such as:

- architecture review
- test review
- performance analysis

Do not create subagents for trivial tasks.

## 6. Make final communication clear

Ask the final response to:

1. Lead with the outcome.
2. Include only important supporting detail.
3. State unresolved items.
4. Avoid unexplained shorthand.

## 7. Re-test old scaffolding

A stronger model may not need every workaround added for older models.

Remove unnecessary instructions only after evaluation.

## Key lesson

> Focus Fable 5 on outcome, boundaries and evidence rather than micromanaging every reasoning step.

## Source

https://platform.claude.com/docs/en/build-with-claude/prompt-engineering/prompting-claude-fable-5
