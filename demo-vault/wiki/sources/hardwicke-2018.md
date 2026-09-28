---
type: source
title: "Hardwicke et al. (2018), Data availability, reusability, and analytic reproducibility"
description: An observational evaluation of a mandatory open data policy at the journal Cognition, assessing its impact on data availability and in-principle reusability (study 1), and the analytic reproducibility of a subset of reported outcomes for 35 articles with reusable data (study 2).
created: 2026-09-04
updated: 2026-09-28
sources: [hardwicke-2018]
status: draft
generated:
  by: claude-code/claude-sonnet-5
  at: 2026-09-04
doi: 10.1098/rsos.180448
licence: CC BY 4.0
---

# Hardwicke et al. (2018), Data availability, reusability, and analytic reproducibility

Hardwicke, Mathur, MacDonald, Nilsonne, Banks, Kidwell, Hofelich Mohr, Clayton, Yoon, Henry Tessler, Lenne, Altman, Long and Frank. *Royal Society Open Science* 5(8), 180448, received 19 March 2018, accepted 25 June 2018. The authors are based mainly at Stanford University's Meta-Research Innovation Center (METRICS) and Department of Psychology, with co-authors at Harvard, the University of Utah, the University of Minnesota, the University of North Carolina at Charlotte, and Stockholm University and the Karolinska Institutet. Both studies were preregistered (https://osf.io/q4qy3/), and the paper states that all deviations from the protocol or additional exploratory analyses are explicitly acknowledged.

## What the paper set out to do

The paper evaluates the mandatory open data policy introduced at the journal *Cognition* on 1 March 2015, which required authors to make research data publicly available, in a form enabling reuse and analytic reproducibility, prior to publication. Study 1 assesses the policy's effect on the frequency of data available statements (DAS) and on whether purportedly available data were in-principle reusable (accessible, complete and understandable). Study 2 assesses, for a subset of articles with in-principle reusable data, whether the reported outcomes could be reproduced by repeating the original analyses on the shared data ("analytic reproducibility").

## Study 1: data availability and in-principle reusability

### Design and sample

A retrospective, quasi-experimental pre-/post-design (not a randomised manipulation): 591 empirical articles published in *Cognition* from March 2014 to March 2017, sampled by an article's submission date, which determined whether the policy applied. 417 articles fell in the pre-policy period and 174 in the post-policy period. Five trained coders, each reaching over 90% agreement with a gold standard on a training set, extracted the measured variables into a standardised Google Form; coders were not blind to the study hypotheses, but the paper judges the potential for coder bias low because the extraction protocol left little room for subjective interpretation. Articles were randomly assigned to coders (in batches of up to 20) to spread any coder drift evenly across the pre- and post-policy periods.

### Data availability statements

No article in the sample carried a "data not available" statement, so the analysis focuses on the proportion with a data available statement (DAS). DAS inclusion rose from 104/417 = 25% (95% CI [21, 29]) pre-policy to 136/174 = 78% (CI [71, 84]) post-policy; a chi-squared test of independence was significant, chi-squared(1, n = 591) = 144.18, p < 0.001.

