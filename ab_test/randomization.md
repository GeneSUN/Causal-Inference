# Why Randomization Is Hard to Maintain in A/B Testing
In practice, maintaining clean randomization in A/B testing is difficult. Two major challenges are choosing **the right unit of randomization** and handling **heavy users who contribute disproportionate traffic.**

## A. Unit of Randomization

It’s mainly a trade-off between **SUTVA violations (interference, multiple versions per unit)** and **statistical efficiency (sample size / variance)**.


| Unit            | Use when                   |
| --------------- | -------------------------- |
| Customer-level  | Best for independence      |
| Household-level | Avoid cross-user influence |
| Store-level     | If price is public         |
| Region-level    | If logistics differ        |


### 1. User-level or Session-level Randomization

**Advantages**
- Easy to implement.
- Enables fast experimentation and large sample sizes.

**Disadvantages**
- Users may experience **cross-contamination** (seeing both variants).
- Potential interference effects, where past exposure influences future behavior.
- Heavy users may dominate traffic, which can bias traffic-weighted metrics.
- Repeated observations from the same user violate independence assumptions.


### 2. Higher-Level Randomization (Cluster, Store, Region, Stratified Sampling)

Advantages
- Reduces contamination and spillover effects.
- Preserves consistent experience within each cluster.
- Better suited for social, marketplace, or geographically dependent experiments.

Disadvantages

- Higher cost and operational complexity.Requires careful matching or stratification to ensure balance.
- Lower statistical power, since the effective sample size becomes the number of clusters.
- Greater variance due to intra-cluster correlation.

## Heavy users usually have a small percentage of the total population but contribute the most traffic


## Sanity Check

### 1) A/A Test (Gold Standard Sanity Check)
What it does

- Split traffic into two groups but show the exact same experience.

What you expect

- No statistically significant differences in metrics
- P-values uniformly distributed
- No systematic metric lift

What it detects
- Bugs in assignment logic
- Logging inconsistencies
- Sample ratio mismatch
- Metric computation errors
- Time-based rollout bias

Red flags
- Frequent false positives
- One side consistently “wins”

> If A/A fails → your A/B infrastructure cannot be trusted

### 2) Sample Ratio Mismatch (SRM) Check


### 3) Pre-Treatment Covariate Balance Check
Goal

Ensure groups look statistically identical BEFORE treatment

**Compare Control vs Treatment on:**
- Geography
- Device type
- User tenure
- Activity level
- Historical revenue
- Engagement last week

Methods
- Standardized mean difference (SMD)
- KS test for distributions
- Visual distribution overlays

Rule of thumb
- Differences should be near zero (|SMD| < 0.1)

If groups differ on pre-treatment variables → randomization likely failed.

### 4) Invariant Metric Tests
Idea

Check metrics that should NOT change due to treatment.

Examples
- Account creation rate (if unrelated)
- Browser version share
- Country distribution
- Past purchase history
- Page load latency (if unrelated)

If invariant metrics move → bias or instrumentation issues
