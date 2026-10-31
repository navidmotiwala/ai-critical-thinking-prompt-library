# Practical Response Command Library

These are short instructions to add to an existing prompt. They are reusable modifiers, not guaranteed system-level commands. Combine only those relevant to your task.

## Accuracy and Evidence

| Modifier | Add to your prompt |
| --- | --- |
| Evidence first | Ground each important claim in evidence available to you. |
| Source audit | Distinguish primary sources, secondary reporting, and unsupported claims. |
| No fabricated citations | Do not invent URLs, quotations, statistics, or references. |
| Explicit uncertainty | Label unverifiable conclusions as uncertain instead of guessing. |
| Fact versus inference | Separate directly observed facts from interpretation. |
| Date-aware | Flag claims that require current verification or depend on a stated date. |
| Recalculate | Show calculations, units, denominators, and rounding. |
| Counterevidence | Include the strongest relevant evidence against the conclusion. |
| Falsifiable | Explain what evidence would show the conclusion is wrong. |
| Verify before certainty | Do not label a suspected defect as confirmed without a reproducible test. |

## Reasoning and Critical Thinking

| Modifier | Add to your prompt |
| --- | --- |
| No sycophancy | Do not agree simply because the user favors a position. |
| Independent judgment | Evaluate the idea using its merits, not the author's preference. |
| Steelman objections | State the strongest credible counterargument fairly. |
| Assumption audit | Identify hidden assumptions and their impact if false. |
| Logic audit | Flag invalid inference, circular reasoning, and misleading causality. |
| Failure modes | Find realistic ways the plan could fail and propose safeguards. |
| Tradeoff analysis | Evaluate benefits, costs, reversibility, and opportunity cost. |
| Alternative hypotheses | Consider plausible competing explanations. |
| Prioritize | Rank findings by evidence, severity, probability, and impact. |
| No forced balance | Do not assign equal weight to unequal evidence. |

## Style and Format

| Modifier | Add to your prompt |
| --- | --- |
| No fluff | Remove generic introductions, praise, and unnecessary conclusions. |
| Direct answer | Give the answer first, followed by essential support. |
| Plain English | Use simple words and explain necessary technical terms. |
| No em dash | Do not use em dashes. |
| No emoji | Avoid emojis and decorative symbols. |
| No AI phrases | Avoid formulaic transitions, exaggerated adjectives, and generic enthusiasm. |
| No repetition | Consolidate overlapping points without losing detail. |
| Concrete examples | Demonstrate advice using realistic situations. |
| Actionable output | Recommend a specific next step and a verification method. |
| Explicit limitations | State important omissions, uncertainty, and unavailable evidence. |

## Ready-to-Use Combinations

### 1. Strict Fact Checker

> Verify the claims in [content]. Evidence first. No fabricated citations. Separate facts from inference. Recalculate numbers. Flag claims requiring current verification. Output verified, unverified, contradicted, and unknown findings.

### 2. Independent Critical Reviewer

> Evaluate [idea]. No sycophancy. Independent judgment. Strongest counterarguments. Assumption audit. No forced balance. Rank findings by impact and explain what would change the conclusion.

### 3. Flaw Finder and Repair Planner

> Review [plan or system]. Identify real weaknesses, missing requirements, dependencies, and plausible failure modes. Separate confirmed problems from hypotheses. For each issue give evidence, severity, repair, and validation test.

### 4. Plain-Language Expert

> Explain [topic] directly in simple English with practical examples. No fluff, emojis, em dashes, AI phrases, or repeated ideas. State any important limitations.

### 5. Decision Audit

> Compare [options] using outcomes, evidence quality, assumptions, costs, risks, reversibility, and opportunity cost. Give a recommendation, strongest objection, and test that could change the decision.

### 6. Research Integrity Check

> Audit [research] for selection bias, confounding, missing data, sample limitations, causal overclaims, and selective reporting. Identify what can and cannot be concluded.

### 7. Implementation Review

> Review [technical implementation] for correctness, edge cases, security controls, operational failures, and missing tests. Do not invent vulnerabilities. Recommend defensive repairs and verification steps.

### 8. SEO and AI Search Audit

> Audit [page or report] for current facts, user intent, technical accessibility, crawl and indexability issues, misleading SEO claims, AI-search assumptions, and weak measurement. Separate observed defects from optimization hypotheses.

## Rules for Combining

- Use three to six modifiers when possible, not every instruction at once.
- Do not add contradictory commands such as "no explanation" and "explain every step".
- Prefer one explicit output structure rather than multiple competing formats.
- High-stakes tasks still require current authoritative evidence and domain expertise.
