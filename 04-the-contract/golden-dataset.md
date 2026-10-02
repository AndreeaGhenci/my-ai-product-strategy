# Golden Dataset & Reliability Contract
Golden Dataset, Module 4

Test cases:
  1. Edge: N · Judge: LLM, IN: Daily activity drops by 42% → OUT: Likely to churn
  2. Edge: N · Judge: rule, IN: System is not delivering the right answers  → OUT: Likely to churn 
  3. Edge: Y · Judge: rule, IN: User is using the product for a different purpose  → OUT: This is outside the scope

Dataset health
- Total: 3
- Edge cases: 1 (33.3%)
- Judge mix: 67% rule / 33% LLM / 0% both


## Golden Dataset Spec

| # | Input | Expected Output | Edge Case? | Judge Type |
|---|-------|----------------|-----------|-----------|
| 1 | | | Y/N | rule / LLM |
| 2 | | | Y/N | rule / LLM |
| 3 | | | Y/N | rule / LLM |
| 4 | | | Y/N | rule / LLM |
| 5 | | | Y/N | rule / LLM |

**Adversarial rows included:** __
**Coverage gaps identified by partner:**

## Confidence UX Design

**Approach:** Chatbot displays how confident it is about data in a dashboard.

**Confident (>90%):** Full answer, showing sources and references, share links.

**Uncertain (50-90%):** Soften language, don't make any commitments. Show to user why data is correct and clarify why data might be wrong. Ask for clarification questions regarding to what is data being used. Ask user to fact check data maybe with a different source.

**Not confident (<50%):** Don't generate a direct answer.  Tell the user that data is incomplete and they should give more direction.

**User control surface:** 

- Users adjust the confidence threshold
- Users see AI reasoning / drivers
- Users correct & override outputs
- Corrections feed back into the model / dataset
- Every recommendation has labels for "accurate", "wrong driver", "missing context", "too agressive", "not actionable" and each label feeds back into the correction loop. 

**Approach:** show uncertainty / tiered confidence / human-in-loop trigger

**High confidence (>90%):**
**Medium confidence (70-90%):**
**Low confidence (<70%):**

**User control surface:**

## Reliability Contract

| Metric | Target | Measurement | Alert Threshold |
|--------|--------|-------------|-----------------|
| Accuracy | | | |
| Hallucination rate | | | |
| Latency (p95) | | | |
| Drift velocity | | | |

| Metric | Target | Measurement | Alert Threshold |
|--------|--------|-------------|-----------------|
| Accuracy | 90% | Weekly - 300 golden rows - LLM as a judge (GPT-4o, accuracy rubric) | <80% |
| Hallucination rate | <1% | Same weekly run - safety rubric flags fabricate data/ tickets/ reports/ release notes. | >2% → route to human review queue |
| Latency (p95) | <800ms | Continuous prod monitoring. | >1200ms → route to human review queue |
| Drift velocity | <0.5/ week | 6 week rolling accuracy trend vs golden data set | >1%/ week → trigger gold-set audit |

## HITL Architecture
<!-- When does a human step in? What's the escalation path? -->

**Trigger:** Confidence under 50% OR safety rubric flag fires on a customer facing output

**Reviewer:** Rotating PM on call 9am - 5pm GMT, Mon - Fri. For out of hours send to PM on call email.

**Feedback loop:** Review correction feed back into the weekly gold set audit,  5+ corrections in a week triggers a model retain candidate.




## Red-Team Findings
*What failure mode did your partner find that you missed?*
