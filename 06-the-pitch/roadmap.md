# Three-Horizon Roadmap & Board Pitch

## Roadmap

### Horizon 1 — Now (0-3 months)
*Quick wins. Ship with existing capabilities.*

| Initiative | Metric | Confidence |
|-----------|--------|-----------|
| | | H / M / L |
| | | H / M / L |

### Horizon 2 — Next (3-9 months)
*Bets. Requires new capabilities or integrations.*

| Initiative | Metric | Confidence |
|-----------|--------|-----------|
| | | H / M / L |
| | | H / M / L |

### Horizon 3 — Bet (9-18 months)
*Moonshots. High uncertainty, high potential.*

| Initiative | Metric | Confidence |
|-----------|--------|-----------|
| | | H / M / L |

## Board Pitch

**Thesis (1 sentence):**

**The case:**
1. Why now:
2. What's defensible:
3. The economics:

**The risks:**
1. Trust / failure modes:
2. Scale / governance:
3. Competitive:

**The ask:**

## M1 Baseline vs. Now
*Your 3-sentence AI strategy from Module 1 vs. what you'd say now:*

**M1 baseline:**

**Now:**

## Horizon 1, Ship (0–4 weeks)

High-confidence initiatives that establish the core product, quality baseline, and unit economics.

| Initiative                                      | Strategy Component | Why it ships now                                                                                                   | Confidence |
| ----------------------------------------------- | ------------------ | ------------------------------------------------------------------------------------------------------------------ | ---------- |
| 1. NDA + MSA triage for 10 design-partner firms | Bet                | Validates the core 4-hour → 15-minute value proposition with real users; 95% recall is the initial quality target. | H          |
| 2. Golden-set eval harness in CI                | Contract           | Essential release gate to prevent regressions below 95% recall or above 2% hallucination.                          | H          |
| 3. Green/yellow/red confidence UX               | Contract           | Makes uncertainty visible and enforces human review on red clauses, establishing user trust.                       | H          |
| 5. Cascading inference router                   | Margin             | Tests whether the 80/20 routing architecture can maintain the $0.12/contract cost target.                          | H          |

Execution caveat: H1 is feasible only if the golden dataset is already labeled, the clause taxonomy is defined, and an initial model exists. Otherwise, four weeks is an aggressive delivery commitment.

## Horizon 2, Validate (1–3 months)

Medium-confidence initiatives requiring evidence of adoption, economic value, or defensibility before scaling.

| Initiative                                    | Strategy Component | Hypothesis                                                                                                              | Kill Criteria                                                                                                                                       | Confidence |
| --------------------------------------------- | ------------------ | ----------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------- | ---------- |
| 4. Clause-library flywheel                    | Moat               | Capturing and reusing reviewer corrections improves firm-specific recall and reduces repeat corrections.                | If by week 6 we cannot demonstrate a ≥10% reduction in repeat corrections on a held-out, firm-specific evaluation set, stop expanding the flywheel. | M          |
| 6. Procurement + employment contract coverage | Bet                | Existing clause models and taxonomy can generalize to adjacent contract types without disproportionate labeling costs.  | If by week 6 neither new contract type achieves ≥90% recall on its own representative validation set, stop expansion and refocus on NDA/MSA.        | M          |
| 7. Self-serve tier + usage-based pricing      | Margin             | Mid-market legal teams will adopt self-serve onboarding and pay $500/month plus $2 per contract at sustainable margins. | If by week 6 fewer than 3 of 10 qualified prospects commit to a paid pilot at target pricing, stop self-serve investment and revisit packaging.     | M          |

Sequencing recommendation: Start correction capture during H1, but treat the flywheel's demonstrated learning advantage as H2. Begin contract-type expansion only after NDA/MSA recall and hallucination thresholds are consistently met.

The H2 kill thresholds above are proposed decision gates, not validated benchmarks. Establish sample sizes and measurement methods before starting each experiment.

## Horizon 3, Explore (3–6 months)

Low-confidence strategic options, funded as contained experiments rather than committed product delivery.

| Initiative                                | Strategy Component | What must be true first                                                                                                                                        | Confidence |
| ----------------------------------------- | ------------------ | -------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------- |
| 8. Negotiation copilot (redline drafting) | Bet                | NDA/MSA triage achieves stable quality, users demonstrate demand for drafting, and human-controlled redlines can be evaluated reliably against firm precedent. | L          |

Scope control: Limit H3 to a redline prototype with 2–3 design partners. Do not commit to becoming a legal-ops system of record until the product demonstrates differentiated workflow value and a credible integration strategy.

## Unmapped (cut or rethink)

| Initiative | Why it's unmapped                                                              | Recommendation                           |
| ---------- | ------------------------------------------------------------------------------ | ---------------------------------------- |
| None       | All eight initiatives connect to at least one of the five strategy components. | No initiative is strategically unmapped. |

However, strategic alignment does not automatically justify investment. Initiative 7 has a valid Margin connection, but self-serve distribution is not necessary to prove the initial product bet and should not receive full development funding before pricing validation.

## Mapping Disagreements

No disagreements, all user mappings stand. No explicit `[User-mapped to: X]` lines were provided, so all eight mappings were assigned independently.

## Strategic gaps identified

Initiative coverage by component

Primary mappings only

Bet

3

Contract

2

Margin

2

Moat

1

Guardrails

0

The biggest gap is Guardrails, with zero directly mapped initiatives despite explicit commitments to legal oversight, approval boundaries, and shadow-AI auditing. These are operational obligations, not optional future enhancements.

I would add an H1 guardrail initiative covering enforcement of the $50K auto-approval boundary, audit logging, and a legal sign-off process for model releases. The shadow-AI audit can follow in H2.

## Final three recommendations

1. Most over-indexed horizon: H1, with four delivery commitments; H3 has only one exploratory bet, while Guardrails lacks implementation work in every horizon.
2. H3 bet to protect: Negotiation copilot, because moving from clause detection to precedent-aware redlining offers the strongest opportunity to expand customer value and defensibility.
3. Initiative to kill today: Kill the self-serve build portion of initiative 7, not pricing validation; it is premature before repeatable onboarding, willingness-to-pay, and reliable unit economics have been demonstrated.
