# Conversation History and the Context Window

**Read time:** 7 minutes  
**Audience:** Developers

## Conversation history is context

In a chat interaction previous user requests and AI responses can influence later output.

Example:

```text
Message 1:
This service uses Java 17.

Message 2:
Generate the implementation.
```

If the project is actually Java 21, the old message may influence the solution until corrected or removed from the working context.

## Context contamination

Long conversations can accumulate:

- Old requirements
- Failed approaches
- Incorrect assumptions
- Irrelevant code
- Contradictory instructions

This can reduce answer quality.

## When to start a new conversation

Consider a fresh conversation when:

- The task has changed substantially
- Earlier assumptions are no longer valid
- Too many failed approaches are in history
- You need an independent review
- The model keeps returning to an outdated idea

## The context window

Models process a limited amount of information in one interaction. Depending on the system this may include:

- System or developer instructions
- User messages
- Previous assistant responses
- Code and files
- Retrieved content
- Tool definitions and results
- The new response being generated

## Why developers should care

Large context can create:

- Higher latency
- Higher token consumption
- Attention dilution
- Less room for new information
- Greater chance of conflicting instructions

## Good practice

For long technical sessions periodically restate the current ground truth:

```text
Current agreed constraints:
- Java 21
- PostgreSQL
- No schema change
- Existing API contract must remain compatible
- Duplicate events are possible
```

## Key lesson

Conversation history is useful working memory but it is not automatically clean, correct or permanent project knowledge.

## Further reading

- https://docs.github.com/en/copilot/get-started/best-practices
- https://docs.github.com/en/copilot/concepts/agents/copilot-cli/context-management
