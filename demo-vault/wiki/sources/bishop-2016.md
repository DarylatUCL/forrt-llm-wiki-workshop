---
type: source
title: "Bishop and Thompson (2016), Problems in using p-curve analysis and text-mining to detect rate of p-hacking and evidential value"
description: Simulations of ghost-variable p-hacking and a manual audit of 30 text-mined papers, used to argue that p-curves cannot quantify the extent of p-hacking or evidential value without control over the p-values entered.
created: 2026-09-04
updated: 2026-09-04
sources: [bishop-2016]
status: draft
generated:
  by: claude-code/claude-fable-5-1
  at: 2026-09-04
doi: 10.7717/peerj.1715
licence: CC BY 4.0
---

# Bishop and Thompson (2016), Problems in using p-curve analysis and text-mining to detect rate of p-hacking and evidential value

Bishop and Thompson, Department of Experimental Psychology, University of Oxford. PeerJ 4, e1715, submitted 1 September 2015, published 18 February 2016. An earlier version appeared as a PeerJ preprint in 2015 and drew a comment from De Winter and Van Assen that the paper says elaborates one of its points. R scripts and outputs are deposited on OSF (h5tvu). The paper's Appendices S1 to S3 (a worked example of the simulation, p-curves without p-hacking, and the DOIs of the 30 audited papers) are not part of the extracted source. The first author declares that she is an academic advisor and academic editor for PeerJ. Both authors were funded by the Wellcome Trust.

## What the paper set out to do

The paper asks how robust p-curve analysis is to violations of its assumptions, and under what circumstances it can be applied to real-world data. It takes as its case the text-mining study by Head et al. (2015), which used one p-value per paper from over 111,000 published papers to test for evidential value and p-hacking in 14 subject areas.

Three lines of work are reported. First, simulations of one form of p-hacking, the use of ghost variables, to see how the shape of the p-curve depends on whether the dependent variables are correlated. Second, a power analysis of the binomial test that compares the number of p-values in two narrow bins just below 0.05. Third, a manual audit of 30 papers from the Head et al. dataset to see whether text-mined p-values are suitable for p-curve analysis.

## How the paper defines p-hacking and ghost variables

The paper separates two ways in which reported p-values distort the evidence against the null. Publication bias affects which studies get published. P-hacking affects which data and analyses from a single study are included in the publication. The paper attributes the term to Simonsohn, Nelson and Simmons (2014) and describes the practice as reporting only the part of a dataset that yields significant results, with the choice made after scrutinising the data. It names deciding which outliers to exclude, when to stop collecting data, and whether to include covariates as ways of doing this, and says the practice was described, without the name, in 1956 (citing De Groot, 2014).

The paper's own focus is ghost variables: dependent variables that are measured in a study but disappear from the published paper once they turn out not to show significant effects. Its illustration is that if two groups are compared on ten independent variables and none differs in the population, the probability that at least one differs at p < .05 is 1 minus (1 minus 0.05) to the power 10, which is .401. A researcher who did not predict which measure would differ and reports only the significant one produces a paper that implies the result is far less likely to have arisen by chance than it is. The paper says this source of irreproducibility is hard to detect and not always recognised by researchers as a problem.

The paper also describes double-dipping, the circular practice of scrutinising a large dataset to find a region or time window that responds to a stimulus and then testing that region, as a form of p-hacking that can generate p-values well below .05.

## The simulations

An R script, Ghostphack, simulates a study in which two groups of N subjects are measured on X dependent variables and only the variables with p < .05 are reported. The number of variables, effect size, inter-correlation between variables, sample size, distribution of the variables, and whether p-hacking is used can all be varied, and one-tailed or two-tailed tests can be chosen. When a true effect is simulated, an effect size is added to one variable for one group only. A t-test is run on each variable; because p-curve analysis requires independent p-values, one significant p-value is selected at random per study, and studies with no significant p-value are discarded. The output is the number of runs with p-values in given bins, in the same form as the tables of Head et al.

All reported simulations used 100,000 runs, each simulating a study with either 3 or 8 dependent variables. Two power levels were compared: low, with 20 subjects per group, and high, with 200 per group. Inter-correlation between the variables was set at 0, .5 or .8. In the Figure 2 simulations the tests were directional, so a variable counted as a ghost only if the difference ran in the predicted direction. The true effect, where present, was d = .3 on one variable. The p-curve is examined only in the range 0 to .05.

## Results: correlated versus uncorrelated variables

With no true effect and ghost p-hacking, the p-curve is flat when the variables are uncorrelated. When the variables are correlated it has a negative (left) skew, with the slope growing with the strength of the correlation. In the Figure 2 simulations the false positive rate is around 40% when the variables are uncorrelated and drops to around 12% when they are inter-correlated at r = .8. The false positive rate rises with the number of variables (8 against 3), which the paper describes as the familiar inflation from multiple comparisons.

