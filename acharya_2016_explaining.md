# <Causal Findings Without Bias>

**Contributor:** <카린 | Caitlin Manchester>

**Full citation:** <Acharya, Avidit, Matthew Blackwell, and Maya Sen. 2016. "Explaining Causal Findings Without Bias: Detecting and Assessing Direct Effects." American Political Science Review 110 (3): 512–29.>

## 1. What the paper establishes

The authors exert that 



Authors recommend estimating CDE using sequential g-estimation, to eliminate competing explanations whilst avoiding serious bias. 

## 2. Checks for a reviewer

a) check if the research simply condition on post treatment variables

b) check for intermediate cofounders: does the author include variables affected by treatment that also have an affect on the mediator and outcome? Does the author exclude obvious ones that would bias results? 
 
c) check the estimand in relation to the paper’s claim, and interpretation of ATE - ACDE: if intermediate confounders are present, check the authors do not identify ANDE or ANIE without acknowledging individual-level homogeneity assumptions. Also check the authors note ATE - ACDE as an aggregation of effects. 

d) check for use of sequential g-estimation: if the authors estimate ACDE with intermediate cofounders present, do they apply sequential g-estimation. 



## 3. Evidence

a) “an extremely common approach to these types of questions is to simply condition on[…] post treatment variables” with the aim of producing “a causal effect estimate washed of an alternative explanation”(p512). The authors estimate that “as many as two thirds of empirical papers[…] make causal claims condition[ed] on post-treatment variables”, with “40% explicitly conditioned on a posttreatment variable in the analysis” and “27% conditioned on a variable that could plausibly be posttreatment”(512).  Furthermore, as “about 23%[…] did so in order to explicitly test or adjudicate between causal mechanisms” or “control for alternative causal pathways”, this attempt to estimate causal effect by fixing variables can lead to “seriously biased estimates of these direct effects”(512). “can induce spurious relationships between the treatment and the intermediate confounders and, thus, the outcome (Rosenbaum 1984)” (518). “selection bias that leaves the coefficient of interest without any causal interpretation” 514 
“can induce spurious correlations between the treatment and the outcome” as may be “endogenous and related to the outcome in non causal ways” 514. 
“inclusion of post treatment variables into a statistical analysis can bias the estimator away from zero[…] overstate the size of a causal effect in either direction” 514
“estimates may also be inconsistent” and “converge to the wrong quantity” 514, 

b) “confounders for the mediator, but are also affected by treatment” and “most previous approaches to causal mediation confront this problem by sssuming no intermediate confounders exist” but “this may be an unrealistic assumption” that “may not be credible in many applied settings” (518). “moreover the ANDE and the ANIE are unidentified in the presence of intermediate confounders” and the “possible presence of intermediate confounders does raise the possibility of intermediate variable bias” (518). 


c) “empirical application will determine the utility of these approaches”, “in some cases indirect effects are of particular interest while in others the combination of indirect effects and interaction is sufficient” (518). 
“both omitting and conditioning on the intermediate confounders leads to a biased estimate of the ACDE” 518 
as a ‘nonzero ACDE for Mi implies that there must be an indirect effect that works through the set Wi’, 

whether author rules out alternative mechanisms: 517: ‘nonzero ACDe implies indirect effect, difference between ATE and ACDE summarises rol of mediator, difference between ATE and ACDE might still provide some information on how causal findings came to be if we take a broader definition, 
518: difference between ATE and ACDE provides aggregation of two effects, but ‘all direct effect qunitities of interest raid the possibility of intermediate confounders’, ‘ande and anie are unidentified in the presence if intermediate confounders without strong individual level homogeneity ssumption’,

’causal questions under investigation and the research design will often determine which of the two estimands is more appropriate’, e.g. ACDE is more suitable for ‘design with multiple treatments that are jointly randomised to each unit’, ANDE ‘combines the direct effect […] with an interaction’ thus ‘providing more information about the decomposition of the total effect’, etc (527). 

