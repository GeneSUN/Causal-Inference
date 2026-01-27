# Pitfall 4: Combining metrics over periods where the proportions assigned to Control and Treatment vary, or over subpopulations sampled at different rates

## 1. What is Simpson’s Paradox (plain meaning)?

In A/B testing terms:

- Treatment wins within each time period / country / Stratified
- But loses overall due to uneven weighting across groups

## 2. Common real-world scenarios where it happens
### (A) Ramp-up over time
- Early phase: 1% Treatment / 99% Control
- Later phase: 50% Treatment / 50% Control

If later days have lower conversion overall, Treatment will:
- Win each day individually
- But look worse overall because it saw more low-quality traffic

### (B) Geographic or market segmentation

Example:
- US → 1% Treatment
- Global → 50% Treatment

If regions differ in baseline conversion:
- Treatment wins in each region
- But loses after combining regions due to unequal weighting

(C) Stratified sampling or platform imbalance

Different treatment proportions across:
- Browsers
- Devices
- Customer tiers
- Data centers

## 3. Root cause when we “dig deeper”

Treatment and Control have different exposure proportions across segments.

Formally:

- Treatment is overrepresented in low-performing segments
- Control is overrepresented in high-performing segments



<img width="619" height="148" alt="Screenshot 2026-01-27 at 2 10 01 PM" src="https://github.com/user-attachments/assets/951b2a90-7c81-4a04-8806-95d6b9e6dd9f" />



using weighted combinations.