An interrupted time-series analysis (logistic regression of DAS inclusion on time, a pre/post indicator and their interaction, described in the paper's Methods) was used to estimate the policy's causal effect net of any pre-existing secular trend, on the assumption that articles submitted immediately before and after the policy were otherwise similar. Results, converted to the risk-ratio scale: a pre-policy secular trend of 1.04-fold per 50 days (CI [1.02, 1.06], p = 0.002); a level change at policy introduction of 1.53-fold higher DAS probability (CI [1.10, 1.90], p = 0.017); and a post-policy secular trend 1.14-fold steeper than the pre-policy trend (CI [1.04, 1.26], p = 0.010). In a further, alternative decomposition, the paper estimates that of the 50-day secular trend increase in the post-period, 5% (CI [0, 10], p = 0.022) reflects the pre-existing baseline trend alone, 65% (CI [40, 90], p < 0.001) reflects the policy's own effect, and 30% (CI [7, 53], p < 0.001) reflects acceleration of the trend caused by the policy; standard errors for this decomposition were approximated by the delta method.

Where data were said to be available: 208 articles (87%) via *Cognition*'s own supplementary materials (the default option), 27 (11%) via a third-party repository, 2 (1%) via a personal webpage, and 3 (1%) by other means (in another article, or a table in the current article). No article's DAS pointed to "available upon request."

### In-principle reusability

Among articles with a DAS, coders assessed whether the data were accessible (could be downloaded and opened), complete (contained raw, individual-level data for all measured variables) and understandable (clearly labelled or documented); the three combined are "in-principle reusable." Data were successfully downloaded and opened in all but four cases. In-principle reusability rose from 23/104 = 22% of pre-policy DAS articles (6% of all 417 pre-policy articles) to 85/136 = 62% of post-policy DAS articles (49% of all 174 post-policy articles). This comparison was exploratory (not preregistered); a chi-squared test of independence was significant, chi-squared(1, n = 591) = 154.38, p < 0.001, and an interrupted time-series analysis (reported in the paper's electronic supplementary material, not part of the extracted source) again indicated a baseline secular trend plus a significant post-policy level change.

Eighteen articles included analysis scripts; only eight of those were shared alongside data judged reusable.

### Study 1 discussion and limitations, in the paper's own terms

The paper reads the results as showing the policy successfully increased data availability and in-principle reusability, while falling short of the ideal: 22% of post-policy articles still lacked a DAS, and 38% of reportedly available post-policy datasets did not appear reusable in principle. It notes the situation was improving over the assessment window, with DAS approaching 100% and in-principle reusability approaching 75% towards the end.

On causal interpretation, the paper names several threats to validity inherent in the non-randomised design: a "maturation" threat (growing awareness of open-science issues among authors generally, independent of the policy), possible anticipatory effects because the editorial announcing the policy was posted online about four months before it took effect, and the possibility of other concurrent events (it names the Open Science Collaboration's 2015 replicability paper as a candidate, while stating it is not aware of any event that specifically coincides with the moment DAS rates changed). It also raises self-selection ("population shift"): that researchers already inclined toward open science may have been drawn to the journal by the policy, or others deterred, which would make the observed increase overestimate the policy's efficacy for less-inclined researchers. Two exploratory (not preregistered) checks partly address this: a stable "author retention index" before and after the policy (no evidence of a persistent-author group being deterred, though these authors are also the least likely to leave), and an increase rather than a decrease in overall journal productivity after the policy (inconsistent with mass author deterrence, though the paper notes a larger pool of authors attracted could mask some who were deterred). Neither check rules out a population shift.

The paper also flags that its reusability assessments involved only "relatively brief visual inspection" and are therefore likely to underestimate reusability in practice, and that coders were not blind to the hypotheses (judged low-risk given the largely non-subjective protocol).

## Study 2: analytic reproducibility

### Sample and design

A non-comparative case-study design. From the 108 articles with in-principle reusable data identified in study 1, a "triage pool" was populated incrementally; 47 were assessed for eligibility by a single author (T.E.H.), and 12 were rejected because no outcome met the criteria below. 35 articles were deemed eligible: 5 from the pre-policy period and 30 from the post-policy period. Sample size was not preregistered; the team ran checks until personnel resources were exhausted.

Within each article, target outcomes were a coherent set of descriptive and inferential statistics supporting a "substantive" finding (one emphasised in the abstract, a figure or a table) obtained through a "relatively straightforward" analysis (one that would appear in an introductory psychology statistics text, e.g. correlations, t-tests, ANOVAs); the first qualifying coherent set encountered in the results section was chosen, and the paper concedes this selection involved subjectivity. Each reproduction followed a co-piloting model: a pilot conducted the initial check independently, then at least one co-pilot verified the pilot's analyses and helped resolve outstanding issues, and the two produced a joint literate-programming (R Markdown) report, available on OSF (https://osf.io/p7vkj/). When analysis specifications were ambiguous or absent, coders were told to record an "insufficient information error" rather than guess extensively, though some limited guesswork (e.g. trying a test with and without a continuity correction) was part of the process. When problems arose, the team contacted the original authors for assistance.

### Error classification

Any numerical discrepancy between a reported and a reanalysed value was expressed as a percentage error (PE = |obtained − reported| / reported × 100): a minor numerical error is 0% < PE < 10%, a major numerical error is PE >= 10%. P-values were treated specially: a "decision error" is a reported p that falls on the opposite side of the 0.05 boundary from the obtained p. Each article-level case was then classed as reproducible (no discrepancies, or only minor ones), reproducible with author assistance only, not fully reproducible, or not fully reproducible despite author assistance, and the paper separately notes whether author assistance was needed. It also attempted, where possible, to identify a causal locus for each discrete reproducibility issue, using a post hoc (not preregistered) scheme: typographical, inadequate analysis specification, original analysis issue, data file issue, or unidentified.

### Results

Errors were initially encountered in 24 of 35 assessments (69%, CI [51, 83]); the team requested and received author assistance in every one of these cases. After assistance, target outcomes in 11 articles (31%, CI [17, 51]) were reproducible without any author assistance, 11 articles (31%, CI [17, 51]) were reproducible with author assistance, and 13 articles (37%, CI [23, 57]) contained at least one outcome that remained not fully reproducible despite author assistance.

Of 1,324 individual values the team attempted to reproduce, 64 major numerical errors (5%, CI [4, 6]) and two insufficient information errors remained after author assistance; there were no decision errors; 146 minor numerical errors were also found but not pursued further given their small magnitude.

In almost all of the cases where target outcomes were not fully reproducible (given as n = 10), the paper judges (through case-by-case qualitative assessment, described as necessarily subjective and reported in full in the paper's electronic supplementary material E, not part of the extracted source) that the reproducibility issues did not appear to seriously undermine the article's original conclusions. Major errors involving effect sizes occurred in five cases; in four (article codes COGGV, DvcDF, jjmld, bPJii) the magnitude of the discrepancy was described as low, and in the fifth (OvGDB) a larger discrepancy was found (reported d = 0.65 versus reanalysis d = 0.23), but all other target outcomes in that article, including other effect sizes and inferential statistics, were reproduced, and the reanalysed effect size was still described as consistent with the hypothesis under scrutiny. Three further cases were left "unclear" because the team lacked sufficient information to complete part of the assessment, so no informed judgement about the original conclusions could be made for those.

By outcome type, the 64 major errors broke down as: 17 (27%) standard deviations or standard errors, 17 (27%) p-values, 10 (16%) test statistics (e.g. t, F), 8 (12%) effect sizes (e.g. Cohen's d, Pearson's r), 4 (6%) means or medians, 4 (6%) degrees of freedom, 1 (2%) a count or proportion, 1 (2%) a confidence interval, and 2 (3%) other miscellaneous values.

Across the 35 assessments, 57 discrete reproducibility issues were identified and classified: 30 (53%) incomplete or ambiguous specification of the original analysis (examples given: data exclusions that could not be mapped to the data file, unreported ANOVA sphericity corrections, unidentified inferential tests, unreported non-standard standard-error methods, unreported pre-analysis aggregation, incomplete linear mixed model specification); 10 (18%) missing or incorrect information in the data file (rounded rather than raw data, missing variables, data entry errors, manual-editing errors); 5 (9%) typographical issues; 3 (5%) errors in the original authors' own analyses (sometimes surfaced only when the original authors themselves tried to reproduce their findings, e.g. outdated analysis versions or a formula error in a confidence-interval calculation); and 9 (16%) issues whose locus could not be identified even after correspondence with the authors. Of the 57 issues, 33 (58%) were resolved through author assistance: 24 (73%) by clarifying specifications, 8 (24%) by replacing incomplete or corrupted data files, and 1 (3%) when authors' code revealed an error in their original analysis.

Time was not recorded precisely, but the paper estimates 2 to 4 person-hours for assessments in the "reproducible" category and 5 to 25 person-hours for the "reproducible with author assistance" and "not fully reproducible despite author assistance" categories, with completion (where author contact was needed) typically spanning a few weeks to several months. In three cases the original authors indicated they would publish a formal correction; the paper states one such correction had been published at the time of writing.

Figure 3 in the paper (described here in words, per the wiki's convention of not embedding source images) plots all 1,324 checked values by article and value type, with non-reproducible major-error values marked and reproducible values shown as circles sized by count, and articles colour-coded by their overall outcome (not fully reproducible despite assistance, reproducible with assistance, reproducible without assistance); articles whose analysis could not be completed are separately marked. Figure 4 plots, for the two categories of article with unresolved or once-unresolved issues, the locus of non-reproducibility by discrete issue, distinguishing issues resolved through author assistance from those left unresolved.

### Study 2 discussion and limitations, in the paper's own terms

The paper describes an initial (pre-assistance) reproducibility success rate of 31%, which it calls comparable to prior assessments in political science and economics and worse than a cited assessment of clinical trials, and states this "lack of analytic reproducibility compromises the credibility of the reported outcomes." It also stresses that authors were, in almost all cases, prompt, detailed and helpful when contacted, but argues that reliance on such back-and-forth exchanges is not a sustainable model for routine data reuse, especially as author responsiveness is expected to decline as papers age.

The paper states plainly that study 2's sample is likely to yield an optimistic estimate of analytic reproducibility, for four reasons it gives explicitly: only a small subset of each article's outcomes was checked; only outcomes tied to a substantive, emphasised finding were targeted (plausibly the most carefully checked by the original authors); only the most straightforward analyses (ANOVAs, t-tests, etc.) were attempted, when more complex analyses are expected to be harder to reproduce; and the 35 articles were drawn from a pool that had already been filtered for a stringent open-data policy and for having in-principle reusable data, so their authors were plausibly more likely than average to run reproducible pipelines. It concludes that these findings "would mostly overestimate reproducibility success" if generalised elsewhere.

The paper is explicit that it cannot always tell whether a non-reproducible value was originally erroneous or was originally correct but has become impossible to retrace; in some cases correspondence with authors identified the likely cause (e.g. a confirmed typo), but in many it could not.

## General discussion

The paper frames the *Cognition* policy as "pioneering" among journal data-sharing policies, states that mandatory open data policies "can increase the frequency and quality of data sharing," but that suboptimal data curation, unclear analysis specification, and reporting errors "can impede analytic reproducibility, undermining the utility of data sharing and the credibility of scientific findings." It draws an analogy between conducting a reproducibility check without an analysis script and assembling flat-pack furniture without an instruction booklet. It closes by framing the choice between "carrot" (voluntary, badge-based) and "stick" (mandatory) approaches to transparency as both useful, but argues the more constructive long-run focus is on redesigning research systems (analysis pipelines, publishing practices) on the assumption that errors are inevitable, drawing an analogy to defensive-programming practices in computer science.

## Recommendations

For the journal's own policy: clearer labelling to distinguish data from research materials (many "supplementary data" links in fact pointed to materials, in .doc/.pdf formats, rather than data); more consistent licensing (only about half of shared data the team encountered carried a licence, typically CC-BY); and preferring a dedicated third-party repository with persistent identifiers over reliance on a journal's own supplementary-materials system, citing evidence that such links go "broken" over time. Editorially: providing authors with clearer data-stewardship guidelines, giving editors/reviewers a structured compliance checklist, and/or assigning data-compliance checking to dedicated editorial staff, while acknowledging this requires weighing costs and benefits.

For analytic reproducibility specifically: requiring analysis scripts (code, or a detailed step-by-step account where code is unavailable) alongside data, since the paper found that when authors did share scripts on request it was "much more straightforward" to re-implement analyses; adopting literate-programming tools (e.g. R Markdown) that interleave code and prose; and, further, using shareable software containers so reported outcomes can be regenerated directly. The paper notes some journals in economics and political science already mandate shared analysis scripts, and one (the *American Journal of Political Science*) goes further and uses a third party to verify analytic reproducibility before publication, while noting it is not established whether shared scripts would themselves prove reusable in practice.

## Cited by

- [[open-data-policy-effect-on-availability]]
- [[analytic-reproducibility-from-shared-data]]
