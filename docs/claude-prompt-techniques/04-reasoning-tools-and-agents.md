# Reasoning, Tools and Agentic Prompting

## Reasoning and effort

Current Claude models can use more reasoning for harder tasks.

For many tasks, a general instruction is enough:

```text
Think carefully about the trade-offs before deciding.
```

Avoid forcing a detailed reasoning procedure unless the workflow requires it.

## Use effort as a control

Where supported, `effort` helps trade off:

- intelligence
- latency
- token usage
- cost

Use lower effort for simple work and higher effort for difficult coding or agentic tasks.

## Make tool requirements explicit

```text
Use repository search to verify whether this API already exists before proposing a new implementation.
```

A vague request may produce advice instead of action.

## Parallel versus sequential tools

Use parallel calls for independent work such as reading unrelated files.

Use sequential calls when later operations depend on earlier results.

## Agentic tasks need boundaries

Define:

- goal
- allowed scope
- prohibited actions
- tools
- verification
- completion criteria
- escalation conditions

Example:

```text
Implement only the requested feature.
Do not refactor unrelated modules.
Run the existing tests.
Report failing tests clearly.
Ask before destructive or irreversible actions.
```

## Ground progress claims

```text
Only report a step as complete when a tool result, test or observable output verifies it.
```

## Prompt chaining

Use separate stages when intermediate output must be inspected or approved.

```text
Draft
  ↓
Review against criteria
  ↓
Revise
```

## Avoid overengineering

```text
Make the minimum change required.
Do not create new abstractions or dependencies unless necessary.
```

## Key lesson

> Agentic prompting is mainly about goals, boundaries, tools, evidence and completion criteria.

## Source

https://platform.claude.com/docs/en/build-with-claude/prompt-engineering/claude-prompting-best-practices
