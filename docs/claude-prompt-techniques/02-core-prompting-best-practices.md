# Core Prompting Best Practices

## 1. Be clear and direct

Weak:

```text
Review this code.
```

Better:

```text
Review this Java service for correctness, security and missing edge cases.
Return findings as High, Medium or Low severity.
Do not rewrite the code.
```

A useful test:

> Could a capable colleague follow the prompt without asking what you meant?

## 2. Give useful context

```text
This API handles payment authorization.
Incorrect retry behavior could create duplicate processing.
Review the retry logic with that risk in mind.
```

## 3. State the required output

```text
Return:
1. Finding
2. Severity
3. Evidence
4. Recommended fix
```

## 4. Prefer positive instructions

Instead of:

```text
Do not be verbose.
```

Try:

```text
Give a concise answer with at most five bullets.
```

## 5. Use numbered steps when order matters

```text
1. Read the requirement.
2. Identify assumptions.
3. Review the implementation.
4. List gaps.
5. Suggest the smallest safe change.
```

## 6. Give an appropriate role

```text
You are reviewing code as a senior Java engineer responsible for payment reliability.
```

A role focuses perspective. It does not provide missing business knowledge.

## 7. Say whether you want advice or action

```text
Implement the change and update the tests.
```

is different from:

```text
Suggest how this could be changed.
```

## Key lesson

> Good prompts reduce ambiguity. They do not need to be long.

## Source

https://platform.claude.com/docs/en/build-with-claude/prompt-engineering/claude-prompting-best-practices
