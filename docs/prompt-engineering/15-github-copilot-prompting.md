# 15 - GitHub Copilot Prompting

**Read time:** 8 minutes  
**Audience:** GitHub Copilot users

## Copilot quality depends on context

When working in an IDE the useful context can include:

- Current file
- Selected code
- Open files
- Repository content
- Conversation history
- Custom instructions
- Prompt files
- Explicitly referenced files

The exact context depends on the Copilot feature and environment.

## Start with a focused task

Weak:

```text
Fix the application.
```

Better:

```text
Review PaymentService.processPayment() for duplicate-processing risk.
Do not modify code yet.
Identify the failure scenario and evidence first.
```

## Open relevant files

If a change depends on interfaces, services, tests or configuration make those artifacts easy for Copilot to access.

Close or avoid irrelevant context where practical.

## Use iterative prompting

A useful coding workflow is:

```text
Understand → Plan → Implement → Test → Review
```

Example:

```text
Explain how PaymentController, PaymentService and PaymentRepository interact.
Do not propose changes yet.
```

Then:

```text
Identify where idempotency should be enforced and explain why.
```

Then implement after the approach is understood.

## Use repository custom instructions

Repeated project rules should not be manually pasted into every chat.

Example location:

```text
.github/copilot-instructions.md
```

Examples of useful instructions:

```text
- Use Java 21.
- Use BigDecimal for monetary values.
- Do not log complete account numbers.
- Controllers must not call repositories directly.
- Run unit tests before considering a task complete.
```

## Use prompt files for repeatable tasks

Example:

```text
.github/prompts/
  code-review.prompt.md
  generate-tests.prompt.md
  explain-service.prompt.md
```

A prompt file represents a reusable task. Custom instructions represent persistent project guidance.

## Prompt vs instruction

```text
Prompt
"Review this service for duplicate processing."

Repository instruction
"All event consumers must implement idempotent processing."
```

## Keep conversations relevant

Start a new conversation when earlier history is no longer useful or contains stale assumptions.

## Always validate

Copilot suggestions should go through normal engineering controls:

- Code review
- Compilation
- Tests
- Security scanning
- Architecture checks
- CI/CD quality gates

## Further reading

- https://docs.github.com/en/copilot/get-started/best-practices
- https://docs.github.com/en/copilot/how-tos/provide-context
- https://docs.github.com/en/copilot/customizing-copilot/adding-custom-instructions-for-github-copilot
- https://docs.github.com/en/copilot/tutorials/customization-library/prompt-files/your-first-prompt-file
