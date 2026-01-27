# Price Elasticity
> “We want to test price elasticity of demand. With different prices, how does demand change? How would you answer?”


## Experiment Design & Causal Inference Template

### Step 1 — Define the Business goal, Causal Goal

- Business goal:

- Causal effect: estimate the causal effect of X (price) on Y (demand)

  - Treatment = Price change
  - Outcome = Demand / conversion / revenue
  - Estimand = Price elasticity
 

### Step 2 — Define Success Metrics & Guardrails

- Primary metric (causal outcome)
  - Units sold
- Secondary / diagnostic metrics
  - Session engagement
- Guardrail metrics (prevent harm)
  - revenue
  - customer complaints
  - long-term retention, brand trust
 
### Step 3 — Define Treatment, Control, and Experimental Variants

Example:

- Control = Current price ($10)
- Treatment A = +5%
- Treatment B = +10%
- Treatment C = −5%

### Step 4 — Define Randomization Strategy (CRITICAL FOR CAUSALITY)

A. Unit of Randomization

| Unit            | Use when                   |
| --------------- | -------------------------- |
| Customer-level  | Best for independence      |
| Household-level | Avoid cross-user influence |
| Store-level     | If price is public         |
| Region-level    | If logistics differ        |

> “I choose the smallest unit that avoids interference — to satisfy SUTVA and prevent spillovers.”

B. Random Assignment Rule

Stratified randomization (by region, tenure, device, etc.)

C. Validity Checks
Interference / spillovers

Threats to validity:

| Risk            | Mitigation            |
| --------------- | --------------------- |
| Seasonality     | Parallel control      |
| Novelty effects | Longer test           |
| Non-compliance  | Intent-to-treat       |
| Spillover       | Cluster randomization |
| Selection bias  | True randomization    |

> “I’d run balance checks to ensure treatment and control groups are statistically comparable.”



### Step 5 — Power Analysis & Sample Size Planning

Consider:

- Minimum detectable effect (MDE)
- Baseline conversion rate
- Desired power (80–90%)
- Traffic availability

> “I’d run a power analysis to ensure we can detect meaningful elasticity without underpowered results.”

### Step 6 — Test Duration & Behavioral Dynamics

Short-term effects:
- Immediate purchase sensitivity
- Low cost
  
Long-term effects:
- Delayed churn
- Reference price anchoring
- Customer learning behavior

> “I’d run the test long enough to capture both immediate demand changes and longer-term behavioral adaptation.”

### Step 7 — Bias, Confounding, and Validity Checks


---

### Step 8 — Run analysis
1. Check assumption
Central limit Theorem, 30 independent, not strongly skewed
2. Define Null Hypothesis
3. Estimate standard error
SE=√((σ_1^2)/n_1 +(σ_2^2)/n_2 )
Decision Error



---

### Step 8 — Estimation Strategy (How You Compute Causal Effect)

### Step 9 — Segment & Heterogeneity Analysis (Senior-Level Signal)

Elasticity varies by:
- Customer tenure
- Income proxy
- Region
- Purchase frequency
- Product category


### Step 10 — Business Decision & Rollout Plan

Interpret results into action:
- Revenue-maximizing price
- Risk-adjusted decision
- Ramp strategy (gradual rollout)

Say this:

“I’d combine statistical significance, business impact, and long-term customer risk to make rollout decisions






