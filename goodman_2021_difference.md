# <DiD Treatment Timing>

**Contributor:** <카린 | Caitlin Manchester >

**Full citation:** <Goodman-Bacon, Andrew. 2021. "Difference-in-Differences with Variation in Treatment Timing." Journal of Econometrics 225 (2): 254–77.>

## 1. What the paper establishes
The DD estimator encompasses both ‘pre’ and ‘post’ treatment time periods, and ‘treatment’ and ‘control’ groups. The paper claims that the TWFE estimator is a weighted average of all DD estimators within a data set and if units receive treatment at different times it affects said weighted average.  
The papers fix is understanding when TWFEDD is applicable, and when alternative estimators should be applied. 

## 2. Checks for a reviewer

A) **Check whether the paper exploits variation across groups of units that receive treatment at different times.**  

B) **If the paper uses TWFE with time-varied treatment, check whether already-treated units act as controls for later treated groups.** If the paper uses DD with units that receive time varied treatment, check whether authors state already-treated units are used as controls. 

C) **If the paper uses TWFE with time-varied treatment, check whether the authors justify constant treatment effects ($\Delta ATT=0$) when already-treated units serve as control.** If treatment effects change over time, TWFE is biased relative to VWATT. This asks if TWFE i causally valid. 

D) **If the paper uses TWFE with time-varied treatment, check whether the author defines the estimand, and whether the TWFE coefficient is noted as ATT or VWATT.** If the treatment has multiple application periods and the TWFE estimator is used, check whether tthe coefficient is shown as ATT or VWATT. With time-varied treatments, the TWFE coefficient is generally VWATT which does not necessarily = ATT. 

E) **If the paper uses TWFE with time-varied treatment, check for time-varying covariates.** adjustment aiming to address confounding or common trends assumption. - thought to make a “common trends” assumption more plausible but most are time-varying controls, introduces a new source of identifying variation that was not there in the unadjusted version.  is it justified as pretreatment/unaffected 



## 3. Evidence
Check whether the paper exploits variation across groups of units that receive treatment at different times

For A)  From the authors literature review, “Half of the 93 DD papers published in 2014/2015 in 5 general interest or field journals had variation in timing“(255). 

For B) “Event-study estimates show that the treatment effects grow over time.. which biases many of the timing comparisons” (256). “All timing groups are controls in some terms, but the earliest and/or latest units necessarily get more weights as controls than treatments” (264). “The comparison of later to earlier treats states.. account for the bias in the overall DD estimate” (266). “when already-treated units act as controls, changes in their outcomes are subtracted and these changes may include time-varying treatment effects“.(255) “the TWFEDD estimator can fail to identify interpretable treatment effect parameters and suggest that practitioners should be careful when relying on it in designs with treatment timing variation”(256). “Standard TWFE regression only results in an unbiased ATE under assumptions of parallel trends and treatment effects constant over time and across groups.“ “In time-varied designs, weight assigned can be negative, meaning the TWFE estimate can go in the opposite direction to the treatment effect”
Note: ”This does not imply a failure of the design in the sense of non-parallel trends in counter factual outcomes, but it does suggest caution when using TWFE estimators to summarize treatment effects.” (255)
Reference: Eq 2 + Theorem 1 

For C) “If [units] treatment effects are changing they can substantially bis TWFEDD away from VWATT” (261). “[C]hanges in the treatment effects for always-treated units may dominate $\Delta{ATT}$.”(261). “Time-varying effects bias estimates say from VWATT because $\Delta{ATT} =/= 0$. 

For D) “The TWFEDD estimate(−3.08) is therefore a misleading summary of the average post-treatment effect(about−5)” (256). “VWATT does not equal the sample ATT. Neither are the weights proportional to the share of time each unit spends under treatment, so VWATT also does not equal the effect in the average treated period” (262). 

For E) “Covariates change the way TWFEDD weights subsample estimators [and] adjust the 2x2 estimates themselves”(270). “Most applications, however, include time-varying controls” see EQ21 (268). “[F]or covariates to aid in identification, they must be unaffected by the treatment to avoid bias from ”conditioning on a post-treatment variable”” the author quotes Rosenbaum 1984 (268). “Adding controls therefore introduces a new source of identifying variation… that was not there in the unadjusted version” (270) shows how adding covariates does not adjust the existing comparison but creates a new identifying variation that can skew results. “The weight on each 2×2 is based on $\hat V^d_{b,k\ell}$ rather than $\hat V^D_{k\ell}$, which shows that covariates change the way TWFEDD weights subsample estimators” (270). “When treatment effects are correlated with post-period changes in the covariates, controls absorb part of the treatment effect.” “Any control variable could inappropriately absorb treatment effects.” (271)

## 4. Scope
Applies to: causal studies using TWFEDD with time-varied treatment. Check A is triggered when 

Does not apply to: 2x2 DD where units have no time variation and controls are untreated. 

Applies to: Studies with multiple application periods of treatment that use TWFE but interpret as ATT. 

Does not apply to: 2x2 DD where all treated units’ treatment occurs in same period. 
Does not apply to: already-treated controls where treatment effects are constant over time. 

## 5. What failure looks like

A paper includes already-treated units but treats the design as 2x2 DD without acknowledging variation in treatment timing. It uses already-treated units with time-varying effects as control against later-treated units without acknowledging effects or balancing for them, potentially producing a misleading summary of the average post treatment effect or bias due to changes in weights. The paper includes such treatment timing variation and does not use simple flexible estimators (Callaway and Sant’Anna) or evaluative tools such as provided by Goodman-Bacon. The paper uses TWFE to summarise treatment effects that vary overtime, despite $\Delta ATT \neq 0$. The paper seeks to estimate the sample ATT but interprets the TWFE coefficient an ATT despite it identifying VWATT. The paper does not address bias or contamination. The paper includes time-varying covariates that introduce a new source of identifying variation, without justification. 

## 6. Test cases
Card & Krueger (1994) April 1992 New Jersey

No:
Assessing the impact of public–private partnership adoption on regional economic growth in Asia, (Lutfah Ariana, Rimawan Pradiptyo, Evi Noor Afifah):
Flag staggered DiD framework, dynamic treatment effect. But, employ the staggered Difference-in-Differences (DiD) approach developed by Callaway and Sant’Anna - does not flag? appropriately accounts for differences in adoption cohorts and avoiding biases associated with conventional TWFE
