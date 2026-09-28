---
type: question
title: "What do published p-values establish about how common p-hacking is?"
description: What the wiki's four p-curve sources say the distribution of published p-values can and cannot show about the prevalence of p-hacking, and the maintainer's recorded view on the dispute.
created: 2026-09-28
updated: 2026-09-28
sources: [head-2015, bishop-2016, hartgerink-2017, bruns-2016]
status: draft
generated:
  by: claude-code/claude-opus-5-5
  at: 2026-09-28
---

# What do published p-values establish about how common p-hacking is?

*Generated from the wiki on 2026-09-28. It reflects the pages listed below as they stood on that date and may go stale as sources are added.*

Drawn from [[p-curve-as-evidence]], [[text-mined-p-values]] and [[judgement-p-curve-dispute]].

## Short answer

On the wiki's sources, published p-values do not establish how common p-hacking is. One source reads a surplus of p-values just below .05 as showing p-hacking to be widespread [[head-2015]]. The other three dispute, on different grounds, that the data can carry that inference: that a surplus can measure extent at all [[bishop-2016]], that the surplus is there once reasonable analytic choices are varied [[hartgerink-2017]], and that the p-curve reads correctly in observational research [[bruns-2016]]. The sources do agree on one thing: the absence of a surplus does not show that p-hacking is absent [[hartgerink-2017]] [[bishop-2016]]. The dispute is open in the sources.

## What the positive finding is

Head et al. text-mined p-values from open-access PubMed papers and found, pooled across 14 disciplines, a proportion of 0.546 (one-tailed lower CI 0.536) in the bin 0.045 to 0.05 against the bin 0.04 to 0.045 for Results sections, and 0.537 (lower CI 0.518) across 10 disciplines for Abstracts, excluding p = 0.05 and p = 0.045 [[head-2015]]. They conclude that p-hacking is widespread [[head-2015]]. In their sexual-selection meta-analysis data the pooled result was significant only when 16 misreported p-values were included [[head-2015]].

## Why that does not settle prevalence

- **A surplus cannot measure extent.** Bishop and Thompson show by simulation that the bin counts depend on the number of studies, the proportion p-hacked, the number of dependent variables, sample size and their correlation, none of which is known in real data; they conclude that the extent of p-hacking cannot be estimated from a p-curve without considerable control over the data entered [[bishop-2016]]. Their power analysis needed around 30,000 studies for 80% power even in the case most favourable to detection [[bishop-2016]].
- **Some p-hacking leaves no surplus.** Ghost-variable p-hacking with uncorrelated variables produces no bump [[bishop-2016]]; optional stopping under a true effect, or reporting the smallest of several p-values, need not either [[hartgerink-2017]]; and p-hacking by omitted-variable bias in observational data produces right skew, not a bump [[bruns-2016]].
- **The surplus is not robust.** Reanalysing the same text-mined data with p = .045 and p = .05 kept and bins built around two-decimal reporting, Hartgerink finds no surplus: proportion .417 for Results sections and .358 for Abstracts, both p > .999 [[hartgerink-2017]]. Head et al. give a reason for excluding p = 0.05 [[head-2015]]; Hartgerink calls it potentially invalid [[hartgerink-2017]].
- **The inputs are mixed.** A hand check of 30 text-mined psychology papers found p-values testing established facts rather than main hypotheses, and double-dipping [[bishop-2016]]; the text-mined data mix experimental and observational designs, where a right skew need not show true effects [[bruns-2016]].

Bishop and Thompson add that a p-curve can still indicate that something is problematic [[bishop-2016]], and Hartgerink recommends detection at the level of the individual paper [[hartgerink-2017]].

## Where the sources disagree

The disagreement turns on three points, recorded as unresolved on [[p-curve-as-evidence]]: whether the tests measure extent or only detect (Head et al. against Bishop and Thompson); whether the surplus exists once analytic choices vary (Head et al. against Hartgerink); and whether right skew shows true effects (Head et al. against Bruns and Ioannidis for observational research) [[head-2015]] [[bishop-2016]] [[hartgerink-2017]] [[bruns-2016]].

The wiki's other evidence on how common questionable practices are comes from self-report surveys, a different method measuring different things; see [[prevalence-from-self-report]].

## The maintainer's recorded view

The wiki holds a judgement on this dispute, [[judgement-p-curve-dispute]]. What follows is the maintainer's view, not a finding of any source.

- **Verdict.** The maintainer's recorded view is that Bishop and Thompson are more persuasive than Head et al.: published p-value distributions do not show that p-hacking is widespread.
- **Reason.** The maintainer holds that the decisive limit is that a surplus just below .05 cannot establish how many studies were p-hacked, since some forms produce no surplus and its size depends on quantities real data do not reveal [[bishop-2016]]; that Head et al.'s surplus changes under Hartgerink's defensible reanalysis, whose paper-level sampling is unclear [[hartgerink-2017]]; and that Head et al. report their result correctly and document misreported p-values [[head-2015]], but neither settles prevalence.
- **What would change the maintainer's mind.** A reproducible analysis of focal, recalculated p-values, validated against known study-level analysis histories, showing that its signal reliably distinguishes widespread p-hacking from reporting and selection effects.

On what follows from that view beyond the dispute itself, for instance for research policy, the wiki has no recorded judgement.
