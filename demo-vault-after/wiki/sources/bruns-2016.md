---
type: source
title: "Bruns and Ioannidis (2016), p-Curve and p-hacking in observational research"
description: Monte Carlo simulations and a cross-country growth illustration showing that null effects with even tiny omitted-variable bias produce right-skewed p-curves, so that p-curves cannot separate true effects from p-hacking in observational research.
created: 2026-09-04
updated: 2026-09-04
sources: [bruns-2016]
status: draft
generated:
  by: claude-code/claude-fable-5-1
  at: 2026-09-04
doi: 10.1371/journal.pone.0149144
licence: CC BY 4.0
---

# Bruns and Ioannidis (2016), p-Curve and p-hacking in observational research

Bruns, Meta-Research in Economics Group, University of Kassel, and Ioannidis, Stanford University (Departments of Medicine, Health Research and Policy, and Statistics, and the Meta-Research Innovation Center at Stanford). PLoS ONE 11(2), e0149144, received 30 October 2015, accepted 27 January 2016, published 17 February 2016. No specific funding and no competing interests declared. The paper states that all relevant data are within the paper and its Supporting Information: three appendices (S1 on the simulation design, S2 on the empirical illustration, S3 on the full-sample rerun of the illustration) and two datasets. None of the appendices is part of the extracted source, so details beyond the main text are not available here.

## What the paper set out to do

The paper asks whether the p-curve, the distribution of statistically significant p-values in a published literature, can distinguish true effects from null effects with p-hacking when the research is observational. It defines observational research as any study in which there is no randomisation in the comparison of the groups of interest, and states that such studies make up the large majority of the scientific literature, putting the figure, from a count by Dal-Ré et al. (2014), at almost 300,000 observational studies against 20,000 randomised ones per year in PubMed.

Two lines of work are reported. First, Monte Carlo simulations in which a null effect is combined with randomly drawn omitted-variable biases and only the significant estimates are kept. Second, an empirical illustration built on the effect of malaria prevalence on economic growth between 1960 and 1996, using a well-known cross-country growth dataset.

## How the paper defines p-hacking

The paper follows the notation of Simonsohn, Nelson and Simmons (2014) and denotes p-hacking as the selection of statistically significant estimates for publication within each study. For experimental research it lists, citing Simmons, Nelson and Simonsohn (2011), choosing dependent variables or covariates after the fact, adding observations until the estimate is significant, and reporting only a subset of experimental conditions. It adds that a survey by John et al. (2012) found questionable research practices that can be used to p-hack, among them the exclusion of data after the fact, rounding down of p-values, and framing an unexpected finding as having been predicted from the start.

The paper's own subject is an additional source of p-hacking that it says is specific to observational research. When regression coefficients are estimated from observational data, many decisions have to be made: the functional form, the estimation technique and, most prominently, the set of adjusting variables included to control for confounders. This flexibility yields a wide range of estimates from which significant ones can be selected. The paper says the practice is also known as multiple modelling, data snooping or data-mining, that it can cause what has been called a vibration of effects, and that it is a well-known threat to the validity of inferences in observational research.

## How the paper reads a p-curve

The paper attributes to Simonsohn and colleagues the argument that true effects generate right-skewed p-curves, that null effects give uniformly distributed p-values, and that a null effect with p-hacking gives a left-skewed p-curve or a peak of p-values just below 0.05. The stated intuition is that p-hacked studies manipulate their estimates to reach p-values that are just significant, while p-values close to zero are hard to obtain by p-hacking. It also describes Jager and Leek (2014) as modelling the p-curve as a mixture of a uniform distribution for null effects and a beta distribution for true effects.

The paper accepts the point, attributed to Simonsohn and colleagues, that the two determinants of the p-curve are the effect size and the sample size, but replies that the estimated effect size can differ from zero because of an omitted-variable bias rather than a true effect.

## Omitted-variable bias as a mechanism for p-hacking

