# Review Workflows and Output Templates

Use these workflows to convert prompts into practical reviews with repeatable results.

## Workflow 1: Verify a Factual Answer

1. Extract atomic factual claims.
2. Check whether each claim has supporting source material.
3. Identify time-sensitive claims that need fresh verification.
4. Check numbers, units, denominators, and interpretations.
5. Label each claim: supported, unsupported, contradicted, or uncertain.
6. Revise the answer without inventing evidence.

**Reusable instruction**

> Audit [answer] claim by claim. Provide claim, evidence, status, required verification, and correction. Do not infer that a citation supports a claim without checking its content.

## Workflow 2: Stress-Test a Business Decision

1. Describe the decision and constraints.
2. Enumerate assumptions and credible alternatives.
3. Compare risks, costs, reversibility, and opportunity cost.
4. Seek the strongest disconfirming evidence.
5. Identify a low-cost test and measurable thresholds.
6. Recommend proceed, revise, test, or stop.

**Reusable instruction**

> Review [decision] independently. Use the steps above. Distinguish facts from estimates and conclude with a specific next test.

## Workflow 3: Audit a Technical Specification

1. Extract explicit requirements.
2. Identify ambiguous words and missing acceptance criteria.
3. Map dependencies and boundary conditions.
4. Review defensive security, privacy, and reliability issues.
5. Design positive, negative, and recovery tests.
6. Assign priority based on actual impact and supporting evidence.

**Reusable instruction**

> Audit [specification] and return a requirement-gap table with evidence, user impact, suggested fix, and acceptance test. Do not claim an untested defect is verified.

## Workflow 4: Red-Team an AI Workflow Defensively

1. Map input sources and trusted or untrusted boundaries.
2. Identify where retrieved text or tool output could be mistaken for instructions.
3. Inspect tool permissions, approval gates, and sensitive data handling.
4. Examine failures from model uncertainty or stale information.
5. Propose mitigations and controlled defensive tests.
6. Specify safe escalation and recovery behavior.

**Reusable instruction**

> Review [AI workflow] for instruction confusion, data leakage, excessive tool permissions, unsafe autonomous actions, and missing recovery controls. Provide a defensive risk register and tests without exploitation instructions.

## Workflow 5: Edit for Natural Language

1. Identify repetitive phrases and generic introductions.
2. Check claims for unsupported or exaggerated assertions.
3. Simplify overly long sentences while preserving meaning.
4. Remove formulaic transitions, emojis, and em dashes.
5. Confirm the revised text remains complete and accurate.

**Reusable instruction**

> Edit [text] for clear, natural language. Keep all important facts. Avoid fluff, AI-sounding phrases, exaggerated claims, emojis, em dashes, and unnecessary repetition. Return the final text.

## Standard Finding Table

| Field | Definition |
| --- | --- |
| ID | Unique finding identifier |
| Finding | Specific problem or risk |
| Evidence | Quote, data, reproduction, or source |
| Status | Confirmed, suspected, or unknown |
| Impact | What may go wrong and who is affected |
| Severity | Critical, high, medium, or low, with rationale |
| Fix | Concrete corrective action |
| Test | How to verify the issue or fix |

## Verification Checklist

- Did the review use the actual source, not just a summary?
- Are quotes and figures faithful to the source?
- Are false positives separated from confirmed issues?
- Were meaningful alternatives considered?
- Is every high-priority recommendation testable?
- Are important gaps and inaccessible data disclosed?
- Were the final output and source files checked after publication?
