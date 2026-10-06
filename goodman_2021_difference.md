# <DiD Treatment Timing>

**Contributor:** <카린 | Caitlin Manchester >

**Full citation:** <Goodman-Bacon, Andrew. 2021. "Difference-in-Differences with Variation in Treatment Timing." Journal of Econometrics 225 (2): 254–77.>

## 1. What the paper establishes
The DD estimator encompasses both ‘pre’ and ‘post’ treatment time periods, and ‘treatment’ and ‘control’ groups. The paper claims that the TWFE estimator is a weighted average of all DD estimators within a data set and if units receive treatment at different times it affects said weighted average.  
The papers fix is understanding when TWFEDD is applicable, and when alternative estimators should be applied. 

## 2. Checks for a reviewer
A) **If the research includes variation in treatment timing, check if it uses already-treated units as control. **

B) **Check if the author claims to estimate the ATT or the VWATT.** If the author claims to use ATT but the treatment has multiple application periods, the author is estimating the VWATT not the ATT. 

C) **If the research includes already-treated units as control, check if it uses TWFEDD estimator. ** 

D) **Look for evidence of dynamic heterogeneity (impact growing/changing over time) ** 

E) **Controls** - thought to make a “common trends” assumption more plausible but most are time-varying controls, introduces a ew source of identifying variation that was not there in the unadjusted version.  

## 3. Evidence

A) “Event-study estimates show that the treatment effects grow over time.. which biases many of the timing comparisons” (256). “All timing groups are controls in some terms, but the earliest and/or latest units necessarily get more weights as controls than treatments” (264). “The comparison of later to earlier treats states.. account for the bias in the overall DD estimate” (266). 

B) “VWATT does not equal the sample ATT. Neither are the weights proportional to the share of time each unit spends under treatment, so VWATT also does not equal the effect in the average treated period” (262). 

C) “the TWFEDD estimator can fail to identify interpretable treatment effect parameters and suggest that practitioners should be careful when relying on it in designs with treatment timing variation”(256). 

D) 

E) “When treatment effects are correlated with post-period changes in the covariates, controls absorb part of the treatment effect.” “Any control variable could inappropriately absorb treatment effects.” (271) 

## 4. Scope

## 5. What failure looks like

## 6. Test cases
