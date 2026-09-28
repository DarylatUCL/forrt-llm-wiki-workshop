---
type: source
title: "Hartgerink (2017), Reanalyzing Head et al. (2015): Investigating the robustness of widespread p-hacking"
description: A reanalysis of Head et al.'s text-mined p-values which finds that the bump below .05 disappears once p = .045 and p = .05 are kept and the bins are chosen around two-decimal reporting, while declining to conclude that p-hacking is absent.
created: 2026-09-04
updated: 2026-09-04
sources: [hartgerink-2017]
status: draft
generated:
  by: claude-code/claude-fable-5-1
  at: 2026-09-04
doi: 10.7717/peerj.3068
licence: CC0 1.0
---

# Hartgerink (2017), Reanalyzing Head et al. (2015): Investigating the robustness of widespread p-hacking

Hartgerink, Department of Methodology and Statistics, Tilburg University. PeerJ 5, e3068, submitted 10 September 2016, accepted 5 February 2017, published 2 March 2017. Sole author; no funding and no competing interests declared. Distributed under a Creative Commons public domain dedication (CC0). Supporting files are archived at Zenodo (doi 10.5281/zenodo.259624). The paper's Supplemental Information 1, which holds the per-discipline tests, is not part of the extracted source. The extraction lacks the title; it is taken from `corpus.md`.

## What the paper set out to do

The paper asks whether Head et al.'s (2015) conclusion that the distribution of reported p-values shows a systematic bump below .05, and hence evidence of p-hacking, is robust to justifiable changes in how the data are analysed. It separates this question from an epistemological objection it attributes to Simonsohn, Simmons and Nelson (2015), that analysing all reported p-values in research articles answers an inappropriate question about evidential value across all results. It notes that the models behind Head et al.'s finding had been discussed in preprints and publications (naming Bishop and Thompson, 2015 and 2016; Holman, 2015; Simonsohn, Simmons and Nelson, 2015; Bruns and Ioannidis, 2016), but that the data themselves had not been extensively reanalysed for robustness.

The inspection proceeds in three steps: explaining the data and the original and reanalysis strategies; re-evaluating the evidence for a bump below .05; and discussing whether the outcome means there is no widespread p-hacking.

## How the paper reads the p-value distribution

Without p-hacking, the p-values from a set of true and null results should form a mixture of the uniform distribution under the null hypothesis and right-skewed distributions under the alternative. P-hacking affects the distribution of statistically significant p-values and can produce a left skew below .05, a bump, but need not. The paper's example of a practice that can produce left skew is optional stopping (data peeking) when the null hypothesis is true.

From this the paper draws a distinction it applies throughout. A systematic bump below .05, meaning one not due to sampling error, is a sufficient condition for the presence of specific forms of p-hacking, and the paper says Head et al. "correctly argue" that an aggregate distribution could show such a bump when left-skew p-hacking is frequent. But the bump is not a necessary condition: optional stopping when there is a true effect, or running several analyses and reporting only the one with the smallest p-value, can occur without a bump. Finding no bump therefore does not exclude p-hacking on a large scale.

## The data

The paper describes Head et al.'s data as over two million p-values text-mined from the Open Access subset of PubMed Central, which indexes the biomedical and life sciences. The text-mining extracted every reported p-value, including those with no accompanying test statistic, so a lone "p < .05" was captured alongside a result such as t(59) = 1.75, p > .05. Head et al. then analysed the subset of statistically significant p-values (at alpha = .05) that were reported exactly, such as p = .043, and the reanalysis uses the same subset. The paper stresses that this dataset does not allow the p-values to be recalculated from test statistics.

The paper does not say whether it sampled one p-value per paper, as Head et al. describe doing; the bin counts it reports are described only as frequencies.

## Head et al.'s test as the paper describes it

Head et al. compared the frequencies in the last two bins below .05 at a binwidth of .005, .04 < p < .045 against .045 < p < .05, with a binomial test, taking a significantly higher frequency in the last bin as sufficient evidence of p-hacking. The paper identifies this as the Caliper test used earlier in publication bias research (Gerber et al., 2010; Kühberger, Fritz and Scherndl, 2014). The bins were chosen because Head et al. expected the signal to be strongest just below .05, regions nearer zero being more likely to hold evidence of true effects.

Two exclusions are singled out. Head et al. excluded p = .05 because, in the passage the paper quotes, they suspected that many authors do not regard p = .05 as significant. And p = .045 was excluded for the symmetry of the compared bins, so that it fell into neither bin.

## What the paper observed in the distribution

Figure 1 shows the significant p-values three ways: in green, the two bins Head et al. compared; in grey, the whole significant distribution at a binwidth of .00125 with p = .045 and p = .05 removed; and in black, the two bins those removals omit (.04375 < p <= .045 and .04875 < p <= .05).

The green bins show a bump below .05. The grey histogram does not clearly show one, which the paper says is because the appearance of a bump depends on which bins are compared. What the grey histogram does show is systematically more p-values at .01, .02, .03 and .04 (and at .05 once the black bins are added) than at neighbouring three-decimal values, from which the paper infers a tendency to report p-values to two decimal places rather than three: p = .041 may be rounded to p = .04, p = .046 to p = .05. The paper offers, and labels as post hoc, the explanation that three-decimal reporting is a recent standard, prescribed in psychology only from the 2010 APA manual after two-decimal reporting in the 1983 and 2001 editions, and supposes other fields report to two decimals most of the time.

