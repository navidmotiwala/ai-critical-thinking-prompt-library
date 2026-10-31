# Universal Master Prompt for Critical Thinking, Flaw Detection, and Independent Review

A reusable framework for critically evaluating ideas, claims, plans, research, products, code, decisions, documents, and AI-generated answers.

**Purpose:** Detect actual weaknesses, not manufacture criticism. Identify what works, what fails, what is uncertain, and how to test or improve the result.

**How to use:** Copy the full prompt, replace the placeholders, and attach the material to be assessed. The checks are selective: apply relevant ones and mark the rest as not applicable. This prevents repetitive, irrelevant findings.

## Exact Copy-and-Paste Critical Review Prompt

The following prompt is preserved verbatim as a standalone, ready-to-use template.

```text
Act as an independent critical reviewer. Your job is to find flaws in the material below, not to defend it or agree with it.

Check for factual errors and hallucinations, unsupported claims, logical fallacies, hidden assumptions, bias, contradictions, missing information, blind spots, counterexamples, edge cases, incorrect calculations, false precision, outdated information, alternative explanations, opposing arguments, practical risks, implementation failures, and missing steps or measurement criteria.

Do not assume the material is correct because it sounds convincing. Do not invent flaws merely to satisfy the request. Distinguish confirmed errors from possible weaknesses and subjective disagreements. Verify important factual claims using reliable sources when tools are available. Never fabricate evidence, citations, or verification. Explain why each finding matters and how to fix it. Rank findings as critical, high, medium, or low. State what cannot be verified. If no material flaw is found, say so clearly.

Output: A. Overall assessment. B. Critical and high-severity flaws. C. Other weaknesses and omissions. D. Missing evidence. E. Counterarguments and failure scenarios. F. Recommended corrections. G. Corrected final version.

Material to review:
[PASTE YOUR CONTENT HERE]
```

## 1. Complete Master Prompt

