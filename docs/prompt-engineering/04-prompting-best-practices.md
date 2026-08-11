# Prompting Best Practices

**Read time:** 8 minutes  
**Audience:** Everyone

## 1. Be specific about the task

Weak:

```text
Improve this code.
```

Better:

```text
Refactor this method to reduce duplication without changing external behavior.
```

## 2. Provide relevant context

Include the files, requirements, terminology or examples the model needs.

Avoid dumping unrelated material into the prompt.

## 3. State constraints explicitly

Examples:

```text
Do not add dependencies.
Do not change database schema.
Use BigDecimal for monetary values.
Do not log account numbers.
```

## 4. Define the output

Example:

```text
Return:
1. Root cause
2. Evidence
3. Proposed fix
4. Regression tests
```

## 5. Use examples for important patterns

Examples are useful when style or classification behavior is difficult to describe precisely.

## 6. Break large tasks into smaller tasks

Instead of:

```text
Modernize this service.
```

Use:

```text
1. Explain the current architecture.
2. Identify the top three risks.
3. Propose modernization options.
4. Compare trade-offs.
5. Implement only the selected option.
```

## 7. Ask for assumptions

```text
List any assumptions you need to make before proposing the solution.
```

This helps expose missing requirements.

## 8. Ask for evidence rather than confidence

Weak:

```text
Are you sure this is correct?
```

Better:

```text
Identify the code, documentation or test evidence supporting each conclusion.
```

## 9. Separate instructions from data

Use headings, code fences or tags.

````text
## Instructions
Review for SQL injection.

## Code
```java
...
```
````

## 10. Iterate deliberately

If the answer is weak, identify why:

- Missing context?
- Ambiguous task?
- Wrong assumptions?
- Poor output format?
- Model capability?

Do not endlessly add words to the prompt without understanding the failure.

## Further reading

- https://developers.openai.com/api/docs/guides/prompt-engineering
- https://ai.google.dev/gemini-api/docs/prompting-strategies
- https://docs.anthropic.com/en/docs/build-with-claude/prompt-engineering/overview
