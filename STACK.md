# A Genuinely Free AI Stack

*Production-grade. Unattended. Zero cost.*

---

Every "free AI" product announced in the last two years has a ceiling, a credit card field, or a pivot to paid buried in the terms. This is a working production stack — pipelines that run on a VPS overnight, unattended, generating content at scale — with zero API spend on the LLM layer.

This is not a list of free trials.

## The stack

| Provider | Free Tier | Best for |
|----------|-----------|---------|
| **Gemini Flash** (Google) | Generous daily limits, no card | Bulk work: ingestion, tagging, classification, content at scale |
| **Groq** | Free tier, rate-limited | Ultra-fast inference: real-time classification, quick ops |
| **OpenRouter** | 29 free models, 200 req/day | Model variety: route to Llama 4, DeepSeek R1, Qwen3, Mistral, Gemma by task |

These three cover every unattended pipeline task. Nothing else is needed.

## The 29 free models on OpenRouter

OpenRouter maintains a free tier that routes across models from Meta, Google, Mistral, DeepSeek, NVIDIA, Alibaba, and others. Key models as of early 2026:

-  — strong general reasoning, reliable tool calling (1M context)
-  — fast, efficient (512k context)
-  — chain-of-thought reasoning (164k context)
-  — coding and analysis (128k context)
-  — large-scale reasoning (128k context)
-  — instruction following, multilingual (128k context)
-  — Google-tuned general use (128k context)
-  — long-context tasks (262k context)
-  — auto-router: picks the best available free model for your request (200k context)

Rate limits: 200 requests/day, 20/minute. Enough for most pipelines.

## How to use it

All three APIs are OpenAI-compatible. Drop-in setup:



No billing setup. No credit card. No trial clock.

## The routing logic

Not every task needs the same model. The hierarchy I use in production:

1. **Gemini Flash** — first choice for all bulk/unattended work. Highest free limits.
2. **Groq** — when latency matters (real-time ops, user-facing classification).
3. **OpenRouter free** — when you want model variety, longer context, or a reasoning-capable model without paying for it.

Paid APIs (DeepSeek, OpenAI, Anthropic) exist in the stack but are reserved for specific protected pipelines. The free tier handles everything else.

## Why this matters

The narrative around AI costs assumes a paid API is the baseline. It is not. A developer who understands model routing can build production pipelines — real ones, running continuously, generating real output — at zero LLM cost.

This stack runs [Tarotsmith](https://tarotsmith.net), a multi-agent article pipeline, a morning brief system, a property listing video generator, and several other projects. All unattended. All free on the LLM layer.

The infrastructure argument for AI being expensive is, at present, a choice — not a technical constraint.

---

*See also: [Free Used to Mean Free](FREE.md)*
