# <DiD Treatment Timing>

**Contributor:** <카린 | Caitlin Manchester >

**Full citation:** <Goodman-Bacon, Andrew. 2021. "Difference-in-Differences with Variation in Treatment Timing." Journal of Econometrics 225 (2): 254–77.>

## 1. What the paper establishes
The DD estimator encompasses both ‘pre’ and ‘post’ treatment time periods, and ‘treatment’ and ‘control’ groups. The paper claims that the TWFE estimator is a weighted average of all DD estimators within a data set and if units receive treatment at different times it affects said weighted average.  
The papers fix is understanding when TWFEDD is applicable, and when alternative estimators should be applied. 

## 2. Checks for a reviewer

A) **Check for variation in treatment timing, and use of already-treated units as control.** If the paper uses DiD with units that receive time varied treatment, check whether authors state already-treated units are used as controls. 

B) **If the research includes already-treated units as control, check if it uses TWFEDD estimator.** 

C) **Check if the estimand is ATT or VWATT.** If the treatment has multiple application periods and the TWFE estimator is used, check whether tthe coefficient is shown as ATT or VWATT. With time-varied treatments, the TWFE coefficient is generally VWATT which does not necessarily = ATT. 

D) **Check for covariates adjustment aiming to adress confounding or common trends assumption.** - thought to make a “common trends” assumption more plausible but most are time-varying controls, introduces a new source of identifying variation that was not there in the unadjusted version.  is it justified as pretreatment/unaffected 

## 3. Evidence

For A)  From the authors literature review, “Half of the 93 DD papers published in 2014/2015 in 5 general interest or field journals had variation in timing“(255). 
 “Event-study estimates show that the treatment effects grow over time.. which biases many of the timing comparisons” (256). “All timing groups are controls in some terms, but the earliest and/or latest units necessarily get more weights as controls than treatments” (264). “The comparison of later to earlier treats states.. account for the bias in the overall DD estimate” (266). “when already-treated units act as controls, changes in their outcomes are subtracted and these changes may include time-varying treatment effects“.
 Reference: Eq 2 + Theorem 1 

For B) “the TWFEDD estimator can fail to identify interpretable treatment effect parameters and suggest that practitioners should be careful when relying on it in designs with treatment timing variation”(256). Standard TWFE regression only results in an unbiased ATE under assumptions of parallel trends and treatment effects constant over time and across groups. In time varied designs, weight assigned can be negative, meaning the TWFE estimate can go in the opposite direction to the treatment effect. However, it is important to note that even when said assumptions are fulfilled, some 2x2D DD comparisons which contribute to TWFE are actually confounded. 
Eq2 + Theorem 1 

For C) “VWATT does not equal the sample ATT. Neither are the weights proportional to the share of time each unit spends under treatment, so VWATT also does not equal the effect in the average treated period” (262). 
Reference: Eq 15-16

For D) “When treatment effects are correlated with post-period changes in the covariates, controls absorb part of the treatment effect.” “Any control variable could inappropriately absorb treatment effects.” (271)
Eq 21-27? Shows new identifying variation created by time-varying covariates. 

## 4. Scope
Applies to: causal studies using TWFEDD with time-varied treatment. Check A is triggered when 

Does not apply to: 2x2 DD where units have no time variation and controls are untreated. 

Applies to: Studies with multiple application periods of treatment that use TWFE but interpret as ATT. 

Does not apply to: 2x2 DD where all treated units’ treatment occurs in same period. 

## 5. What failure looks like
Has variation in treatment time
uses already treated units as controls 
Does not address bias/contamination
Says estimates ATT but TWFE estimator is actually producing VWATT

## 6. Test cases
Card & Krueger (1994) April 1992 New Jersey

No:
Assessing the impact of public–private partnership adoption on regional economic growth in Asia, (Lutfah Ariana, Rimawan Pradiptyo, Evi Noor Afifah):
Flag staggered DiD framework, dynamic treatment effect. But, employ the staggered Difference-in-Differences (DiD) approach developed by Callaway and Sant’Anna - does not flag? appropriately accounts for differences in adoption cohorts and avoiding biases associated with conventional TWFE
