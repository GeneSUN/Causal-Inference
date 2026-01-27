## 1. What is Sample Ratio Mismatch (SRM)?

You planned:
- 50% Control
- 50% Treatment

But you observe:
- 57% Control
- 43% Treatment

This suggests:
- Randomization or traffic allocation is broken — meaning your causal estimate may be invalid.


## 2. How to Check SRM (Statistical Test)

Step 2 — Run a chi-square test

<img width="295" height="66" alt="Screenshot 2026-01-27 at 1 21 57 PM" src="https://github.com/user-attachments/assets/fad286f5-20e9-4fa7-ab75-523e1d2cbd52" />

## 3. How to Decide If SRM Is Acceptable?

| SRM size | Action                 |
| -------- | ---------------------- |
| <0.5–1%  | Monitor                |
| 1–2%     | Investigate            |
| >2%      | Likely invalidate test |


## 4. How to Fix SRM (What To Do)

### Reweight samples (only if mild)

Apply inverse probability weighting:

$$ w = expected/observed $$

### Option D — Intent-to-Treat (ITT)

Analyze based on original assignment, not observed exposure


⚠️ Say clearly in interviews:

Reweighting helps but does not fully restore causality.
