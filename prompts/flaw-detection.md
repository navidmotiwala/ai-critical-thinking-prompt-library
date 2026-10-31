# Flaw detection prompts

### 1. Failure audit

> Audit [plan or document] for factual errors, logical gaps, contradictory requirements, hidden dependencies, edge cases, and execution risks. Rank findings by severity and likelihood. For each, give the evidence, impact, and practical fix.

### 2. Assumption inventory

> List the assumptions behind [proposal]. Mark each as verified, plausible but unverified, or unsupported. Identify the three assumptions whose failure would most change the outcome.

### 3. Missing requirements

> Review [specification] as a skeptical implementer. Identify ambiguous requirements, missing acceptance criteria, failure states, accessibility gaps, security and privacy considerations, and operational dependencies. Do not invent requirements without labeling them as recommendations.

### 4. Contradiction check

> Compare these statements: [text]. Identify direct contradictions, apparent contradictions caused by missing context, and statements that can both be true. Quote the relevant passages.

### 5. Pre-mortem

> Assume [project] failed six months after launch. Give plausible causes, early warning signals, and preventive actions. Separate likely risks from low-probability scenarios.

### 6. Prioritized repairs

> For each confirmed issue in [audit], provide a minimal reproducible example or supporting passage, severity, affected scope, proposed repair, and verification test. Do not call a suspected issue confirmed without evidence.
