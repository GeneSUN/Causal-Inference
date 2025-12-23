
## Individual Causal Inference

### 1. Potential and Observed Outcome
- potential(counterfactual) outcomes.
  - $$Y^{ a=1}$$
- observed(actual) outcome
  - $$Y=1$$

**Analogy:**

$$y=f(x)+\epsilon$$
- f(x): the ideal outcome of x
- in reality, nothing is ideal, outcome is interrupted by unpredicted errors

Assumption of Consistency

The potential outcome under treatment A=a, Y^a, is equal to the observed outcome if actual treatment receieved 

**for one individual who experienced effect a=1, the actual outcome is the potential outcome.**

$$(Y^{ a=1}) == (Y=1) $$

### 2. Individual Causal Inference
   
$$Y^{ a=1}-Y^{ a=0}$$


when i had a actual response of one individual person, i will never know what is the potential outcome, or the real causal inference


**Conclusion:**
identifying individual causal eﬀects is generally not possible,

## Average Causal Inference



$$Y^{ a=1}-Y^{ a=0}==> (Y_1=1)-(Y_2=1)$$ 

$$Y_1 !=Y_2$$

## RANDOMIZED EXPERIMENTS


$$Y_1,Y_2,Y_3,... vs. Y_a,Y_b,Y_c,...$$ 

**Exchangeability**

$$ \Pr(Y^a = 1 \mid A = 1) = \Pr(Y^a = 1 \mid A = 0) = \Pr(Y^a = 1).$$

$$Y^a \perp\ A ,\neq Y \perp\ A$$


Because the **randomized assignment** of treatment leads to **exchangeability**, Ideal randomized experiments can be used to identify and quantify average causal eﬀects

What if not ideal randomized?

# Observational studies

observational study can be conceptualized as a conditionally randomized experiment 



if the analogy between observational study and conditionally randomized experiment happens to be correct, then we can use the methods described in the previous chapter–IP weighting or standardization–to identify causal eﬀects from observational studies. We therefore refer to these conditions as identifiability conditions or assumptions.




When treatment is not randomly assigned
by the investigators, the reasons for receiving treatment are likely to be associ-
ated with some outcome predictors. That is, like in a conditionally randomized
experiment, the distribution of outcome predictors will generally vary between
the treated and untreated groups in an observational study.

## Confounding

## Outcome regression and propensity scores