> **Role**
>
> Act as an independent, evidence-driven critical reviewer. Your job is to evaluate the supplied material objectively, identify meaningful flaws, test assumptions, challenge conclusions, and recommend specific corrections.
>
> Do not agree with my position to be polite. Do not disagree merely to appear independent. Reach conclusions according to the evidence and explicitly state uncertainty.
>
> **Material to review:** [Paste or attach the idea, response, report, strategy, code, product specification, decision, argument, or research.]
>
> **Objective:** [What should this material achieve?]
>
> **Intended audience:** [Who will read, use, or act on it?]
>
> **Relevant context:** [Industry, product, market, technical environment, target users, prior decisions, and known facts.]
>
> **Constraints:** [Deadline, budget, format, available data, rules, dependencies, and non-negotiable requirements.]
>
> **Evidence available:** [Links, data, studies, logs, screenshots, documents, or measurements.]
>
> **Decision at stake:** [What action depends on this review?]
>
> **Review depth:** [Quick / Standard / Deep / Adversarial]
>
> **Rules for the review**
>
> 1. Interpret the objective accurately before criticizing the work.
> 2. Distinguish facts, direct observations, assumptions, hypotheses, opinions, and predictions.
> 3. Challenge unsupported statements, including statements I appear to prefer.
> 4. Search for counterevidence and credible alternative explanations.
> 5. Never invent sources, quotes, numbers, test results, defects, or tool access.
> 6. Do not call a risk or possible failure a confirmed vulnerability without supporting evidence.
> 7. Prefer primary and recent evidence when the claim is time-sensitive. State clearly when current verification is unavailable.
> 8. Separate factual errors from preferences, optimization opportunities, and missing information.
> 9. Rank findings by evidence strength, impact, likelihood, and urgency, not by how dramatic they sound.
> 10. Do not repeat the same finding under several names.
> 11. Apply only the review dimensions relevant to the material and explain important exclusions.
> 12. Avoid excessive caveats when a conclusion is well supported.
> 13. Do not give legal, medical, financial, or security conclusions beyond available expertise and evidence. Identify where specialist validation is needed.
>
> **Step 1. Establish the claim and intended outcome**
>
> Summarize the central claim, desired outcome, constraints, and evaluation criteria. Identify material ambiguities or mismatches between the stated goal and the proposed approach. Where information is missing, make narrowly scoped assumptions and label them.
>
> **Step 2. Test factual accuracy and evidence**
>
> Extract important verifiable claims. For each, assess whether the provided material supports it, contradicts it, or leaves it unverified. Check names, dates, quotations, calculations, units, denominators, benchmarks, definitions, links, and source relevance when applicable.
>
> **Step 3. Expose assumptions and reasoning flaws**
>
> Identify hidden premises, unsupported causal claims, logical contradictions, circular reasoning, false dichotomies, selection effects, cherry-picked evidence, survivorship bias, and misleading framing where present. Do not claim a fallacy merely because you disagree with the conclusion.
>
> **Step 4. Consider competing explanations**
>
> Develop the strongest plausible objections and alternative hypotheses. Assess each against the evidence. Identify the counterargument that most threatens the original conclusion and explain why.
>
> **Step 5. Identify weaknesses, failure modes, and blind spots**
>
> Look for missing requirements, neglected stakeholders, conflicting incentives, edge cases, dependencies, unsafe defaults, operational failure, unclear responsibilities, accessibility gaps, privacy risks, technical defects, and unintended second-order effects where relevant.
>
> **Step 6. Stress-test feasibility and tradeoffs**
>
> Evaluate cost, timelines, staffing, capabilities, reversibility, scale, maintenance, opportunity cost, and alternatives. Identify what must be true for the proposal to succeed, what could make it fail, and leading signals of failure.
>
> **Step 7. Assess the quality of the argument and presentation**
>
> Check whether the material is complete, coherent, specific, understandable to the intended audience, and free from redundant or exaggerated claims. Distinguish problems of presentation from problems of substance.
>
> **Step 8. Prioritize and repair**
>
> Group duplicate or dependent issues. For each material finding, provide supporting evidence, an impact assessment, confidence, a concrete correction, and a realistic verification test. Mark uncertain issues as needing investigation.
>
> **Step 9. Seek disconfirming evidence**
>
> State what new observation, experiment, source, or user behavior would most strongly overturn your conclusion. Describe how it could be checked.
>
> **Step 10. Deliver an independent verdict**
>
> Give a direct assessment of what is sound, what is weak, what needs verification, and whether to proceed, revise, test, or stop. Do not make a binary judgment if the evidence only supports a conditional one.
>
> **Output format**
>
> A. Executive verdict: 2 to 4 sentences.
>
> B. Scope and assumptions: what was reviewed and what could not be checked.
>
> C. Finding table with columns: ID, finding, evidence, status, severity, likelihood, impact, fix, verification method.
>
> D. Strongest objections and alternative explanations, with brief responses.
>
> E. Missing evidence and open questions, ordered by decision impact.
>
> F. Recommended action plan: immediate fixes, validation tests, and later improvements.
>
> G. Final judgment: proceed, proceed with conditions, test first, revise, or stop, with rationale and conditions for changing this judgment.
>
> **Style**
>
> Direct, precise, and natural English. No automatic praise, generic introductions, emojis, em dashes, artificial balance, invented certainty, or duplicated points. Use tables only when they improve the review.

## 2. Review Dimensions

Use this matrix to select checks based on the material. Do not force every review category into every task.

| Dimension | Key questions | Useful evidence |
| --- | --- | --- |
| Factual accuracy | Which concrete claims are wrong, outdated, or unsupported? | Primary sources, documents, data |
| Logical consistency | Do premises support conclusions? Do statements contradict? | Argument map, quoted passages |
| Assumptions | What must be true for the outcome to happen? | Assumption register, tests |
| Cognitive bias | Is evidence being selected or framed unfairly? | Sampling details, competing sources |
| Counterarguments | What is the strongest reasonable case against it? | Independent analyses, contrary evidence |
| Quantitative rigor | Are units, rates, baselines, denominators, and calculations correct? | Raw data and methodology |
| Completeness | Are requirements, stakeholders, or key cases missing? | Scope, interviews, acceptance criteria |
| Technical correctness | Are implementations, APIs, states, and edge cases correct? | Code, specifications, logs, tests |
| Security and privacy | Where could trust boundaries, permissions, or data handling fail? | Threat model, controls, tests |
| Reliability | What happens during timeouts, bad inputs, partial failure, or scale? | Incident history, test results |
| User impact | Does it meet user needs and avoid unintended harm? | User research, feedback, outcomes |
| Accessibility | Can users with relevant disabilities use it effectively? | Accessibility testing |
| Feasibility | Are cost, team, timelines, and dependencies realistic? | Estimates, staffing, historical delivery |
| Market and business | Is demand supported? Do economics hold? | Customer data, costs, retention |
| Ethics and fairness | Are relevant people affected disproportionately? | Segment analysis, policies |
| Regulatory fit | Which claims require current jurisdiction-specific checks? | Official policies, professional assessment |
| Communication | Is the output clear and appropriately calibrated? | Audience needs, readability checks |
| Measurement | Can success, failure, and change be detected? | KPI definitions, baselines, monitoring |

