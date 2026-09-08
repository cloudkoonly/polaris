---
title: "AI-First Is a Discipline, Not a Slogan"
date: 2026-09-08
slug: "ai-first-is-a-discipline"
tags: ["ai-first", "strategy", "engineering-culture", "leadership"]
status: "published"
excerpt: "Every second board deck now calls its company AI-first. The label is cheap; the operating discipline is not. Here is what AI-first actually means, why it matters for companies that are not AI companies, and how to do it well."
---

Somewhere between the launch of ChatGPT and the last earnings call, "AI-first" stopped being a technical statement and became a costume. Companies that sell washing machines, insurance and accounting services now describe themselves as AI-first, often without a single model in production. The phrase is nearly free. The operating discipline behind it is not. This post is about the discipline: what AI-first should mean, why it matters for ordinary companies, and what it looks like when it is done honestly.

## What "AI-first" should mean

An AI-first company is not a company that mentions AI a lot. It is a company where intelligence is treated as a design material — considered at the beginning of a product or process decision, evaluated with the same rigor as any other engineering choice, and used only where it demonstrably helps.

Three features separate real AI-first practice from decoration:

1. **It starts with work, not with models.** The unit of analysis is a job to be done — a support ticket, a sales follow-up, an underwriting review — and the question is whether a model changes its cost, speed or quality.
2. **It has evidence loops.** Claims about AI value are tested against baseline data, not against demos.
3. **It keeps humans accountable.** Models recommend, draft and automate; people decide, approve and answer for the result.

None of these require an AI product to sell. They require a management system that treats AI as ordinary infrastructure with unusual properties.

## The stakes are no longer hypothetical

It is easy to dismiss AI as hype if you only read marketing. The evidence from ordinary work is harder to wave away.

- **Adoption moved faster than any prior technology.** ChatGPT reached roughly 100 million users within two months of launch in 2023 — the fastest consumer adoption on record. Usage is not proof of business value, but it reset what customers expect software to do.
- **Software development changed measurably.** In a 2023 randomized experiment at GitHub, developers using GitHub Copilot completed a task 55.8% faster than a control group (arXiv:2302.06590). Coding was the first knowledge-work category where the productivity effect was measured in a controlled study rather than asserted.
- **Customer support changed measurably.** A 2023 study of a customer-support tool (Brynjolfsson, Li & Raymond, NBER working paper 31161) found a generative AI assistant raised resolved-issues-per-hour by about 14% on average — and by roughly 34% for the least-experienced workers. The important detail is who gained most: the model compressed the learning curve, not just the typing.
- **Capital followed.** Microsoft reported its AI business passed a $10 billion annual revenue run rate in 2024 — which it described as the fastest business in company history to reach that scale — and the largest technology companies guided to tens of billions in annual AI-related capital expenditure in 2025. Whatever you think of the bubble question, the budgets are real.

These are not science-fiction numbers. They are productivity and cost effects measured inside ordinary support and engineering work. For a company that is not an AI company, the strategic question is therefore not "should we build an AI product?" It is: "will our cost curve, response quality and speed keep up with competitors who restructure the same kind of work we do?"

## Why most "AI-first" initiatives fail

The usual failure is not technical. It is organizational, and it follows a recognizable pattern:

1. Buy subscriptions, add a chatbot to the website, declare victory. Nothing else changes.
2. Run a pilot everywhere, measure nowhere. Without a baseline and a metric, a pilot is a demo with a deadline.
3. Confuse model procurement with strategy. The choice of vendor becomes the whole conversation, while the actual work the model should improve is never redesigned.
4. No owner, no budget line. AI work lives in a slide deck owned by no department and starves in the gap between IT, product and operations.
5. Fear of looking behind leads to claiming credit for capabilities that are not in production.

The common thread is treating AI as a purchase rather than a change in how work is done. That is why "AI theater" — impressive slides, nothing in production — is so common, and why it is so cheap to produce.

## How to do AI-first well

The following is not a recipe with five steps to transformation. It is a set of operating habits that we have seen survive contact with real budgets.

### 1. Choose the work before choosing the model

Pick tasks that are frequent, costly, and full of judgment — triage, drafting, summarization, routing, first-pass review. Define the metric before building anything: handle time, cost per ticket, defect rate, conversion. Measure the baseline first. If you cannot name the metric, you are not ready to start; if the model cannot plausibly move it, pick another task.

### 2. Treat models as interchangeable parts

Frontier models are improving quickly, and prices are falling faster than most companies update their plans. Act accordingly:

- Isolate model calls behind a small internal interface so swapping vendors is a configuration change, not a rewrite.
- Benchmark on your own task samples, not on leaderboards that measure something else.
- Re-run the benchmark on a schedule; last year's best model may be this year's second choice.
- Consider small or open models where data rules, latency or cost matter; the frontier is not always the right answer.

Vendor lock-in is a choice you can simply decline to make.

### 3. Redesign the loop, not just the interface

The largest gains come from changing how humans and models divide work, not from replacing a form with a chat window. Decide where the model drafts and where a human approves; set confidence thresholds; design escalation paths. The person responsible for the outcome should be identifiable at every step — for legal, regulatory and practical reasons, someone must answer for results that a model cannot be held accountable for.

### 4. Invest in data and evaluation plumbing

Models improve quickly, but your ability to know whether they are improving *for you* must improve faster. That means logging every production call with outcome labels, building golden sets from real usage, capturing user feedback where it exists, and keeping a small team that owns evaluation. Most failed AI projects fail here: they can demo, but they cannot measure.

### 5. Engineer for probabilistic failure

A model is a junior colleague who is fast, confident and occasionally wrong. Build for that:

- Validate outputs against schemas where possible.
- Add fallbacks and retries; never let a model failure take down a workflow.
- Watch cost and latency per call as carefully as error rates.
- Set budgets and alerts; model spend compounds faster than expected.

Treat wrong answers as an incident class to be designed against, not a surprise to be discovered.

### 6. Organize for it

Give AI work a single owner with a real budget. Keep the core team small. Embed it with the business units where the work actually happens. Raise the floor of AI literacy across the company — including executives, who should be able to tell a benchmark from a demo. Review progress quarterly against business metrics, and be honest in public reports about what did not work. The companies that earn trust with AI are the ones that report failures as routinely as successes.

## What good looks like

Seen from the outside, an AI-first company is almost boring. The AI is not in the press release; it is in the workflow. Support response times fall without quality complaints rising. Developers ship more of their time doing design rather than boilerplate. Underwriting, sales qualification or document review show unit-cost curves trending down quarter after quarter, backed by eval reports an outsider could audit.

The companies that win with AI will not be the ones with the best slogan. They will be the ones with the best feedback loop: a clear problem, a measured baseline, a model in the loop with a human accountable, and the discipline to keep iterating when the first attempt underdelivers. AI-first is not a statement about your company's ambition. It is a statement about your company's operating system — and that is a claim you have to earn with evidence.
