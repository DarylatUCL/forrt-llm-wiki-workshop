---
type: concept
title: "Are text-mined p-values suitable for p-curve analysis?"
description: Whether p-values harvested automatically from published papers meet the conditions p-curve analysis requires, what a manual audit of such data found, how Results sections, Abstracts and meta-analyses compare as sources, and what the mix of experimental and observational designs behind them does to the inference.
created: 2026-09-04
updated: 2026-09-04
sources: [head-2015, bishop-2016, hartgerink-2017, bruns-2016]
status: draft
generated:
  by: claude-code/claude-fable-5-1
  at: 2026-09-04
---

# Are text-mined p-values suitable for p-curve analysis?

Text-mining lets a p-curve be built from very large numbers of papers, but the p-values it harvests are whatever the papers report, not p-values chosen to test a particular hypothesis [[bishop-2016]]. They are also reported values, which cannot be recalculated from test statistics and carry the rounding habits of the authors who wrote them [[hartgerink-2017]]. This page collects what the sources say about that trade-off. For the logic of reading a p-curve, see [[p-curve-as-evidence]].

## How text-mined p-curves have been built

Head et al. text-mined p-values from all open-access papers in PubMed, analysed p-values from Results sections and from Abstracts separately, took the mean bin count over 1,000 bootstraps that drew one p-value per Results section or Abstract, and excluded disciplines with fewer than 50 significant p-values, leaving 14 disciplines for Results and 10 for Abstracts [[head-2015]]. They say they adopted counter-measures against the recognised weaknesses of text-mining, described in a supplementary text that is not part of the wiki's source [[head-2015]].

Bishop and Thompson report that Head et al. included only p-values stated exactly, with an equals sign, and to at least three decimal places, so that values given as "less than" were omitted, and that the number of papers per discipline ranged from 94 in Mathematical Sciences to over 60,000 in Medical and Health Sciences [[bishop-2016]]. They describe it as the largest study of p-hacking they know of [[bishop-2016]].

Hartgerink describes the same dataset as over two million p-values mined from the Open Access subset of PubMed Central, which indexes the biomedical and life sciences, and notes that the text-mining captured every reported p-value, including lone values with no accompanying test statistic; the analysed subset, which the reanalysis reuses, is the significant p-values that were reported exactly [[hartgerink-2017]]. Because no test statistics travel with the p-values, the dataset does not allow them to be recalculated [[hartgerink-2017]].

## What a manual audit found

Bishop and Thompson hand-checked 30 of the 1,736 papers that Head et al. classified as Psychology and Cognitive Sciences [[bishop-2016]]. The papers reported on average 14.1 significant p-values each, with a range of 2 to 43 [[bishop-2016]]. Counting values given as < .01 or < .001 in the lowest bin (0 to .025) gave an average of 9.97 such p-values per paper; excluding them, as Head et al. did, gave 4.47, which Bishop and Thompson read as around half of the extreme p-values having been left out even though they belonged in the lowest bin [[bishop-2016]]. They call Head et al.'s rule very conservative, and say it reduced the power of the test rather than biasing it towards finding extreme values [[bishop-2016]].

The audit also found p-values that Bishop and Thompson judge unsuitable for a p-curve. In virtually all of the 30 papers, some p-values tested facts that were already well established or expected, such as a Stroop effect or a check that emotional stimuli worked as intended, rather than the paper's main hypothesis [[bishop-2016]]. Some papers used double-dipping, choosing a time window or region by inspecting the data and then testing it, which Bishop and Thompson say produces p-values well below .05 and so mimics evidential value rather than a p-hacking bump [[bishop-2016]]. P-values from assumption tests or model fit were rare, two papers reporting Mauchly's test and none reporting model-fitting statistics [[bishop-2016]].

Bishop and Thompson also note that papers differ in how many decimal places they report, so a value such as p = .04 may be exact or rounded, and that different rules for handling this give different p-curves [[bishop-2016]].

## How reported p-values are rounded

Hartgerink plotted the exactly reported significant p-values at a binwidth of .00125 and found systematically more of them at .01, .02, .03, .04 and .05 than at neighbouring three-decimal values, where a smooth, decreasing curve would be expected [[hartgerink-2017]]. The reading offered is that authors tend to report to two decimal places, so that p = .041 becomes p = .04 and p = .046 becomes p = .05; the paper's post-hoc explanation is that three-decimal reporting is a recent standard, prescribed in psychology only from the 2010 APA manual, and it supposes other fields report to two decimals most of the time [[hartgerink-2017]]. This is the pattern Bishop and Thompson anticipated when they noted that p = .04 may be exact or rounded and that different handling rules give different p-curves [[bishop-2016]]; Hartgerink shows it in the data and builds the choice of bins around it [[hartgerink-2017]]. For the effect on the p-hacking test, see [[p-curve-as-evidence]].

Hartgerink argues that reporting tendencies cannot be removed from this dataset, and so must be handled in the analysis, because the p-values cannot be recalculated; the paper cites earlier work (Hartgerink et al., 2016; Krawczyk, 2015) as showing that the expected smooth distribution re-emerges when recalculated rather than reported p-values are inspected [[hartgerink-2017]].

A second reporting effect concerns the values Head et al. excluded. Bishop and Thompson's audit concerns "less than" values at the low end, such as p < .001 [[bishop-2016]]. Hartgerink raises the same exclusion at the high end: a p-value of .047 may be more likely to be reported as p < .05 than one of .037 as p < .04, and since every "p < X" value is dropped, p-values near .05 could be under-represented; the paper estimates the size of the asymmetry from a figure in Krawczyk (2015); the estimate is on [[hartgerink-2017]].

## Results sections versus Abstracts