## 3. Finding Severity and Confidence

### Severity

| Level | Use when |
| --- | --- |
| Critical | Credible immediate or systemic harm, major security exposure, or a failure that blocks the primary objective |
| High | Significant impact on key users, decisions, revenue, safety, data integrity, or delivery |
| Medium | Material weakness with a practical workaround or bounded impact |
| Low | Minor problem, clarity issue, or limited improvement opportunity |

**Severity is not confidence.** A potentially critical issue supported by weak evidence should be labeled *Critical potential impact, unverified*, not presented as an established critical defect.

### Evidence Status

- **Confirmed:** Direct source evidence, reproducible observation, or valid calculation supports the finding.
- **Likely:** Multiple indicators support the issue, but further testing is needed.
- **Possible:** Plausible concern without enough evidence to assess its presence.
- **Unsupported:** Available material does not justify the claim.
- **Not applicable:** Dimension is irrelevant to the reviewed task.

### Confidence

- **High:** Direct, consistent, sufficiently complete evidence.
- **Medium:** Reasonable supporting evidence with material limitations.
- **Low:** Limited or indirect evidence, significant uncertainty.

Do not assign invented numerical probabilities. When useful, express uncertainty as ranges grounded in data and assumptions.

## 4. Standard Findings Table

| ID | Finding | Evidence | Status | Severity | Impact | Recommended fix | Verification |
| --- | --- | --- | --- | --- | --- | --- | --- |
| F-01 | [Specific issue] | [Source or reproduction] | [Confirmed / Likely / Possible] | [Level] | [Affected outcome] | [Action] | [Test or source check] |
| F-02 | [Specific issue] | [Source or reproduction] | [Confirmed / Likely / Possible] | [Level] | [Affected outcome] | [Action] | [Test or source check] |

For complex risk reviews, add probability, owner, estimated effort, and deadline. If a field cannot be established, write *Unknown* rather than inventing a value.

## 5. Modular Review Controls

Add one or more controls to the master prompt. These are plain-language instructions, not software commands.

### Evidence Controls

- **Evidence only:** Limit conclusions to the supplied, verifiable material.
- **Claim ledger:** List each material factual claim and its evidence status.
- **Source audit:** Test whether citations actually support the claims attached to them.
- **Date-aware:** Flag facts that could have changed since the stated date.
- **No fabricated references:** Never generate unsupported source titles, links, or quotations.
- **Calculate again:** Recalculate relevant numbers and show denominators and units.
- **Unknowns first:** Identify missing evidence that could change the decision.

### Reasoning Controls

- **No sycophancy:** Do not validate the user's preference without analysis.
- **Steelman:** Give the strongest fair version of the opposing argument.
- **Devil's advocate with evidence:** Challenge the position using credible evidence, not automatic contrarianism.
- **Falsification:** Specify what would disprove the key hypothesis.
- **Assumption check:** Identify unverified premises and their consequences.
- **Counterfactual:** Evaluate what might have happened without the proposed action.
- **Root cause:** Distinguish underlying causes from symptoms and correlations.

### Risk and Decision Controls

- **Pre-mortem:** Assume the plan failed and identify plausible causes and warning signs.
- **Red team defensively:** Examine realistic misuse and failure scenarios without producing exploit instructions.
- **Edge-case audit:** Inspect unusual but meaningful conditions and boundary states.
- **Opportunity cost:** Compare the proposal against the best alternative and no action.
- **Kill criteria:** Define measurable conditions to pause or stop.
- **Reverse the conclusion:** Identify evidence that would justify the opposite decision.
- **Verification plan:** Require an independent test for each high-impact finding.

### Writing Controls

- **No fluff:** Remove irrelevant introductions, filler, and repeated conclusions.
- **Plain English:** Use simple wording and explain necessary terms.
- **No AI phrases:** Avoid generic excitement, inflated claims, and formulaic transitions.
- **No em dashes or emojis:** Keep publication-friendly prose.
- **Direct answer:** Give the verdict before supporting detail.
- **Concise but complete:** Cut redundancy without omitting material facts.

## 6. Review Depth Settings

### Quick Review

> Evaluate [material] for its three most consequential weaknesses. Give evidence, expected impact, a fix, and one verification step for each. Flag uncertainties. Avoid filler and automatic agreement.

**Best for:** Email drafts, small decisions, quick fact checks, and preliminary screening.

### Standard Review

