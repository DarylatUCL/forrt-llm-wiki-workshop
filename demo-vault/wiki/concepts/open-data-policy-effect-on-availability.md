---
type: concept
title: "Do mandatory open data policies increase data availability and reusability?"
description: What a pre-/post-evaluation of one journal's mandatory open data policy found about the frequency of data-available statements and the in-principle reusability of shared data, the causal threats such a non-randomised design faces, what a landscape survey of 318 biomedical journals found about how common and how strong such policies are and what predicts having one, and what each source concedes about its own limits.
created: 2026-09-04
updated: 2026-09-28
sources: [hardwicke-2018, vasilevsky-2017]
status: draft
generated:
  by: claude-code/claude-sonnet-5
  at: 2026-09-04
---

# Do mandatory open data policies increase data availability and reusability?

Making data available is only useful if the data are also reusable: accessible, complete, and understandable [[hardwicke-2018]]. This page collects what the wiki's sources report about whether, and how often, a journal-level policy changes either of those things. One source evaluates the before/after effect of one journal's own mandatory policy [[hardwicke-2018]]; a second surveys the prevalence and strength of such policies across 318 biomedical journals and what predicts having one, without measuring any policy's effect on the articles published under it [[vasilevsky-2017]]. The two ask different questions about the same institutional lever, and the page keeps their figures separate rather than combining them; see "How the two sources relate" below.

## The policy and the evaluation design

The source evaluates the mandatory open data policy introduced at the journal *Cognition* on 1 March 2015, which required authors to make their data publicly available, in a form enabling reuse and reproduction, before publication [[hardwicke-2018]]. The evaluation is a retrospective, quasi-experimental pre-/post-design: 591 empirical articles published in the journal from March 2014 to March 2017, split by submission date into 417 pre-policy and 174 post-policy articles, coded by five trained coders for whether each article carried a data available statement (DAS) and, where it did, whether the data were accessible, complete and understandable [[hardwicke-2018]]. The design was not a randomised manipulation; the source states this explicitly and reasons about the causal threats that follow from it, described below [[hardwicke-2018]].

## Data availability statements

DAS inclusion rose from 25% of pre-policy articles (104/417, CI [21, 29]) to 78% of post-policy articles (136/174, CI [71, 84]), chi-squared(1, n = 591) = 144.18, p < 0.001 [[hardwicke-2018]]. An interrupted time-series analysis, fitted to estimate the policy's effect net of any pre-existing secular trend, found a pre-policy trend of 1.04-fold higher DAS probability per 50 days (CI [1.02, 1.06], p = 0.002), a level change at the policy's introduction of 1.53-fold (CI [1.10, 1.90], p = 0.017), and a post-policy trend 1.14-fold steeper than the pre-policy trend (CI [1.04, 1.26], p = 0.010) [[hardwicke-2018]]. Almost all data-available statements pointed to *Cognition*'s own supplementary materials (208 articles, 87%) rather than a third-party repository (27, 11%), a personal webpage (2, 1%) or other means (3, 1%); none pointed to "available upon request" [[hardwicke-2018]].

## In-principle reusability

Among articles with a DAS, in-principle reusable data (successfully downloadable, complete raw data, and understandable without further contact) rose from 22% of pre-policy DAS articles (23/104; 6% of all 417 pre-policy articles) to 62% of post-policy DAS articles (85/136; 49% of all 174 post-policy articles), chi-squared(1, n = 591) = 154.38, p < 0.001 [[hardwicke-2018]]. This comparison was exploratory rather than preregistered [[hardwicke-2018]]. Only 18 of the sampled articles included analysis scripts at all, and of those only 8 accompanied data judged reusable [[hardwicke-2018]].

## Causal threats the source names for its own design

Because the design compares articles before and after the policy rather than randomising it, the source names several threats to a causal reading of the above figures, and reports what it did to address them [[hardwicke-2018]]. A "maturation" threat: authors submitting to the journal may simply have grown more aware of open-science norms over the same period, independent of the policy [[hardwicke-2018]]. Anticipatory effects: the editorial announcing the policy was available online about four months before the policy took effect, which could shift behaviour ahead of the formal start date [[hardwicke-2018]]. Concurrent events: the source names the Open Science Collaboration's 2015 replicability study as a candidate for a co-occurring influence on the field, while stating it is not aware of any event coinciding specifically with the moment DAS rates changed [[hardwicke-2018]].