If an adjusting variable has its own effect on the dependent variable and is correlated with the variable of interest, leaving it out of the regression induces omitted-variable bias, which the paper describes as a typical case of unaccounted confounding. Its illustration is regressing exam grades on class attendance: attendance may have no effect at all, but ability and study effort affect grades and are correlated with attendance, so an unadjusted estimate is likely to be biased upwards and may be significant without any true effect.

The paper's central argument is that this bias behaves differently from the p-hacking discussed for experimental research. Omitted-variable bias makes the estimate of the effect of interest biased and inconsistent, so the p-value approaches zero as the sample size grows whether or not there is a true effect. Even a tiny bias reaches p-values near zero if the sample is large enough. This generates a right-skewed p-curve, exactly as true effects do. In experimental research, by contrast, randomisation keeps estimation unbiased and consistent, and p-hacking relies on chance rather than on a systematic and asymptotic bias. Hence, on the paper's account, if omitted-variable biases are used for p-hacking, the p-curve cannot tell true effects from null effects with p-hacking.

The paper says it focuses on omitted-variable bias because varying the regression specification is likely to be the main way of selecting significant estimates, but that other biases which also make estimation biased and inconsistent (simultaneity, misspecification of the functional form, measurement error) may produce right-skewed p-curves in the same way. It also says the scope of the bias is wider than p-hacking, citing work by Schuemie et al. (2014) as showing that in pharmacoepidemiology even best-practice designs (case-control, cohort and self-controlled case series) produce far more false positives under null effects than the 5% expected by chance, which the paper suggests may be caused by omitted-variable biases the designs do not remove.

## The simulations

### Design

The data-generating process is y = β*x + γz + ε, with the effect of interest β* set to zero so that only null effects are simulated. There are 500,000 iterations. In each, x, z and ε are drawn from a multivariate standard normal distribution with exogeneity ensured, and the regression is estimated with z omitted, so that the estimated coefficient on x is potentially biased. The expected bias is γ times the covariance of x and z divided by the variance of x. With the variance of x equal to one and the covariance fixed at 0.2, the coefficient γ is drawn afresh in each iteration from a uniform distribution between 0 and a maximum, so the expected omitted-variable bias is uniformly distributed between 0 and 0.2 times that maximum.

Three strengths of bias are simulated, set so that the maximum expected Pearson correlation between y and x is 0.01 (Case 1), 0.05 (Case 2) or 0.1 (Case 3). The paper stresses that this correlation is due to omitted-variable bias, not a true effect, and notes that on Cohen's (1988) conventions even 0.1 counts as small, so the maximum biases range from one tenth of a small effect to a small effect. The sample size of each iteration is drawn from a uniform distribution with a minimum of 50 and a maximum of 100, 1,000, 10,000 or 100,000, which the paper matches to domains from small studies of novel biomarkers or uncommon conditions to large cohorts and big data.

The paper calls its modelling of p-hacking conservative: all variables are resampled in every iteration, rather than resampling only γ for a fixed dataset until a significant estimate appears, so there is no intensive search across biases within one dataset.

### Results

Fig 1 has three panels, one per case, each plotting the share of statistically significant p-values in bins across the range 0 to 0.05 for the four maximum sample sizes, with a dashed horizontal line marking a uniform distribution. The extracted text reports that even for these tiny biases the p-curves become right-skewed once the sample size is sufficiently large, and that none of the p-curves is left-skewed or peaks just below 0.05.

The panel legends, which are present only in the figure images and not in the extracted text, give the share of the 500,000 iterations that reached p < 0.05. For Case 1 (maximum correlation 0.01): 5.04% at a maximum sample size of 100, 5.19% at 1,000, 6.91% at 10,000 and 23.88% at 100,000. For Case 2 (0.05): 5.72%, 10.33%, 41.8% and 77.87%. For Case 3 (0.1): 8.11%, 26.94%, 69.12% and 89.52%. In the panels, the curves for the smallest biases and sample sizes lie close to the uniform line, and the right skew grows with both the bias and the sample size; in Case 1 it is pronounced only at the largest sample size, whereas in Case 3 every curve, including the one for samples of at most 100, slopes downwards from the lowest bin.