The paper explains the skew as an effect of sampling one p-value per study. If all p-values from all runs are plotted, the distribution is uniform whatever the correlation. But when variables are correlated their p-values are correlated too, so the range of p-values within a single run is narrower (Table 1 shows ten runs at r = 0 and ten at r = .8). In the limiting case of multicollinear variables, a run behaves like a single test with the run's median p-value. If the median is well below .05, most p-values in the run are eligible for selection; if the median is just above .05, only the values close to the boundary are eligible. Selection with a cutoff therefore distorts the distribution towards .05. With uncorrelated variables there is no such constraint and all values below .05 are equally likely.

With a true effect of d = .3 on one variable, the p-curve shows the expected right skew. The extent of the skew depends on statistical power and shows little effect of the number of dependent variables. Appendix S2, not in the extracted source, is said to show that without p-hacking the p-curve is flat under the null and similarly right-skewed under d = .3, with no influence of correlation in either case.

## Masking of right skew

The paper reports that when power is low and the variables are highly correlated, including a proportion of p-hacked studies can cancel the right skew that true effects produce, because of the left skew that ghost p-hacking with correlated variables induces (Figure 3). It presents this as one example of how combinations of parameters that are unknown in practice (the proportion of p-hacked studies, sample size, and the number and correlation of dependent variables) can produce unexpected p-curves. It says such cases appear to contradict the general rule, quoted from Simonsohn, Nelson and Simmons (2014), that any set of studies containing some true effects should give a right-skewed p-curve. The paper's stated position is that a p-curve must not be taken as definitive evidence of the presence or absence of p-hacking or evidential value, though it can indicate that something is problematic.

## Power of the near-bin versus far-bin test

The paper examines the test used by Head et al. that compares the number of p-values in a far bin (.04 < p < .045) with a near bin (.045 < p < .05). It lists five things the bin counts depend on: the number of studies in the p-curve, the proportion of studies with ghost p-hacking, the number of variables, the sample size, and the correlation between variables.

It then takes an extreme case designed to maximise the difference: no true effects, ghost p-hacking in every study, and eight variables inter-correlated at .8. Even here the left skew is described as slight. Simulated data were used to estimate the proportions in the near and far bins and the power to detect the difference. To reach 80% power, around 1,200 p-values in the range .04 to .05 are needed. Only 4% of simulated studies had a p-value in that range, so the paper concludes that around 30,000 studies would be needed to detect the p-hacking bump with 80% power in the situation where ghost p-hacking makes the largest difference (Figure 4, which the paper notes has the saw-tooth pattern typical of such power curves).

## The text-mined dataset

The paper describes the Head et al. study as follows: all available open-access papers were downloaded from PubMed, categorised by subject area, and text-mined for p-values in the range 0 to .05 in Abstracts and Results sections; one p-value was randomly sampled per paper, the sampling was repeated 1,000 times, and the rounded average count per bin was used. The number of papers per discipline ranged from 94 in Mathematical Sciences to over 60,000 in Medical and Health Sciences. The paper calls this, to its knowledge, the largest study of p-hacking in the literature, and says the merit of its massive data comes with a lack of control over which p-values enter the analysis.

### Ambiguous p-values

The paper states that Head et al. included only p-values given exactly, with an equals sign, and reported to at least three decimal places, so that values given as "less than", which are common for very low values such as p < .001, were omitted.

The authors manually checked a random subset of 30 of the 1,736 papers classified by Head et al. as Psychology and Cognitive Sciences. The average number of significant p-values reported per paper was 14.1, with a range of 2 to 43. If values given as < .01 or < .001 were counted in the lowest bin (0 to .025), the average number of p-values per paper in that bin was 9.97; if they were excluded, as in Head et al., it was 4.47. The paper reads this as around half of the extreme p-values having been excluded even though they could have been assigned accurately to the lowest bin. It adds that including them might have exposed Head et al. to a charge of bias in favour of extreme values, so the approach taken was very conservative and reduced the power of the test. It also notes that the number of decimal places varies between papers, so that a value such as p = .04 may be exact or rounded, and that different rules for handling this give different distributions.

### Unsuitable p-values

Scrutiny of the same 30 papers raised three issues.

1. Most serious in the paper's view: many p-values related to facts that were well established or expected a priori and were not the focus of the main hypothesis, apparently reported for completeness or reassurance. The examples given are a very low p-value for the association between depression and suicidality (paper 1); a learning effect at p < .001 in a study of music and verbal learning, which then produced further significant linear and quadratic trend tests (p = .004 and p < .001) (paper 10); a check that negative photographs elicited more negative emotion than positive ones, p < .001 (paper 11); and a highly significant Stroop effect in a study of bilinguals (paper 20). The paper says examples of this kind could be found in virtually all of the papers examined, and that such p-values could exaggerate evidential value.

2. Some papers showed double-dipping. The example is an event-related potential study (paper 6) in which a time window where two conditions differed was chosen by inspecting average waveforms and then mean amplitudes in that window were compared. The paper says this form of p-hacking generates p-values well below .05, so it would not be detected by looking for a bump just below .05 and would instead give a false impression of evidential value. In support it cites Vul et al. (2009) on circular analysis in brain imaging, and calculates that a correlation of 0.74 with N = 16 would give p < .001.

