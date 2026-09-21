# Cost Curve & Pricing Strategy
Packaging Decision 
- Leader: Backlog creation 
- Filler: Release notes creation 
- Killer: Delivery Report creation
- Killer usage: 35%-> Add - on 

## Cost Model

| Cost Category | Per-User/Month | Notes |
|--------------|----------------|-------|
| Inference (primary model) |$20| Claude Opus5|
| Inference (cascading/triage) |$8 |Claude Haiku |
| Infrastructure |$0.50 | AWS |
| Data/storage | $2| AWS RDS|
| Human-in-the-loop |$10 |  |
| **Total AI COGS** | 40.50| |

## Cascading Strategy
<!-- Cheap model → frontier model routing logic -->
**Triage model: Claude Haiku 4.5**
**Frontier model: Claude Opus 5**
**Routing rule:**
**Expected cascade ratio: 65/35**

| Feature | Complexity | Model Tier | Cost/ Req|Volume% | Weighted|
|---------|------------|------------|----------|--------|---------|
|Bug Creation|Complex| Frontier| $0.50| 56%|$ 0.325%|
|Release Notes creation| Medium| Mid| $1.50| 25%| $0.375|
|Delivery report creation| Medium| Mid| $0.80| 10%| $0.080|
|Blended| | | |100% |$0.78|



## Pricing Model

**Current pricing:**
**Proposed AI pricing:**
**Model:** seat-based / usage-based / outcome-based / hybrid

Pricing Strategy Block, Module 3

Pricing Strategy
- Strategy posture: Maximize
- Pricing model: Hybrid (base + usage)
- Unit of work metered: 100 tickets
- Base fee ($/month): 300
- Price per unit: $2
- Estimated units/user/month: 3
- Implied revenue/user/month: $306.00

Decision Note
Why this pricing structure fits the buyer and the value delivered: Users pay per 100 tickets creation, which is the equivalent unit of work· The Margins are about 98.6%


## Stress Tests

| Scenario | Impact on Margin | Response |
|----------|-----------------|----------|
| Inference costs 3x | | |
| Heaviest segment doubles | | |
| Model provider raises prices 50% | | |

## Board One-Pager
<!-- Before/After: Old SaaS revenue vs. AI usage revenue for your product -->

**Before (traditional SaaS):**
**After (AI-enabled):**
**Net margin shift:**