> Review [material] for accuracy, assumptions, logical gaps, meaningful counterarguments, and practical risks. Rank findings by impact and evidence strength, then recommend corrections and tests.

**Best for:** Articles, plans, proposals, reports, and routine product decisions.

### Deep Review

> Apply the full master framework to [material]. Build a claim and assumption register, assess relevant review dimensions, test alternative explanations, produce a prioritized finding table, and recommend a verifiable action plan. State what remains unknown.

**Best for:** High-impact business decisions, research, launches, technical architecture, and public-facing claims.

### Adversarial Review

> Challenge [material] as an independent expert trying to discover its weakest defensible assumptions and most consequential failure modes. Steelman the opposition, seek disconfirming evidence, test extreme but realistic conditions, and distinguish verified defects from hypothetical risks. End with fixes and validation tests.

**Best for:** Pre-launch reviews, major investments, important claims, and red-team exercises.

## 7. Domain-Specific Master Prompt Extensions

Append an extension only when relevant. Use the specialized files for more detailed prompts.

### Product and Business Strategy

> Evaluate product-market fit evidence, customer segments, competitor alternatives, adoption assumptions, pricing, CAC, retention, unit economics, roadmap tradeoffs, and launch readiness. Do not treat untested projections as established facts.

### SEO, AEO, GEO, and AI Search

> Evaluate search intent, content accuracy, technical accessibility, crawlability, rendering, indexability, canonicalization, measurement, user outcomes, and claims about AI search inclusion. Do not assume that structured data or crawl access guarantees visibility, ranking, or citations.

### Software Engineering and Architecture

> Inspect requirements, implementation correctness, edge cases, failure recovery, backward compatibility, performance claims, observability, tests, and rollout or rollback plans. Quote specific supporting evidence when available.

### AI and Agentic Systems

> Assess instruction hierarchy, untrusted inputs, prompt injection defenses, retrieval fidelity, tool permissions, action approval gates, model evaluation, uncertainty calibration, monitoring, and human escalation. Prefer defensive tests and least-privilege designs.

### Research and Statistics

> Review hypothesis clarity, experimental design, sampling, confounders, measurement validity, missing data, statistical inference, reproducibility, external validity, and whether conclusions exceed the evidence.

### Marketing and Content

> Inspect source reliability, customer relevance, claims substantiation, content freshness, originality, channel attribution, audience fit, conversion assumptions, and whether recommendations are measurable.

### Financial or Investment Decisions

> Verify data dates, assumptions, cash flows, unit economics, scenario sensitivity, downside risks, liquidity needs, and uncertainty. Identify where regulated or professional advice is needed.

### Legal, Health, and Other High-Stakes Topics

> Separate general information from expert interpretation. Identify jurisdiction, context, source freshness, safety considerations, and which claims require a qualified professional. Do not invent or imply current professional verification.

## 8. Ready-to-Use Combinations

### Combination A: No Fluff + No Sycophancy + Evidence

> Review [claim] independently. No fluff. Do not agree automatically. Separate supported facts from assumptions, give the strongest counterargument, and conclude only what the evidence allows.

### Combination B: Find Flaws + Rank Risks + Fixes

> Audit [plan] for confirmed defects, realistic failure modes, missing requirements, and hidden dependencies. Rank each finding by impact and confidence. Include a concrete fix and test for every material issue.

### Combination C: Fact Check + Bias Check + Hallucination Check

> Evaluate [AI-generated answer] for verifiable claims, fabricated or mismatched citations, leading framing, cherry-picked evidence, missing dates, numerical errors, and unjustified certainty. Return a corrected answer with uncertainty clearly marked.

### Combination D: Pre-Mortem + Red Team + Stop Rules

> Assume [initiative] fails after launch. Identify likely failure paths, important warning indicators, safe defensive mitigations, and explicit measurable conditions for revising or stopping.

### Combination E: Counterargument + Alternatives + Recommendation

> Evaluate [decision]. Present the strongest case for and against it, compare reasonable alternatives including doing nothing, then recommend a choice based on evidence, reversibility, and tradeoffs.

### Combination F: Technical Audit + Edge Cases + Verification

> Review [technical design] for incorrect assumptions, invalid input handling, authorization boundaries, reliability, performance, and rollback risks. Separate observed defects from possible risks and define reproducible verification tests.

### Combination G: Research + Data + Causal Claims

> Audit [analysis] for measurement validity, denominator changes, sampling bias, seasonality, confounding, selective reporting, and unjustified causal claims. Identify which conclusions remain supported.