3. P-values from tests of a method's assumptions, or from model-fitting where a low p-value means poor fit, are also unsuitable. These were rare in the audited papers: two reported Mauchly's test of sphericity, only one of them exactly (p = .001), and none reported model-fitting statistics. The paper judges these unlikely to affect a p-curve except in sub-fields where such statistics are common.

Table 2 of the paper summarises the problems in two columns. Cases where p-hacking would not be detected by the binomial test: p-values reported as p < .05 and so excluded; limited power because few p-values fall between .04 and .05; p-values ambiguous because rounded to two decimal places. Cases where a right skew is not due to evidential value: p-values confirming prior characteristics of the groups compared; p-values confirming well-known effects, such as that a method behaves as expected; double-dipping; and p-values from model-fitting or assumption tests. The table marks most of these as potentially avoidable by analysing data from meta-analyses, and several as less likely to affect text-mined data from Abstracts.

## What the paper claims

On text-mined data, the paper argues that the Results-section p-values used by Head et al. do not meet the first of the three criteria it attributes to Simonsohn and colleagues for valid p-curve inference: that the p-values test the hypothesis of interest, are uniform under the null, and are independent of each other. Selecting one p-value at random per paper avoids dependence but admits unsuitable p-values. It concludes that this makes it unfeasible to use the p-curve to quantify the extent of p-hacking or evidential value from text-mined data.

On Abstracts, the paper says most of the problems are less likely to apply, because p-values reported there are likely to concern the most important findings (citing De Winter and Dodou, 2015). But reporting p-values in Abstracts is optional, the decision to report may depend on the size of the p-value, and power is hard to achieve: it notes that Head et al. found evidence of p-hacking in only two of the ten subject areas analysed from Abstracts, and that in six areas fewer than ten p-values fell between .04 and .05.

On meta-analyses, the paper says many of the problems can be avoided because the p-values have been selected to test specific hypotheses, and that Head et al. included such an analysis for that reason. It adds that the approach is labour-intensive and has limited power to detect p-hacking when the total number of p-values between .04 and .05 is small, pointing to Head et al.'s Table 3.

More generally, the paper argues that the binomial test cannot be used to quantify the amount of p-hacking, and that this applies to all p-curves, not only text-mined ones. Ghost p-hacking does not usually produce a significant difference between the adjacent bins near .05: with uncorrelated or weakly correlated variables the p-curve is flat, and with correlated variables the left skew is too small to detect without very large numbers of studies. A near-bin versus far-bin test therefore gives a conservative estimate of p-hacking. To model a p-value distribution one needs to know (drawing on Lakens, 2015) the number of studies with true and null effects, the type I error rate, power and publication bias, to which the paper adds whether dependent variables were correlated, whether p-values tested a specific hypothesis, and how many were excluded for ambiguous reporting.

On evidential value, the paper accepts that right skew indicates evidential value, but argues that with heterogeneous data the extent cannot be quantified from the degree of skew, because the skew depends on power, and because ghost p-hacked correlated variables have little effect at high power but can cancel the right skew completely at low power.

The paper's conclusions: the absence of a bump in the p-curve does not indicate the absence of p-hacking; a right-skewed p-curve cannot be treated as an indicator of the extent of evidential value without a model specific to the type of p-values entered; and it is not feasible to use the p-curve to estimate the extent of p-hacking and evidential value unless there is considerable control over the data entered. P-hacking with ghost variables in particular is likely to be missed. The authors say they share Head et al.'s concern about the damage p-hacking does, quote Head et al.'s conclusion that p-hacking is probably common but weak relative to real effect sizes, and reply that relying on a bump below .05 will miss much p-hacking that goes "under the radar". They allow that p-curve analysis still has a place where a set of p-values from studies testing one hypothesis meets the criteria of Simonsohn and colleagues, but hold that simple comparisons between ranges of p-values from disparate studies cannot quantify either p-hacking or real effects.

## What the paper concedes

- Ghost variables are only one method of p-hacking, and the bump observed by Head et al. could have arisen for other reasons; the paper notes that Head et al.'s own meta-analysis showed authors misreporting non-significant p-values as significant to be a contributing factor.
- The simulations model a true effect on a single variable and examine only the range 0 to .05.
- The power analysis concerns the extreme case chosen to maximise the ghost p-hacking difference; the paper does not report power for other parameter settings.
- The audit covers 30 papers from one discipline category, Psychology and Cognitive Sciences, out of 1,736 in that category.
- Examples of assumption-test and model-fit p-values were rare in the audited papers, so that problem is judged unlikely to matter outside sub-fields where such statistics are common.
- Head et al.'s exclusion of "less than" p-values is described as very conservative rather than as a bias in Head et al.'s favour.
- The paper says the p-curve can indicate that something is problematic even though it cannot be treated as definitive evidence either way.

## Cited by

- [[p-curve-as-evidence]]
- [[text-mined-p-values]]
- [[what-p-hacking-is]]
- [[p-hacking-and-meta-analysis]]
- [[preregistration-as-a-remedy]]
- [[judgement-p-curve-dispute]]
