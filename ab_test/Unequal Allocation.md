# Unequal Allocation of Traffic in A/B Tests: Pros and Cons

40% control / 60% treatment split, you can still estimate the causal effect the same way as long as assignment was randomized (and you didn’t change the split mid-test).


<img width="593" height="201" alt="Screenshot 2026-01-27 at 3 54 22 PM" src="https://github.com/user-attachments/assets/192be0e3-01e0-4ebb-a70c-5f8c04141625" />


<img width="641" height="213" alt="Screenshot 2026-01-27 at 3 54 11 PM" src="https://github.com/user-attachments/assets/c8dc74f4-4ce3-46c9-af6b-621f03c60261" />

## 3) When would you need weighting (IPW)?




set different treatment probabilities by stratum (e.g., 40% in stratum 1, 50% in stratum 2), 
as long as randomization happens within each stratum and those probabilities are pre-specified. This is a standard “stratified randomized experiment” setup.


1) Estimate effect within each stratum


2) Combine strata into ONE overall effect (post-stratified / stratified ATE)

- https://academic.oup.com/jrsssb/article/75/2/369/7075411?utm_source=chatgpt.com&login=false


3) Standard error (how to combine uncertainty)


4) Equivalent (and often easiest) approach: regression with strata fixed effects

https://chatgpt.com/share/69795260-a1f8-8009-a143-91d38cc73c27
