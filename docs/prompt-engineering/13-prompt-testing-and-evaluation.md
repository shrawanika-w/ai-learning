# Prompt Testing and Evaluation

**Read time:** 8 minutes  
**Audience:** Developers and AI Leads

## Why testing matters

LLM output is probabilistic. Manual testing with two or three prompts is not enough for an important workflow.

## Build an evaluation set

Include representative cases:

```text
Happy path
Boundary case
Missing information
Ambiguous request
Incorrect input
Long input
Rare scenario
Adversarial input
```

For a code-review prompt include both clean code and code containing known defects.

## Define expected behavior

Possible criteria:

- Correctness
- Completeness
- Relevance
- Required format
- Security-policy compliance
- Groundedness
- Citation accuracy
- Hallucination rate
- Latency
- Token usage
- Cost

## Example evaluation case

```yaml
case: duplicate-payment-risk
input: kafka-consumer-v2.java
expected:
  must_identify:
    - missing idempotency control
  must_not_recommend:
    - in-memory lock as cross-pod solution
```

## Compare versions

```text
Prompt v1 ─┐
           ├─ Same evaluation dataset → Compare results
Prompt v2 ─┘
```

Do not change the test set between versions when making a direct comparison.

## Automated and human evaluation

Use both where appropriate.

Automated checks can validate:

- JSON schema
- Required fields
- Keywords
- Classification labels
- Deterministic rules

Human reviewers are useful for:

- Technical quality
- Helpfulness
- Nuanced correctness
- Architecture judgement

## Regression testing

When a prompt changes rerun old successful cases.

A new prompt may improve one scenario while breaking another.

## Production feedback loop

```text
Observed failure
      ↓
Add evaluation case
      ↓
Improve prompt or system
      ↓
Run regression suite
      ↓
Release
```

## Key lesson

> Prompt engineering without evaluation is guesswork.

## Further reading

- https://developers.openai.com/api/docs/guides/evaluation-best-practices
- https://developers.openai.com/api/docs/guides/model-optimization
