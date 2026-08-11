# 10 - Prompt Anti-Patterns

**Read time:** 8 minutes  
**Audience:** Everyone

## 1. Vague request

```text
Fix this.
```

The model must guess what "fix" means.

Better: state the defect or goal.

## 2. Context dumping

Providing dozens of unrelated files can reduce focus.

Better: include the smallest useful context set.

## 3. Conflicting instructions

```text
Be extremely concise.
Explain every detail thoroughly.
```

Resolve conflicts before sending.

## 4. Leading the model

```text
Explain why this design is secure.
```

This encourages confirmation.

Better:

```text
Review this design for security weaknesses and provide evidence.
```

## 5. Asking the model to invent missing requirements

```text
Implement our company's refund policy.
```

If the policy is not provided or retrievable the model may guess.

## 6. Trusting fabricated APIs

Generated method and configuration names can look convincing but may not exist.

Verify APIs against the repository or official documentation.

## 7. One giant prompt

A single request to analyze, redesign, implement, migrate and test an application makes review difficult.

Use decomposition.

## 8. Infinite prompt polishing

If ten prompt rewrites still fail, the issue may be:

- Missing knowledge
- Wrong model
- Need for a tool
- Need for retrieval
- Need for deterministic code
- Poor source data

## 9. Using generated tests as independent proof

The same model may repeat the same misunderstanding in implementation and tests.

Use requirement-based tests and human review.

## 10. Stale chat history

Old context can continue influencing current answers.

Start fresh when necessary.

## 11. Persona inflation

```text
You are the world's greatest architect with 100 years of experience.
```

This does not provide missing project knowledge.

## 12. Asking for certainty instead of evidence

```text
Are you 100% sure?
```

Better:

```text
What evidence supports the conclusion and what remains uncertain?
```

## Remember

A polished response can still be wrong.
