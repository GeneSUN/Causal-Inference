
## 1. What is interference in A/B testing?

Standard A/B tests assume **SUTVA (Stable Unit Treatment Value Assumption)**:

> One user’s outcome is not affected by another user’s treatment.

## Example of Interference

| Effect                    | What happens                  | Bias                   |
| ------------------------- | ----------------------------- | ---------------------- |
| Spillover to control      | Control is indirectly treated | Underestimates effect  |
| Competition effects       | Treatment harms control       | Overestimates effect   |
| Network influence         | Behavior propagates           | Confounds attribution  |
| Market equilibrium shifts | System-wide changes           | Invalid counterfactual |


## Solution
### Fix — Ego-Cluster Randomization

Instead of randomizing individuals:

- Treat a user and their social neighbors together
- Randomize at the social network cluster level

### Coarser Randomization (Geo-Level)

Randomize by:

- City
- Region
- Market

So:

- Entire local supply-demand system is treated together
- No cross-group driver competition

### Fix — Switchback Design (Time-Based Randomization)

Instead of splitting users:
- Apply pricing to everyone, but only during certain time windows




