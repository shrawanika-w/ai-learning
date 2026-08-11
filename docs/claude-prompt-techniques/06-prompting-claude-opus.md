# Prompting Claude Opus 5 and Opus 4.8

## Claude Opus 5

Opus 5 is aimed at complex coding and enterprise agentic work.

### Give the complete task

It is well suited to:

- multi-file features
- large refactors
- end-to-end implementation
- code review
- long-running agentic work

### Control verbosity explicitly

Effort controls reasoning depth, not reliably the visible answer length.

```text
Keep the final response concise.
Lead with the result and include only important supporting details.
```

### Avoid unnecessary verification scaffolding

Opus 5 may verify its work proactively. Old prompts that force repeated verification can waste time and tokens.

### Constrain narrow tasks

```text
Change only the retry behavior.
Do not refactor adjacent code or introduce new dependencies.
```

### Code review tip

Avoid filtering too early.

Instead of asking for only severe findings, first find relevant issues and prioritize them afterward.

---

## Claude Opus 4.8

### Effort matters

Use lower effort for short scoped tasks and higher effort for difficult reasoning or agentic coding.

### Thinking behavior differs

Opus 4.8 does not use adaptive thinking unless it is enabled. Newer models can have different defaults.

### Instructions are literal

```text
Apply this validation rule to every endpoint in this module, not only the first endpoint.
```

### Be explicit about tools and subagents

Say when tool use or delegation is expected.

## Migration checklist

Re-test:

- verbosity
- effort
- thinking behavior
- tool use
- verification
- scope
- subagents
- style

## Key lesson

> Treat prompt version and model version as a pair.

## Sources

- https://platform.claude.com/docs/en/build-with-claude/prompt-engineering/prompting-claude-opus-5
- https://platform.claude.com/docs/en/build-with-claude/prompt-engineering/prompting-claude-opus-4-8