The source also raises self-selection, or "population shift": researchers already inclined toward transparency might have been drawn to submit to the journal by the new policy, while others were deterred, which would make the observed increase overestimate the policy's effect on researchers not already so inclined [[hardwicke-2018]]. Two further exploratory checks (not preregistered) partly address this without ruling it out: a yearly "author retention index" was stable both before and after the policy, suggesting no evidence that a persistent group of returning authors was deterred, though the source notes these are also the authors least likely to leave a journal regardless; and overall journal productivity increased rather than fell after the policy took effect, which the source reads as inconsistent with large-scale author deterrence, while allowing that a larger number of newly attracted authors could mask a smaller number who were deterred [[hardwicke-2018]].

## What the source concedes about its own reusability assessment

The source states plainly that its reusability judgements (accessible, complete, understandable) were based on "relatively brief visual inspection" of each dataset and are therefore likely to underestimate how reusable the data actually are in practice [[hardwicke-2018]]. Coders were not blind to the study's hypotheses, though the source judges the risk of bias from this to be low because the coding protocol left little room for subjective interpretation [[hardwicke-2018]].

## How common and how strong are journal data-sharing policies

A landscape survey of 318 biomedical journals, sampled from the top quartile by impact factor or publishing volume within a defined set of Web of Science categories, scored each journal's own editorial policy on a six-level rubric from "required as a condition of publication" (DSM 1) to "no mention" (DSM 6) [[vasilevsky-2017]]. Only 11.9% of journals required data sharing as a condition of publication, and a further 9.1% required it without stating the consequence for publication decisions; 23.3% encouraged but did not require sharing, 9.1% mentioned it only indirectly, 14.8% addressed only omics data, and 31.8% made no mention of data sharing at all [[vasilevsky-2017]]. Weighted by publishing volume the picture is less stark: the 21.1% of journals that required sharing published 42.1% of the sampled journals' citable items in each of 2013 and 2014, though much of that share came from a single very high-volume journal [[vasilevsky-2017]].

Among the policies that did address data sharing, guidance was sparse on the specifics that would make shared data actually reusable: only 7.3% of such journals mentioned copyright or licensing, and only 2 of the full 318 journals said anything about how long data should be retained [[vasilevsky-2017]]. Most journals that addressed sharing at all recommended a public online repository as the method, and most of those that recommended journal hosting did not specify any file-size limit [[vasilevsky-2017]].

## What predicts a strong policy

Impact factor was significantly associated with policy strength: the median IF for journals requiring data sharing (as a condition of publication) was more than double that of journals with no mention of it, and this held after collapsing the six-level scheme to a simple required/not-required split [[vasilevsky-2017]]. Open-access status was not: at the journal level, open-access and subscription journals were not significantly different in how likely they were to require data sharing, though at the level of individual articles, an open-access article was much more likely to come from a journal that required sharing, an association the source attributes largely to the volume of one very productive open-access journal in its sample [[vasilevsky-2017]].

## How the two sources relate

Both sources concern the same institutional lever, a journal's own data-sharing policy, but they measure different things and their figures are not placed side by side here. The landscape survey reports what fraction of 318 journals have a policy of each strength, and what predicts having one; it does not measure whether any journal's articles became more available or reusable as a result of adopting a policy [[vasilevsky-2017]]. The single-journal evaluation reports the opposite: a before/after change in one journal's own article-level data availability and reusability, not the prevalence of policies across journals [[hardwicke-2018]]. A prevalence figure from the landscape survey (for instance, that 11.9% of journals require sharing) and an article-level rate from the single-journal evaluation (for instance, that 78% of that journal's post-policy articles carried a data-available statement) answer different questions, on different denominators, and neither source draws a comparison between them; the wiki does not construct one either.

The landscape survey does note, in its own discussion, that most existing policies (of whatever strength) give little specific guidance on licensing, retention or hosting method [[vasilevsky-2017]]. The single-journal evaluation reports a different gap: only 18 of its sampled articles carried an analysis script at all, and only 8 of those paired it with data judged reusable [[hardwicke-2018]]. Neither source measures the other's setting, and the wiki does not treat the two gaps as a shared finding.

## Related pages

- [[analytic-reproducibility-from-shared-data]] for what happened when the single-journal evaluation's team tried to use that policy's reusable data to reproduce reported findings.
