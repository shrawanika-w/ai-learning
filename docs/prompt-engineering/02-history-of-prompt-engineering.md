# 02 - A Short History of Prompt Engineering

**Read time:** 7 minutes  
**Audience:** Everyone

## Why it matters

Prompting practices have changed as models have become more capable. Techniques that were useful for an older model may be unnecessary or less effective with newer reasoning models.

## Simplified evolution

```text
Text completion
      ↓
Zero-shot instructions
      ↓
Few-shot examples
      ↓
Instruction-tuned chat models
      ↓
System and user messages
      ↓
Chain-of-thought research
      ↓
RAG and grounding
      ↓
Tool and function calling
      ↓
Structured outputs
      ↓
Reusable instructions and prompt files
      ↓
Reasoning models
      ↓
Context engineering and agents
```

## Early completion models

Early language models mainly continued text. Users learned that examples and carefully phrased prefixes could strongly influence output.

## Instruction prompting

Instruction-tuned models became better at requests such as:

```text
Summarize this document in five bullets.
```

This made zero-shot prompting more useful.

## Few-shot prompting

Examples became a powerful way to show expected behavior.

```text
Input: Timeout calling fraud service
Output: Reliability

Input: SQL built by string concatenation
Output: Security

Input: CPU usage above 95%
Output:
```

## Chain-of-thought era

Research showed that step-by-step reasoning prompts could improve some tasks for some model families.

Do not turn this into a universal rule. Modern reasoning models often work best with simple direct instructions and may reason internally without needing prompts such as "show every step".

## RAG, tools and structured outputs

Prompt quality alone cannot solve every problem.

Modern applications increasingly use:

- Retrieval for external knowledge
- Tools for actions and live data
- Structured outputs for machine-readable responses
- Evaluations for quality measurement
- Persistent instructions for repeatable behavior

## Context engineering

The focus is shifting from:

```text
How do I write the perfect prompt?
```

To:

```text
What information, rules, tools and validation does the model need for this task?
```

## Key lesson

Prompt engineering is evolving from wording optimization into AI workflow engineering.

## Further reading

- https://developers.openai.com/api/docs/guides/reasoning-best-practices
- https://docs.anthropic.com/en/docs/build-with-claude/prompt-engineering/overview
- https://ai.google.dev/gemini-api/docs/prompting-strategies
