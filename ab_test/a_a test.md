
## The purpose of A/A tests?
  1. run an A/A test on the metric to obtain its variance, σ² (prepare for the sample size calculation for an A/B test.)
  2. A/A tests assess if the experimentation platform works as expected.  (the experimentation platform introduces bias in the treatment and control groups before the intervention, invalidating any test results.) (if the observed ratio split is statistically different from the expected ratio?)<img width="659" height="91" alt="image" src="https://github.com/user-attachments/assets/03191112-0128-4107-973e-d216291e8026" />

## The difference between A/A tests and A/B tests
A/A tests follow the same design logic as A/B tests that split the users into two groups and assign the treatment accordingly. The only difference is A/A tests assign the same treatment to both groups.<img width="676" height="63" alt="image" src="https://github.com/user-attachments/assets/684726ed-a15e-4ca5-a52b-a2c57fe939a2" />

## How to interpret
the p-values of repeated A/A trials follow a uniform distribution, which is the central argument of today’s blog post.<img width="676" height="63" alt="image" src="https://github.com/user-attachments/assets/f558018e-46ff-442e-87aa-5f5e9eb7021f" />


	1. p-values should fall 
		p<0.05 for 5% of the time
		p<0.10 for 10% of the time
		p<0.20 for 20% of the time
		p<0.30 for 30% of the time
		This is simply another way of restating the definition of p-value from earlier. 
	2. Another way to say the same thing is that p-values should be distributed uniformly between 0 and 1.
		

  <img width="150" height="113" alt="image" src="https://github.com/user-attachments/assets/716cb4cb-d6ed-4b97-9ed4-3daa4a93aa42" />
  <img width="150" height="113" alt="image" src="https://github.com/user-attachments/assets/3ef6db92-ed20-4e58-8071-0b89e4f1a913" />


[p-Values for Your p-Values: Validating Metric Trustworthiness by Simulated A/A Tests](https://www.microsoft.com/en-us/research/articles/p-values-for-your-p-values-validating-metric-trustworthiness-by-simulated-a-a-tests/)