d) because “ACDE is non-parametrically identified under[…] sequential unconfoundedness” this can be “unrealistic in observational studies”, thus 
“assumption might be violated if[…] there are determinants […] that are not included” (520)
“use of sequential g-estimation also avoids potential problems associated with posttreatment bias” (522)
but “validity of approach will depend on the validity of the modeling assumptions in (23)”, and with “limited dependent variables the conditional expectation function will not be truly linear so that there may be some bias in the estimation of the coefficients in (23) and thus the estimation of the demediation function” (521)
also note definition of intermediate confounders (522), some pretreatment confounders could be “miscategorised[…] and thus would be an intermediate confounder”(523). 
“sequential g-estimation is valid for differences in mesns[…] but not for logistic models” as it “can lead to bias from model misspecification” (523). 
by varying p we can vary the severity of th unmeasured confounding for the effect of Mi’, and thus 
‘use of sequential g-estimation also avoids potential problems associated with posttreatmentvias’ 
‘sensitivity analysis allows us to determine what effect unmeasured confounding will have in any empirical application’ 524
‘estimated direct effect […] using sequential g estimation’ may be ‘far stronger’ 525 


## 4. Scope

Applies to: research including intermediate confounders, i.e. variables that occur after the treatment and before the mediator, affecting both the mediator and the outcome.
Does not directly apply to: pre-treatment confounds or variables occurring after the mediator (thus not having a causal effect upon it). Note, post-mediator variables may still cause bias by blocking the pathway or acting as a collider. 
Applies to: studies where variables affected by treatment are controlled for using standard regression or matching, whether to test causal mechanisms or as accidental over-control.  
Does not apply to: research employing sequential g-estimation methods. Note: sequential g-estimation is valid for linear models (differences in means), ‘but not for logistic models’ (523). Or papers only estimating ATE with zero intermediate confounders, thus allowing for standard regression. 


## 5. What failure looks like

A paper seeking to establish causal relationships that controls for post-treatment variables without applying sequential g-estimation, or application of said sensitivity test to logistic models. Papers that claim to identify ANDE/ANIE despite post-treatment confounding variables, or mislabel ATE-ACDE as a pure indirect effect. 

## 6. Test cases

SHOULD trigger: Alesina, Alberto, Paola Giuliano and Nathan Nunn (2013). “On the Origins of Gender Roles: Women and the Plough.” _Quarterly Journal of Economics_ 128 (2): 469-530. the authors use the post-treatment mediator of modern-day per capita income in an OLS regression, introducing post-treatment bias. 
The authors ‘implicitly assume no intermediate confounders, Zi, for the effect of income on women’s political participation’ but this is ‘implausible’(524). 
Issue is found with the ‘ambiguity about the causal ordering’ of outcome and mediator (524). Checks (a)-(d) should apply. (a) should flag the conditioning on post-treatment covariates, (b) should flag the modern variables acting as intermediate confounders as well as the omission of additional factors such as modern education, (c) should flag the targeting of ACDE by holding modern income fixed to show a negative cultural effect remains (without defining the estimand or testing for further interaction),
(d) should flag the lack of usage of sequential g-estimation while using intermediate confounders. 
Fearon, James D., and David D Laitin (2003). “Ethnicity, Insurgency and Civil War.” _American Political Science _ 9 01): 75-90. In showing that the impact of ethnic fractionalisation on the onset of civil wars fades when controlling for several post-treatment factors, the authors include post-treatment variables such as political instability and per capita income. This introduces intermediate variables 
It is noted further that ‘good practice would be to combine different specifications of pretreatment/intermediate confounders and sensitivity analyses’ as there is the possibility of miscategorisation of confounders. Checks (a)-(d) should apply. (a) should flag direct conditioning on post-treatment variables such as political instability, (b) should flag how controls such as regime type act as intermediate confounders thus blocking causal pathways, (c) should flag the implicit targeting of ACDE in trying to show ethnic fractionalisation has no effect when other variables are held fixed, and (d) should flag the use of single regression rather than sequential g-estimation, and the use of logistic regression. 

SHOULD NOT trigger: Acharyacoup, Blackwell, Sen (2016): “The Political Legacy of American Slavery.” _The Journal of Politics_ 78 (3): 621-641. No checks should apply. Authors define ACDE, separate pre-treatment covariates and post-treatment confounders, and apply sequential g-estimation
