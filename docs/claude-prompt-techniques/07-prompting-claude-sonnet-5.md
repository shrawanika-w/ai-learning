# Prompting Claude Sonnet 5

Claude Sonnet 5 is particularly strong in coding and agentic tasks.

## 1. Control response length explicitly

```text
Give a concise answer with a recommendation and at most three supporting points.
```

Positive examples of the desired style can be more useful than only listing what not to do.

## 2. Calibrate effort

A practical guide:

- **low** - short, simple, latency-sensitive work
- **medium** - cost-sensitive work with moderate reasoning
- **high** - general default for demanding work
- **xhigh** - hardest coding and agentic tasks

Benchmark with your own workload.

## 3. Adaptive thinking is on by default

Sonnet 5 uses adaptive thinking by default.

Because thinking consumes output capacity, re-check `max_tokens` when migrating applications.

## 4. Tool use is proactive

Sonnet 5 is more likely to use tools and self-verification.

If thinking is disabled and tool use is required, state it:

```text
Use web search to verify current framework behavior before answering.
```

## 5. Instructions are followed literally

Weak:

```text
Use this format.
```

Better:

```text
Use this format for every section of the response.
```

## 6. Prompt for tone

Use system instructions when a particular voice is required.

```text
Use a professional, collaborative tone.
Keep explanations technically precise and concise.
```

## 7. For design work, ask for options first

```text
Propose four clearly different visual directions.
Give a one-line rationale for each.
Do not build until one direction is selected.
```

## Key lesson

> Sonnet 5 responds well to explicit scope, calibrated effort and clear tool instructions.

## Source

https://platform.claude.com/docs/en/build-with-claude/prompt-engineering/prompting-claude-sonnet-5
