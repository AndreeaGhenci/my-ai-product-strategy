# Compounding System Design

## Feedback Loops

| Loop | Input | Output | Compounds? | Status |
|------|-------|--------|-----------|--------|
| Recursive Learning | transaction data from true to positives and false negatives | feeds into monthly model retraining | Y | active |
| Cross-Domain Transfer | transaction data from true positives | update anti- money laundering models | Y | missing |
| Network Intelligence | customer reports in customer service | update golden dataset | N | missing |

**Broken loop identified by partner:** ·

**Fix plan:** ·

## Context Connectivity
<!-- How does knowledge flow across teams and domains? Where does it silo? -->

**How knowledge flows:** True positives training data which is used for multiple fraud models in the bank transfers.

**Where it silos:** Customer service chats don't get into the training data. 

**Broken loop identified by partner:**
i.e Audit your governance policy for Samsung- path risks ( data leaks) and Air Canada (AI making promises the company can't keep)
Keep in mind Look for missing data clases, unclear escalation paths, agents without human oversight, no review cadence. 
Loops: Broken handoff? Theoretical learning? Corrections trashed? 
Governance: Unapproved gent action? Missing data class? Samsung style paste path? Air Canada - style customer bot? 

**Fix plan:**
Be specific about how the plan will be fixed. Be very specific on what are the action points. 

## Governance Policy

**Scope:**
**Autonomy boundaries:**
**Escalation triggers:**
**Audit cadence:**
**Regulatory exposure (EU AI Act / other):**

## Agent Topology
<!-- If using agents: what can each agent do? What can't it do? Who approves what? -->
<!-- Governance Policy, SupportCopilot v1.2 -->

## Governance Policy

**Scope:** AI features in the SupportCopilot product line, automated reply drafting, routing, and resolution scoring. Excludes: Internal-only analytics dashboards (covered by separate data-team policy).

**Autonomy boundaries:** Drafting automated replies, auto. Sending replies under $0 risk (FAQ, account info), auto. Sending replies with promised remedies (refunds, credits, escalations), even if confidence > 95%, human approval required. Closing tickets without reply, never auto.

**Escalation triggers:** (1) Confidence < 70% on response. (2) Customer message flagged legal, medical, or distressed. (3) Any reply mentioning refund, credit, or policy exception. (4) Customer requests human contact. (5) Three or more turns in a single conversation.

**Audit cadence:** Weekly, Automated eval against golden dataset (PM: Sam). Monthly, Human review of 50 random conversations + all escalation cases (Legal: Priya). Quarterly, Full policy review with security + legal (CTO sign-off).

**Regulatory exposure (EU AI Act / other):** EU AI Act, GDPR, SOC 2. Risk tier: limited. Controls: Data minimization in prompts · No training on customer PII · SOC 2 log retention controls in place · DPIA on file..

## Agent Topology

_Not shipping agents this version._


## Shadow AI Audit

| Tool | Owner | Risk Level | Decision |
|------|-------|-----------|----------|
| | | H / M / L | keep / govern / kill |
| | | H / M / L | keep / govern / kill |
| | | H / M / L | keep / govern / kill |

i.e 
Shadow AI Audit (user-side), Module 5
## Discover, User-Side Workarounds
| Workaround | Signal source | Signal type | Freq | $/mo | Decision | 
|------------|---------------|-------------|------|------|----------|
|Export weekly report CSV → ChatGPT for exec summary | source: Support ticket | signal: Workflow gap | freq: H | spend: $20/mo | decision: Build |
|Pipe API output through Claude to clean tone before client send | source: User interview | signal: Trust gap | freq: M | spend: $20/mo | decision: Build |
|Zapier recipe: our webhook → OpenAI → Slack alert summarizer | source: Zapier/Make | signal: Capability gap | freq: M | spend: $15/mo | decision: Partner |
|Users running our exports through ChatGPT to translate to non-English markets | source: Forum/Reddit | signal: Capability gap | freq: L | spend: $20/mo | decision: Partner |
|CS team manually runs Perplexity on customer domain to enrich onboarding | source: Sales call | signal: Workflow gap | freq: H | spend: $20/mo | decision: Build |
|Users asking ChatGPT to interpret our pricing page before buying | source: Social media | signal: Trust gap | freq: L | spend: $0/mo | decision: Ignore |

## Pattern Assessment
- Workarounds found: 6
- Build candidates: 3
- Partner candidates: 2
- Ignore decisions: 1
- Adjacent spend: $95/mo
- Dominant signal: Workflow gap

## Action Plan
### Build
CSV export → exec summary (high freq, clear capability gap)
CS onboarding domain enrichment (high freq, internal workflow)
Tone-cleanup for client-facing API output (M4 trust gap, pair with reliability contract refresh)

### Partner
Zapier webhook → OpenAI summarizer recipe → ship an official Zapier integration with templated recipes
Translation workflow → partner with one localization-AI provider with a deep link from the export screen

### Ignore + Monitor
Users running ChatGPT on our pricing page → not strategic to absorb; monitor sentiment and improve pricing page clarity instead.

## Roadmap Brief
Based on your audit: 6 user-side workarounds discovered.
Decisions: 3 build · 2 partner · 1 ignore · 0 TBD.
Estimated adjacent spend: $95/mo across surveyed users.
Dominant signal: Workflow gap.

Recommended next step: Workflow gaps dominate, your users are stitching your product into multi-step pipelines. Strongest near-term move is partner integrations with the AI tools they already chain in.

Sequence the Build column by frequency × strategic relevance. Confirm Partner candidates with the external tools' partnership teams. Re-run this audit each quarter, workarounds shift fast.


**Total tools found:**
**Tools after triage:**
**Estimated hidden spend:**