On p = .045, the paper reports that once it is included there is no evidence of a bump: the frequency for .04 < p <= .045 is 20,114 against 18,132 for .045 < p < .05. It does not say whether these counts are for Results sections, Abstracts, or both. On p = .05, the paper argues that researchers treat p = .05 as significant more often than Head et al. supposed, citing a study by Nuijten et al. (2015), so the assumption behind the exclusion may not hold. It adds that if p-values are strategically rounded down, for example p = .054 reported as p = .05 (citing Vermeulen et al., 2015), that is itself a form of p-hacking, and excluding p = .05 removes those cases from the test and lowers its sensitivity to a bump.

## The reanalysis

Three analyses are reported, all on the same subset of exactly reported significant p-values.

1. Fisher's method over the whole range .04 < p < .05, which keeps p = .045. Each p-value is transformed as (p minus .04) divided by .01 so that the method tests for a surplus towards .05 (left skew) rather than towards zero. The result is chi-squared(76,492) = 70,328.86, p > .999: no evidence of a bump.

2. A Caliper test on bins chosen to take two-decimal reporting into account, .03875 < p <= .04 against .04875 < p <= .05 (binwidth .00125), keeping both p = .045 and p = .05. In Figure 1 these are the large grey bin at .04 and the rightmost black bin. The null hypothesis is that the proportion in the .05 bin is at most .5. A Bayesian Caliper test is added, computed with the BayesFactor package under an "ultrawide" prior (r = 1); the paper reads BF10 above 1 as the data being more likely under left-skew p-hacking and BF10 below 1 as more likely under no left-skew p-hacking. Results and Abstract sections are analysed separately.

3. A check on the paper's own bin choice, discussed under limitations below.

### Results of the adjusted-bin test

At binwidth .00125, Results sections held 26,047 p-values in .03875 < p <= .04 against 18,664 in .04875 < p <= .05, proportion .417, p > .999, BF10 < .001. Abstracts held 4,597 against 2,565, proportion .358, p > .999, BF10 < .001.

Sensitivity analyses at wider binwidths gave the same direction (Table 1):

- Binwidth .005 (.035 < p <= .04 against .045 < p <= .05): Abstracts 6,641 against 4,485, proportion .403; Results 38,537 against 30,406, proportion .441.
- Binwidth .01 (.03 < p <= .04 against .04 < p <= .05): Abstracts 9,885 against 7,250, proportion .423; Results 58,809 against 47,755, proportion .448.

Every one of these tests has p > .999 and BF10 < .001. Separated by discipline, the paper reports that no binomial test for left-skew p-hacking is significant in either Results or Abstract sections; the per-discipline figures are in Supplemental Information 1, which is not in the extracted source.

## What the paper claims

- The evidence for a bump below .05 presented by Head et al. is not robust to minor changes in the analysis: evaluating .04 < p < .05 continuously instead of in bins, which brings p = .045 back in, or choosing bins that respect the observed tendency to round to two decimals.
- Head et al.'s conclusion "might still be correct, but the data do not undisputably show so"; the evidence for widespread left-skew p-hacking is "ambiguous at best".
- Second-decimal reporting tendencies must be taken into account when choosing bins, because this dataset cannot eliminate them by recalculating p-values. The paper cites its own earlier work (Hartgerink et al., 2016) and Krawczyk (2015) as showing that the theoretically smooth distribution re-emerges when recalculated rather than reported p-values are inspected.
- Analyses on aggregated p-values can detect bump-producing p-hacking if it is widespread but cannot prove that no p-hacking occurs in individual papers. Two reasons are given: an ecological fallacy, since papers may show a bump at the paper level even when the aggregate does not; and the fact that some forms of p-hacking produce right skew, which these tests do not pick up and which is hard to detect in heterogeneous results. The paper's recommendation is that any attempt to detect p-hacking be made at the paper level, after careful scrutiny of which results are included, citing Simonsohn, Simmons and Nelson (2015) and Bishop and Thompson (2016).
- The absence of a bump below .05 "seems to be stronger than its presence throughout the literature". The paper names a reanalysis by Lakens (2014) of Masicampo and Lalande (2012) and two further datasets (Hartgerink et al., 2016; Vermeulen et al., 2015) as having found no bump, and concludes that claims of a bump need to be robust.

## What the paper concedes

- Choosing the bins just below .04 and .05 makes them non-adjacent, which may make the test less sensitive to a bump below .05. To address this the paper reran Head et al.'s original comparison with the second decimal included, .04 <= p < .045 against .045 < p <= .05, and again found no bump: proportion .431, p > .999, BF10 < .001. The paper does not say which section this figure is for.
- Restricting the data to exactly reported p-values may itself distort the distribution through rounding. A researcher with p = .047 may be more likely to report p < .05 than one with p = .037 to report p < .04; since every value reported as "p < X" is excluded, this could affect the results. The paper states that there is some indication the tendency to round up is stronger around .05 than around .04, by roughly a factor of 1.25, a figure it derives from a figure in Krawczyk (2015), which could leave p-values near .05 under-represented.
- Finding no evidence of a bump does not mean there is no p-hacking, since other forms of p-hacking do not produce one. The paper repeats this in the abstract, the introduction, the discussion and the conclusion.
- The explanation for two-decimal reporting in terms of publication-manual standards is offered as a post-hoc explanation.

## Cited by

- [[p-curve-as-evidence]]
- [[text-mined-p-values]]
- [[what-p-hacking-is]]
- [[judgement-p-curve-dispute]]
