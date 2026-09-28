---
type: concept
title: "Does p-hacking distort the conclusions of meta-analyses?"
description: Whether p-hacking in primary studies changes the pooled effect sizes or qualitative conclusions of meta-analyses, how meta-analysts can check, and how pooling can itself be used to obtain significance.
created: 2026-09-04
updated: 2026-09-28
sources: [head-2015, bishop-2016, wicherts-2016]
status: draft
generated:
  by: claude-code/claude-opus-5
  at: 2026-09-04
---

# Does p-hacking distort the conclusions of meta-analyses?

Meta-analyses combine effect sizes across studies after weighting each by its reliability, and are only as good as the studies they pool [[head-2015]]. If p-hacking inflates the effect sizes in primary studies, the pooled estimate inherits the inflation [[head-2015]].

## What the sources report

Head et al. obtained p-values for the primary studies behind 12 published meta-analyses on sexual selection in evolutionary biology and tested each set for evidential value and p-hacking [[head-2015]]. Nine of the 12 showed significant evidential value, and the three that did not had the smallest samples [[head-2015]]. With 16 p-values that had been misreported as p < 0.05 included, 7 of 12 sets had more p-values in the 0.045 to 0.05 bin than in the 0.04 to 0.045 bin, the pooled proportion in the upper bin was 0.615 (lower CI 0.513), p = 0.033, and one dataset, Jiang et al. (2013) on assortative mating, was individually significant (7 against 17, p = 0.032) [[head-2015]]. With the misreported p-values excluded, the pooled proportion fell to 0.489 (lower CI 0.375), p = 0.443, and the individual signal in Jiang et al. disappeared (7 against 11, p = 0.240) [[head-2015]].

## Meta-analysed p-values as inputs to a p-curve

Both sources treat p-values gathered for a meta-analysis as better inputs for a p-curve than text-mined ones, because they were chosen to test a specific hypothesis [[head-2015]] [[bishop-2016]]. Bishop and Thompson say this is why Head et al. included the analysis, and that it avoids most of the problems they found in text-mined data, but that it is labour-intensive and has limited power to detect p-hacking when few p-values fall between .04 and .05, which they say is the case in Head et al.'s twelve datasets [[bishop-2016]]. They also note that Head et al.'s meta-analysis data showed misreporting of non-significant p-values as significant to be a contributor to the bump below .05 [[bishop-2016]].

## The position taken by Head et al.

Head et al. read their results as indicating that studies on questions important enough to warrant a meta-analysis tend to be p-hacked, but that the effect seems weak relative to the real effect sizes being measured, so p-hacking probably does not drastically alter conclusions drawn from meta-analyses [[head-2015]]. For the one dataset with a significant signal, they argue the qualitative conclusion is unlikely to change because evidential value was strong and the 0.045 to 0.05 bin held only a small share of the significant p-values, while allowing that the mean effect size might have been inflated [[head-2015]].

Two reasons are offered for why meta-analyses may be robust: the studies most susceptible to p-hacking are small ones, which get less weight, and, at least in ecology and evolution, meta-analyses often draw on data that were secondary to the original paper's aim and so less likely to be p-hacked [[head-2015]].

## Where the sources disagree

Bishop and Thompson quote Head et al.'s conclusion that p-hacking is probably common but weak relative to real effect sizes, and reply that a small bump below .05 does not measure a small amount of p-hacking [[bishop-2016]]. In their simulations, p-hacking by ghost variables leaves no bump at all when the variables are uncorrelated and only a slight one when they are correlated [[bishop-2016]]. In their manual check of 30 of Head et al.'s text-mined papers they also found double-dipping, which can produce p-values well below .05, so relying on the bump will miss p-hacking that goes "under the radar" [[bishop-2016]]. They say they share Head et al.'s concern about the damage p-hacking does [[bishop-2016]].

The disagreement is about inference, not about the twelve datasets: Head et al. treat the size of the near-bin excess as informative about how much p-hacking there was and hence about how much the pooled effects could be inflated [[head-2015]], while Bishop and Thompson hold that the near-bin test is at best a conservative detector and cannot bound the amount of p-hacking [[bishop-2016]]. Neither source reports a direct estimate of how much any pooled effect size was inflated. The wiki records the disagreement as unresolved.

## Pooling as an instrument of p-hacking

The page so far treats the meta-analysis as the victim of p-hacking in the studies it pools. Wicherts and colleagues add the reverse case. Among the design choices on their checklist is failing to specify a sampling plan, which they say allows a researcher to run several small studies and present only the best, and also allows small underpowered studies to be pooled by an ad hoc meta-analysis in order to obtain a statistically significant result; they cite Ueno et al. (2016) for the latter [[wicherts-2016]]. The meta-analysis at issue there is the within-article pooling of a paper's own studies, not the published meta-analyses of a literature that the rest of this page concerns, and Wicherts and colleagues report no data on how often it happens [[wicherts-2016]].

Their paper also supplies the premise the rest of this page rests on, from the other direction. They state that strategic use of researcher degrees of freedom may inflate effect size estimates, attributing the point to earlier work by Ioannidis, Bakker and colleagues, Simonsohn and colleagues, and van Aert and colleagues, and treat that inflation as one of the two reasons researcher degrees of freedom matter, alongside the raised chance of a false positive [[wicherts-2016]]. This is a claim about the mechanism rather than a measurement of it: the paper reports no data and no simulation [[wicherts-2016]].

One entry on their checklist bears directly on the twelve datasets above. Misreporting results and p-values, for instance presenting a non-significant result as significant, is listed as a researcher degree of freedom in the reporting phase [[wicherts-2016]], and the p-hacking signal Head et al. found in the twelve datasets was present only when 16 p-values misreported as p < 0.05 were counted [[head-2015]]. Wicherts and colleagues offer no estimate of how often such misreporting occurs, so the two sources meet only in naming the practice, not in measuring it.

## Checks proposed for meta-analysts

Head et al. recommend that meta-analyses report the p-value attached to each effect size, which they say is not standard practice, and then test the set for evidential value and p-hacking [[head-2015]]. To gauge sensitivity they suggest randomly removing the number of studies that make up the hump just below 0.05, or estimating the effect size from the p-curve using only significant results [[head-2015]]. They add that p-curve methods are still developing and that real data are likely to violate assumptions of the simulations used to test them [[head-2015]].

Bishop and Thompson add that other bias-correction techniques used in meta-analysis, such as trim and fill, rest on assumptions of their own and become hard to interpret when those are not met [[bishop-2016]].

## Qualifications that travel with these figures

The 12 datasets come from one field, sexual selection in evolutionary biology, and Head et al. concede that questions chosen for meta-analysis may not represent research questions generally [[head-2015]]. Whether the p-hacking signal appears depends on whether misreported p-values are counted, and Head et al. acknowledge that counting them could be argued to bias the test towards detection while maintaining that misreporting is part of p-hacking [[head-2015]]. Bishop and Thompson's claim that the near-bin test is underpowered on these datasets rests on their simulations of ghost variables, which is one form of p-hacking among several [[bishop-2016]].

## Related pages

- [[p-curve-as-evidence]] for the test applied to the primary studies.
- [[text-mined-p-values]] for the alternative source of p-values and its problems.
- [[what-p-hacking-is]] for the practices that produce the inflation.
- [[preregistration-as-a-remedy]] for what a preregistration would have to specify to prevent it.