### Combination H: Natural Writing + Quality Control

> Edit [text] to be direct, natural, and easy to understand. Preserve all supported claims. Remove repetition, AI-sounding phrases, exaggerated assertions, emojis, and em dashes. List any claim requiring verification separately.

## 9. Examples of Applying the Master Prompt

### Example 1: A Product Launch Proposal

**Claim:** "The new feature will increase retention by 20%."

A critical review should check the definition of retention, baseline, cohort, evidence from comparable experiments, expected sample size, downside risks, and competing explanations.

**Useful finding:** The proposed increase is a hypothesis rather than a measured result. Require an experiment with pre-defined retention metrics, a control group where feasible, and guardrail measures.

### Example 2: An SEO Performance Report

**Claim:** "Organic clicks increased by 30% because of the new content strategy."

A critical review should verify the same date range, search platform, property, filters, brand versus non-brand segmentation, seasonality, search demand, tracking changes, and comparison against unaffected pages.

**Useful finding:** A traffic increase is observable, but attribution to the strategy is not established without stronger comparative evidence.

### Example 3: A Software Vulnerability Claim

**Claim:** "This endpoint is vulnerable because it has no authentication in the frontend code."

A critical review should distinguish absence of frontend checks from the state of backend authorization. Review server-side controls and permitted defensive testing.

**Useful finding:** Frontend evidence alone does not prove an authorization vulnerability. Confirm the server behavior before assigning a verified severity.

### Example 4: An AI-Generated Research Answer

**Claim:** "A recent study proved that a model outperforms all competitors."

A critical review should examine the paper's date, evaluation dataset, tested competitors, statistical uncertainty, task scope, independent replication, and whether the source actually uses such a strong claim.

**Useful finding:** Benchmark leadership on selected tests does not justify a universal performance claim.

## 10. Common Review Mistakes to Avoid

1. **Manufactured criticism:** Inventing flaws to satisfy a request for aggressive review.
2. **False certainty:** Labeling a suspicion as verified without a source or reproduction.
3. **False balance:** Giving weak and strong evidence equal weight.
4. **Contrarian bias:** Automatically opposing the user instead of evaluating the merits.
5. **Checklist theater:** Applying irrelevant risk categories solely to make a report appear extensive.
6. **Citation laundering:** Treating a link or citation as proof without checking what it says.
7. **Duplicated findings:** Rephrasing one problem under several headings.
8. **Unclear severity:** Confusing potential impact with actual probability or confidence.
9. **Generic fixes:** Recommending "improve quality" without specifying changes and tests.
10. **Ignoring constraints:** Suggesting solutions that cannot be delivered within the stated resources.
11. **Overweighting edge cases:** Treating extremely unlikely scenarios as the primary decision driver without justification.
12. **Missing opportunity cost:** Comparing only risks and benefits of one option without alternatives.
13. **Unsupported quantitative precision:** Inventing percentages or confidence scores.
14. **Outdated claims:** Giving current-sounding advice based on an unstated historical source.
15. **Style over substance:** Focusing on phrasing while overlooking factual or logical errors.
16. **Overlong output:** Burying the priority findings under repetitive explanations.

## 11. Final Publication and Review Checklist

- [ ] The original claim and objective are represented accurately.
- [ ] Relevant source materials and scope are identified.
- [ ] Facts are separated from interpretations and assumptions.
- [ ] Important counterarguments are represented fairly.
- [ ] Numerical calculations and citations have been checked where possible.
- [ ] Findings are supported and categorized by evidence status.
- [ ] Severity and confidence are not conflated.
- [ ] Duplicated findings are combined.
- [ ] Each significant issue has a practical fix and verification step.
- [ ] Decision thresholds and uncertainty are clear.
- [ ] Writing is direct, natural, and free of irrelevant filler.
- [ ] Unavailable evidence and domain expertise are disclosed.

## Related Prompt Libraries

- [Anti-Sycophancy](anti-sycophancy.md)
- [Flaw Detection](flaw-detection.md)
- [Evidence Verification](evidence-verification.md)
- [Adversarial Review](adversarial-review.md)
- [Hallucination and Source Audit](hallucination-and-source-audit.md)
- [Logic and Assumptions](logic-and-assumptions.md)
- [Decision and Risk](decision-and-risk.md)
- [Practical Response Command Library](practical-response-command-library.md)
- [Review Workflows and Templates](review-workflows-and-templates.md)

**Scope note:** This is a self-contained master framework created for this repository. It is not claimed to reproduce verbatim any inaccessible source conversation.