The paper reads the simulations as showing that both of the standard readings, right skew as a true effect and left skew as p-hacking, can be false in observational research.

## The empirical illustration

### Data and the constructed null

The illustration uses the dataset of Sala-i-Martin, Doppelhofer and Miller (2004), widely used in the cross-country growth literature. Its dependent variable is the annualised average growth rate of real GDP per capita between 1960 and 1996, and it holds 68 candidate determinants of growth, of which the paper selects 15 that are likely to affect growth, most measured in 1960 or the 1960s to avoid simultaneity. The effect examined is malaria prevalence in 1966. The paper reports that the original authors' Bayesian model averaging found this effect sensitive to model size, with larger models rendering it insignificant, and that recent reviews (it cites Rockey and Temple, 2015) do not treat malaria prevalence as a genuine determinant of growth, so it regards a null effect as safe to assume for the sake of illustration.

To make the effect exactly zero, the paper regresses growth on malaria prevalence and all 15 adjusting variables, then generates a new growth variable from the estimated intercept, the 15 coefficients and the residuals with the malaria coefficient set to zero. The original estimate on malaria in that full regression is -0.00764, with a p-value of 0.224. The correlation between the original and the constructed growth variable is 0.987.

### Model space and vibration of effects

The typical model in the growth literature has seven independent variables, so each regression includes malaria prevalence and 6 of the 15 adjusting variables, giving 5,005 possible models. Data are available for 99 countries; samples of countries are drawn with sizes uniform between 50 and 99, so that results are not specific to one sample and sample sizes vary across studies as they do in real literatures.

A vibration plot (Fig 2) shows the estimates from all 5,005 models on each of 100 random samples, 500,500 estimates in all, against transformed p-values, with a solid line at p = 0.05 and dashed lines at the 1st, 50th and 99th quantiles of both distributions. Estimates of both signs occur. Of the 500,500 estimates, 62.6% are negative and not significant, 23.4% are negative and significant at p < 0.05, 0.103% are positive and significant, and 13.9% are positive and not significant.

### The p-hacked p-curve

P-hacking is modelled as follows: draw a random sample of countries; browse randomly through the 5,005 models; if a negative and significant estimate appears, keep it, draw a new sample and start again; if none of the 5,005 models gives one, draw a new sample and start again. This continues until 100,000 negative, significant estimates have been collected. The paper describes this as less conservative than the simulation, and possibly more realistic, because many specifications are tried on the same dataset before a new sample is drawn.

Fig 3 shows the resulting p-curve (left) and the histogram of the selected estimates (right), based on the 100,000 significant negative estimates. The paper reports that the p-curve is right-skewed, consistent with the simulations, and that there is no sign of a peak just below 0.05. At a reviewer's request the illustration was rerun using the full sample of 99 countries every time, to remove sampling error; the paper reports that this too gives a right-skewed p-curve (S3 Appendix, not extracted), which it takes as confirming that omitted-variable bias is what produces the skew.

## What the paper claims

