---
title: "The Real Cost of AI-First"
date: 2026-09-08
slug: "the-real-cost-of-ai-first"
tags: ["ai-first", "costs", "strategy", "operations"]
status: "published"
excerpt: "Inference is the cheapest line item. The bill for AI-first is mostly evaluation, review, maintenance and compliance — and most budgets miss it. Here is the arithmetic that decides whether an AI feature is worth building."
---

The first AI feature a company ships is usually cheap. An API key, a prototype, a demo that lands well in a leadership meeting. The second year is where the money goes — and it is rarely the money anyone planned for.

## The invoice is not the inference bill

Model calls are the most visible cost and, increasingly, the least important one. Prices for a given level of capability have fallen by roughly an order of magnitude per year for the last three years, and competitive pressure keeps pushing them down. Meanwhile the costs that surround the model call are stable or rising:

- **Evaluation and data plumbing.** Logging every interaction with outcome labels, maintaining golden sets, and building regression gates. Without this you cannot tell improvement from noise — and you will pay for it in shipped regressions instead.
- **Human review and escalation.** Wherever a wrong answer is expensive, a person has to check the output. That labour is not free, and it does not shrink just because the model got better; it moves.
- **Maintenance across model churn.** Providers retire model versions, change defaults and deprecate parameters. Every one of those events triggers re-testing, prompt adjustments and sometimes a re-qualification of the whole feature.
- **Compliance and security review.** Data residency, retention, subprocessor lists, DPAs, and now AI-specific questions from customers and app stores. This work is one-off per feature, but it recurs per vendor and per jurisdiction.
- **Support for probabilistic software.** Users report things that are hard to reproduce because the answer differs each time. Support tooling and playbooks have to be rewritten for that reality.
- **Failure cost.** A hallucinated price, a wrong summary in a contract review, an offensive output shown to a customer. You may never see these in a cost model, but they are the reason several AI features were quietly withdrawn.

None of these lines show up in a "cost per million tokens" comparison, which is exactly why they are easy to miss.

## What the evidence says about payoff

The payoff distribution is not even. Two kinds of evidence coexist in the same market.

On one side, controlled measurement shows real gains in narrow, high-volume work: a 2023 GitHub randomized experiment found developers finished a task 55.8% faster with an AI assistant (arXiv:2302.06590), and a study of customer-support tooling found resolved issues per hour up about 14% on average, with roughly 34% for the least-experienced workers (Brynjolfsson, Li & Raymond, NBER working paper 31161).

On the other side, portfolio-level results are poor. A 2025 MIT study of enterprise generative-AI pilots reported that the large majority produced no measurable profit-and-loss impact, and a 2024 S&P Global survey found a large share of companies had abandoned most of their AI initiatives. Both findings should be read as approximations of a messy reality rather than precise measurements — but they point the same way.

The reconciliation is not complicated. Gains appear where a workflow has a measurable metric, enough volume to matter, and an output that a person can check quickly. Losses cluster where the metric was never defined, volume was low, or the feature was built because it was possible rather than because someone was accountable for the result.

## The arithmetic that decides it

Before building, write three numbers down:

1. **Cost per task** with the model, including retries, review labour and amortised maintenance.
2. **Cost per task today**, all in — salary, tooling, error correction.
3. **Cost of being wrong**, and whether a human review step bounds it.

An AI feature is defensible when the first number is meaningfully below the second after review costs are included, the third is bounded by a process you actually operate, and volume is high enough that the difference compounds. If the third number is unbounded — a decision that can injure someone, breach a regulation, or destroy a relationship — then the review step is not optional and must be priced in from the beginning.

Two consequences follow. First, some of the best AI projects are small: they replace a narrow, repetitive, high-volume task. Second, some features should be refused. That is not an anti-AI position; it is what a budget does.

## Where AI is simply the wrong tool

- **Deterministic logic.** Tax calculation, eligibility rules, inventory arithmetic. Rules are cheaper, faster, auditable and stable. Adding a model makes them worse, not modern.
- **Low volume.** If a task runs fifty times a month, the fixed cost of an eval set, a review process and a maintenance owner will never be repaid.
- **Bad inputs.** If the underlying data is incomplete or the process is undefined, a model will produce confident nonsense at scale. Fix the data first; the model has nothing to work with.
- **Unbounded error cost without review.** Where a person must approve every output anyway, ask honestly whether the model saved anything at all, or just moved the work.

## Budgeting it honestly

Three habits separate teams that get value from teams that get invoices.

**Set a ceiling before you build.** A maximum cost per successful task, and a volume assumption. If the feature cannot beat the ceiling at that volume, it does not ship — no matter how good the demo was.

**Track cost per successful outcome, not cost per call.** A cheap model that fails a third of the time is expensive. A capable model used only for the hard 20% of cases, with a small model handling the rest, is usually the cheapest architecture available.

**Write the kill criterion in advance.** "If quality does not reach X on our eval set by date Y, we stop." Almost every AI initiative that becomes a permanent cost centre began as a pilot that nobody was empowered to end.

Prices will keep falling, and that helps — but cheaper inference does not reduce review labour, maintenance or the cost of a wrong answer. AI-first is not a decision to use AI everywhere. It is the discipline of finding the places where the numbers genuinely work, and having the nerve to say so when they do not.

*Related: [AI-First Is a Discipline, Not a Slogan](/blog/ai-first-is-a-discipline).*
