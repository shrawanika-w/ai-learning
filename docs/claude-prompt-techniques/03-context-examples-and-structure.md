# Context, Examples and Prompt Structure

## Use examples when words are not enough

### Zero-shot

No example is provided.

```text
Classify this incident as Critical, High, Medium or Low.
```

### One-shot

One example is provided.

### Few-shot

Several examples are provided.

Good examples should be:

- **Relevant**
- **Diverse**
- **Consistent**

Bad examples can teach bad patterns.

## Structure complex prompts

XML-style tags are useful with Claude:

```xml
<instructions>
Review the transaction for policy violations.
</instructions>

<policy>
...
</policy>

<transaction>
...
</transaction>

<output_format>
Return decision, reason and evidence.
</output_format>
```

The tag names are not magic. Their value is clear separation.

## Long-context prompting

For large documents:

1. Put source material before the final question.
2. Separate documents and metadata clearly.
3. Put the task after the source material.
4. Ask the model to ground conclusions in the supplied content.

Example:

```xml
<documents>
  <document>
    <source>Policy A</source>
    <content>...</content>
  </document>
</documents>

<task>
Identify the requirements that apply to payment retries.
</task>
```

## More context is not always better

Prefer:

**relevant + current + non-conflicting context**

over:

**everything available**

## Key lesson

> The examples and context surrounding an instruction can strongly shape the answer.

## Source

https://platform.claude.com/docs/en/build-with-claude/prompt-engineering/claude-prompting-best-practices