Head et al. analysed both, and report that Abstract p-values are optional and therefore likely to be censored towards the strongest results, which would exaggerate evidential value and make p-hacking harder to detect, even though Abstract p-values are more likely to concern primary hypotheses [[head-2015]]. They found significant evidence of p-hacking in Abstract p-values for only two of the ten disciplines analysed, Multidisciplinary and Information and computing sciences, against four of fourteen for Results sections [[head-2015]].

Bishop and Thompson take the same view of Abstracts from the other direction: most of the problems they found in Results-section p-values are less likely to affect Abstracts, because p-values reported there tend to concern the most important findings, but reporting is optional, the decision to report may depend on the size of the p-value, and power is hard to achieve [[bishop-2016]]. They point out that in six of the ten Abstract subject areas fewer than ten p-values fell between .04 and .05 [[bishop-2016]].

Hartgerink's reanalysis kept the two sections separate and found that the surplus below .05 survived in Results sections but not in Abstracts: with bins of .03875 < p <= .04 against .04875 < p <= .05, the proportion in the upper bin was .583 for Results sections (26,047 against 18,664) and .358 for Abstracts (4,597 against 2,565), with the Results-section excess significant and no discipline individually significant for Abstracts [[hartgerink-2017]].

## Which research designs the p-values come from

Bruns and Ioannidis raise a problem with harvested p-values that is separate from which hypothesis each one tests: the design of the study behind it. Text-mined p-values, they note of Head et al.'s data, stem from both experimental and observational research designs, and they define observational research as any study without randomisation in the comparison of interest, which they say makes up the large majority of the scientific literature, citing a count of PubMed entries by Dal-Ré et al. (2014) [[bruns-2016]]. In observational research, on their account, a null effect combined with even a tiny omitted-variable bias produces a right-skewed p-curve as the sample grows, so a right skew in a p-curve that mixes designs does not show that the studies analyse true effects [[bruns-2016]]. They say Head et al.'s main result, that most studies in various disciplines analyse true effects, rests on that assumption, which may be false for observational research, and that little can be learned from such studies beyond an indication that p-curves may be right-skewed across some disciplines, the sources of the skew remaining unexplained [[bruns-2016]]. None of the sources reports design-stratified results for these datasets, so the wiki cannot say how the mix would separate. For the simulations behind this objection, see [[p-curve-as-evidence]].

## Meta-analyses as an alternative source

Both sources treat p-values collected for meta-analyses as a way round the problem, because those p-values were selected to test specific hypotheses [[head-2015]] [[bishop-2016]]. Head et al. ran such an analysis on twelve sexual-selection meta-analyses alongside their text-mining [[head-2015]]. Bishop and Thompson say this is why Head et al. included it, and add that the approach is labour-intensive and has limited power to detect p-hacking when few p-values fall between .04 and .05 [[bishop-2016]]. What that analysis found is on [[p-hacking-and-meta-analysis]].

## Where the sources agree and where they disagree

Both sources agree that text-mined data pool many kinds of statistical test. Head et al. concede that this means their p-curves cannot show whether some fields or questions within a discipline have a flat p-curve [[head-2015]]. Bishop and Thompson go further and say the Results-section p-values fail the requirement, which they attribute to Simonsohn and colleagues, that p-values in a p-curve test the hypothesis of interest [[bishop-2016]].

The disagreement is about what follows. Head et al. take the finding of a surplus just below .05 in both Results and Abstract p-values as supporting their conclusion that p-hacking is widespread [[head-2015]]. Bishop and Thompson argue that because unsuitable p-values inflate the appearance of evidential value, and because "less than" values and low power blunt the p-hacking test, text-mined p-curves cannot be used to quantify either the extent of p-hacking or the extent of evidential value [[bishop-2016]].

Hartgerink agrees with Bishop and Thompson that detection, if attempted, should be done at the paper level after careful scrutiny of which results are included, and cites them for it [[hartgerink-2017]] [[bishop-2016]]. The paper's own departure from Head et al. is narrower: it takes the text-mined data as given and reports that the surplus just below .05 disappears once p = .045 and p = .05 are kept and the bins respect two-decimal reporting [[hartgerink-2017]]. Head et al. exclude p = 0.05 on the stated suspicion that many researchers do not regard it as significant [[head-2015]]; Hartgerink calls that assumption potentially invalid, citing Nuijten et al. (2015), and adds that strategic rounding down to p = .05 is a form of p-hacking the exclusion removes from view [[hartgerink-2017]].

Bruns and Ioannidis dispute a different inference from the same data: not the surplus below .05 but the right skew. Head et al. read the strong right skew in every discipline as evidence that researchers predominantly study non-zero effects [[head-2015]]; Bruns and Ioannidis hold that for the observational studies in a text-mined corpus the skew is equally consistent with null effects and omitted-variable bias [[bruns-2016]]. Their objection and Bishop and Thompson's converge on the conclusion that a text-mined right skew cannot be read as a measure of evidential value, but for different reasons: Bishop and Thompson because many harvested p-values test the wrong hypothesis and the skew depends on power [[bishop-2016]], Bruns and Ioannidis because the study design behind a harvested p-value can generate skew without a true effect [[bruns-2016]].

The wiki records three open disagreements: whether the text-mined p-curves license an estimate of extent, which Head et al. assume and Bishop and Thompson deny; whether the surplus below .05 is present in the data at all once the analytic choices are varied, which Head et al. report and Hartgerink does not find; and whether the right skew shows true effects, which Head et al. conclude and Bruns and Ioannidis deny for the observational part of the data. The features of the data that each source describes are not themselves disputed by the others.

## Related pages

- [[p-curve-as-evidence]] for the inference the data are meant to support.
- [[p-hacking-and-meta-analysis]] for the meta-analysis route.
- [[what-p-hacking-is]] for the practices at issue.
