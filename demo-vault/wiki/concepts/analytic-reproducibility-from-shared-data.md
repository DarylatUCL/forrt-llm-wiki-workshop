---
type: concept
title: "When data are shared, can the reported analyses be reproduced?"
description: What one case-study evaluation of a sample of articles with in-principle reusable data found about analytic reproducibility, its error classification and article-level outcome scheme, what caused non-reproducibility, and what the source concedes about how optimistic its own estimate is likely to be.
created: 2026-09-04
updated: 2026-09-28
sources: [hardwicke-2018]
status: draft
generated:
  by: claude-code/claude-sonnet-5
  at: 2026-09-04
provisional: true
---

# When data are shared, can the reported analyses be reproduced?

Data being available and in-principle reusable does not by itself establish that the analyses reported from it can be repeated and the same outcomes obtained; that further question is analytic (or computational) reproducibility [[hardwicke-2018]]. This page collects what one source reports about attempting that check directly. It rests on a single source and carries `provisional: true` until a second paper speaks to it.

## Sample and method

The source assessed analytic reproducibility for 35 articles drawn from a pool of 108 articles already judged, in a companion evaluation of a mandatory data-sharing policy at one journal, to have in-principle reusable data; 47 were screened for eligibility and 12 rejected because no outcome met the criteria below, leaving 35 (5 pre-policy, 30 post-policy) [[hardwicke-2018]]. For each article, the target was a coherent set of descriptive and inferential statistics behind a "substantive" finding (one emphasised in the abstract, a figure or a table), reached through a "relatively straightforward" analysis of the kind covered in an introductory statistics course (e.g. correlations, t-tests, ANOVAs); the source concedes this selection involved subjective judgement [[hardwicke-2018]]. Each reproduction was run by a pilot and then verified by at least one co-pilot, working from the shared data, the original article and any accompanying documentation, and the original authors were contacted for assistance whenever problems arose [[hardwicke-2018]].

## How errors and outcomes were classified

Numerical discrepancies between a reported and a reanalysed value were expressed as a percentage error and classed as minor (0% to under 10%) or major (10% or more); p-values were treated separately, as a "decision error" when the reported and obtained p fell on opposite sides of the 0.05 threshold; and an "insufficient information error" was recorded when the original specification was too ambiguous or absent to attempt a reanalysis at all [[hardwicke-2018]]. Each article-level case was then classed as reproducible, reproducible with author assistance only, not fully reproducible, or not fully reproducible despite author assistance [[hardwicke-2018]].

## Findings

Errors were initially found in 24 of 35 assessments (69%, CI [51, 83]), all of which prompted a request for author assistance [[hardwicke-2018]]. After that assistance: 11 articles (31%, CI [17, 51]) were reproducible without any author help, 11 (31%, CI [17, 51]) were reproducible with author help, and 13 (37%, CI [23, 57]) had at least one outcome that remained not fully reproducible despite it [[hardwicke-2018]]. Of 1,324 individual values checked, 64 (5%, CI [4, 6]) remained major numerical errors after assistance, 2 remained insufficient information errors, no decision errors occurred at any point, and 146 minor numerical errors were found but set aside as too small to warrant further pursuit [[hardwicke-2018]].

For almost all of the ten cases the source counts as not fully reproducible, the source's own (explicitly subjective) qualitative judgement was that the reproducibility issues did not appear to seriously undermine the article's original conclusions [[hardwicke-2018]]. Major effect-size errors occurred in five cases: four were judged low in magnitude, and in the fifth the reported and reanalysed effect sizes diverged more substantially (d = 0.65 reported against d = 0.23 reanalysed), though every other target outcome in that article was reproduced and the reanalysed effect size still matched the direction of the hypothesis under test [[hardwicke-2018]]. Three further cases were left "unclear" because the team could not complete part of the assessment, so no judgement about their original conclusions could be reached [[hardwicke-2018]].

Of the 64 unresolved major errors, by outcome type: 17 (27%) standard deviations or standard errors, 17 (27%) p-values, 10 (16%) test statistics, 8 (12%) effect sizes, 4 (6%) means or medians, 4 (6%) degrees of freedom, 1 (2%) a count or proportion, 1 (2%) a confidence interval, and 2 (3%) other values [[hardwicke-2018]].

## What caused the errors

Across the 35 assessments, 57 discrete reproducibility issues were classified by likely cause: 30 (53%) incomplete or ambiguous specification of the original analysis; 10 (18%) missing or incorrect information in the shared data file; 5 (9%) typographical slips in transferring analysis output to the manuscript; 3 (5%) errors in the original authors' own analyses; and 9 (16%) issues whose cause could not be identified even after contacting the authors [[hardwicke-2018]]. Of these 57 issues, 33 (58%) were resolved through author assistance: 24 (73%) by clarifying an ambiguous specification, 8 (24%) by replacing an incomplete or corrupted data file, and 1 (3%) when the authors' own code revealed an error in their original analysis [[hardwicke-2018]].

The source estimates 2 to 4 person-hours for a "reproducible" assessment and 5 to 25 person-hours for the two categories requiring author assistance, with cases needing author contact typically taking a few weeks to several months to resolve given back-and-forth correspondence [[hardwicke-2018]]. In three cases, the original authors indicated they would publish a formal correction; the source reports one such correction had appeared by the time of writing [[hardwicke-2018]].

## What the source concedes about how optimistic this estimate is

The source states explicitly that its own sample is likely to overestimate reproducibility success if generalised, for four stated reasons: only a small subset of each article's outcomes was checked, so other reported values might not have reproduced as well; only outcomes tied to a substantive, emphasised finding were targeted, which are plausibly the values original authors checked most carefully themselves; only the most straightforward analyses were attempted, when more complex analyses are expected to be harder to reproduce; and the 35 articles were drawn from a pool already filtered for a stringent data-sharing policy and for having in-principle reusable data, so their authors were plausibly more likely than average to run a reproducible analysis pipeline in the first place [[hardwicke-2018]]. It also states it cannot always establish whether a non-reproducible value was originally miscalculated or was calculated correctly but can no longer be retraced; in some cases author correspondence identified a likely cause (for instance, a confirmed typographical error), but in many it could not [[hardwicke-2018]].

## Related pages

- [[open-data-policy-effect-on-availability]] for whether the underlying data this page's reproducibility checks relied on were available and reusable in the first place.
