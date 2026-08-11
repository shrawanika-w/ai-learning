# Prompt Engineering Overview

## What is prompt engineering?

Prompt engineering is the practice of improving the instructions and context given to an AI model so that its output better meets your goal.

## Before improving a prompt

Start with three things:

1. **Success criteria** - What does a good answer look like?
2. **Evaluation method** - How will you check whether the answer is good?
3. **First draft prompt** - You need something concrete to improve.

Without these, prompt tuning becomes guesswork.

## Not every problem is a prompt problem

| Problem                   | Better lever                                |
| ------------------------- | ------------------------------------------- |
| High latency              | Faster model or less work                   |
| High cost                 | Cheaper model, lower effort or less context |
| Missing current knowledge | Retrieval or tools                          |
| Wrong source data         | Fix the source or retrieval                 |
| Inconsistent output       | Better examples, structure and evaluation   |
| Model lacks capability    | Stronger model                              |

## A practical cycle

```text
Define success
     ↓
Write prompt
     ↓
Test
     ↓
Review failures
     ↓
Change one thing
     ↓
Re-test
```

## Key lesson

> Improve prompts against clear success criteria, not intuition alone.

## Source

https://platform.claude.com/docs/en/build-with-claude/prompt-engineering/overview