- P-hacking in observational research typically produces right-skewed p-curves, which have been taken as evidence of true effects, and none of the analysed p-curves shows the left skew that has been taken as evidence of p-hacking. P-curves may therefore identify neither true effects nor p-hacking in observational research, and inferences drawn from them on either count are likely to be flawed when observational designs are involved.
- The extent of the right-skewed distortion under a null effect is proportional to the amount of omitted-variable bias. With small samples, a bias corresponding to a maximum correlation of 0.1 suffices for major distortion; with large samples, as in big cohorts or big data, a bias corresponding to 0.01 distorts p-values, in the paper's words, beyond repair. The paper offers this as a possible explanation of the failure of major inferences from observational studies to replicate in randomised trials and as a reason for caution about observational big data.
- Head et al. (2015), whose text-mined p-values come from both experimental and observational designs, found right-skewed p-curves in many disciplines and concluded that most studies analyse true effects even though p-hacking is ubiquitous. The paper says that conclusion rests on the assumption that right skew indicates true effects, which may be false for observational research, and that even in experimental research a right-skewed p-curve implies only that some of the studies analyse true effects. It cites a preprint by Bishop and Thompson (2015) as illustrating that right skew can occur when only 25% of the studies analyse true effects.
- Jager and Leek's (2014) estimate of a 14% false discovery rate in the medical literature rests on the assumption that the right-skewed beta component of their mixture comes from true effects; since the paper shows that null effects with p-hacking in observational research can generate the same skew, it says the false discovery rate for that distribution could be anything, even 100%.
- Little can be learned from such studies beyond an indication that p-curves may be right-skewed across some disciplines; the sources of the skew remain unexplained and uncertain. Replication projects (the paper names the Open Science Collaboration and the Many Labs project) are described as a much more promising route to the false discovery rate.
- The paper says its findings are consistent with Schuemie et al. (2014), whom it also cites as showing that the inflated false-positive rate under best-practice observational designs comes with right-skewed p-curves, and as finding that at least 54% of findings claimed significant at 0.05 in the biomedical literature become non-significant when p-values are empirically calibrated against an empirical null built from drug-outcome pairs believed to have no causal link. It suggests that research using large observational datasets should avoid judging p-values against theoretical null distributions and the 0.05 threshold, while noting that calibration is not always possible because a sufficient sample of uncontested true positives and true negatives may not exist.
- Observational research that tests hypotheses would benefit from careful pre-specification of the analysis plan; the paper cites a survey by Boccia et al. (2015) as finding that registered observational protocols almost never pre-specify their statistical analysis. Hypothesis-generating studies should report their exploratory character transparently, acknowledge results obtained under different models, and interpret the highlighted model with great caution.
- The same problem can arise in nominally experimental research. The paper cites evidence that many randomised studies are not properly randomised or carry biases that subvert randomisation, argues that questionable research practices can turn a trial into the equivalent of an observational study, and cites a study by Saquib et al. (2013) of trials in leading clinical journals in which the adjusted or unadjusted analysis of the primary outcome differed between protocol and paper, with the significant analysis almost always the one the authors preferred. Group imbalances in trials, it says, are hard to attribute to chance or to subverted randomisation.
- The paper also cites other work (Bishop and Thompson, 2015; Lakens, 2015) as finding that some kinds of p-hacking leave no left skew even in experimental research.

## What the paper concedes

- The omission of confounders is not necessarily p-hacking. It may stem from unavailable data or from not knowing what to adjust for, and even seasoned experts rarely agree on the adjustment set; the paper cites an assessment of 60 studies of pterygium risk factors in which no two studies adjusted for the same variables.
- If omitted-variable bias is used to exaggerate a true effect rather than to make a null effect significant, the resulting right skew correctly indicates a true effect. The paper says this may often happen when power is low, and that a right-skewed p-curve therefore leaves open three states: a null effect with p-hacking, a true effect, or a true effect exaggerated by p-hacking.
- Simonsohn and colleagues introduced the p-curve primarily for experimental research, and the paper allows that right skew may be a sign of true effects for those designs.
- The simulation is conservative by design, with no intensive search within a dataset; the empirical illustration is less conservative. The null effect in the illustration is constructed, since the paper treats the absence of a malaria effect on growth as safe to assume for illustration rather than as established.
- The paper simulates omitted-variable bias only; the other biases it names as possible sources of right skew are discussed but not simulated.
- Empirical calibration of p-values is not always feasible.

## Cited by

- [[p-curve-as-evidence]]
- [[text-mined-p-values]]
- [[what-p-hacking-is]]
- [[preregistration-as-a-remedy]]
