---
type: concept
title: "Can preregistration close off researcher degrees of freedom?"
description: What the sources say a preregistration has to contain if it is to remove the analytic flexibility that produces p-hacking, how the quality of a preregistration can be assessed, and what the sources propose for studies that are not preregistered.
created: 2026-09-04
updated: 2026-09-28
sources: [wicherts-2016, head-2015, bishop-2016, bruns-2016, fraser-2018, agnoli-2017]
status: draft
generated:
  by: claude-code/claude-sonnet-5
  at: 2026-09-04
---

# Can preregistration close off researcher degrees of freedom?

All six sources that discuss remedies name preregistration or pre-specification as one of them [[wicherts-2016]] [[head-2015]] [[bishop-2016]] [[bruns-2016]] [[fraser-2018]] [[agnoli-2017]]. Only one of them examines what a preregistration would have to contain in order to work [[wicherts-2016]]. This page collects what the sources say about that. For the practices a preregistration is meant to shut down, see [[what-p-hacking-is]].

## What a preregistration has to contain

Preregistration means stipulating in advance the research hypothesis, the data collection plan, the specific analyses, and what will be reported in the paper [[wicherts-2016]]. Wicherts and colleagues set three conditions on that stipulation. It must be specific, meaning a detailed description of every step from hypothesis to final report. It must be precise, meaning that each step allows only one interpretation or implementation. And it must be exhaustive, meaning that it excludes the possibility that other steps are also taken [[wicherts-2016]]. For the confirmatory part of a study, they say, the word "only" is key, as in "we will test only Hypothesis A in the following unique manner" [[wicherts-2016]].

The reason for the third condition is that a preregistration which merely names what will be done leaves everything it did not name available. Naming the scale to be used as the primary outcome does not stop a researcher trying many ways of scoring its items; stipulating a test of one hypothesis does not preclude also testing another [[wicherts-2016]]. The authors report from their own experience that writing a preregistration to this standard is no easy task and that manoeuvrability remains where the standard is not met [[wicherts-2016]]. They recommend that the analysis syntax preferably be written in advance and run once on the collected data [[wicherts-2016]].

The same paper works the requirement through phase by phase: which manipulated and non-manipulated independent variables will be used and how each is to be operationalised, and that no others will enter the confirmatory analyses; which dependent variables will be used and how their scores will be computed; which participants will be excluded and that those rules are the only exclusion rules; the sample size with its power analysis, together with the population, the sampling procedure, the end point of collection and what happens if the target is not met; the randomisation technique; the blinding procedure; and the inference criteria [[wicherts-2016]]. The list of choices this is meant to cover is on [[what-p-hacking-is]].

## Assessing a preregistration

Because a preregistration can be incomplete in all the ways above, its quality can be scored. Wicherts and colleagues describe a protocol, based on their checklist, that scores specificity, precision and completeness at the level of each researcher degree of freedom: 0 if the degree of freedom is not limited, 1 or 2 if the description is partly or fully specific and precise, and 3 if it is also exhaustive [[wicherts-2016]]. They state that authors can score their own preregistration in order to improve it and that reviewers of registered reports and registered studies can use the protocol as well [[wicherts-2016]]. They report having a study under way applying the protocol to a random sample of preregistrations on the Open Science Framework, but the paper reports no results from it, so the wiki has no evidence on how actual preregistrations score [[wicherts-2016]].

A related mechanism is the registered report, in which the registration itself is peer reviewed and revised before data collection and the report is accepted for publication regardless of the direction, strength or statistical significance of the results [[wicherts-2016]]. Wicherts and colleagues describe the format as in use at a number of journals at the time of writing, citing Chambers (2013) for the count, which is on [[wicherts-2016]]. They also list failing to mention, misrepresenting or misidentifying a preregistration as a researcher degree of freedom in its own right, and suggest that reviewers compare the preregistration with the submitted article [[wicherts-2016]].

## What the other sources recommend

Head et al. recommend that researchers label their studies as prespecified or exploratory, and that journals encourage or provide platforms for prespecification [[head-2015]]. Their other recommendations are for reporting rather than for planning: full reporting of analyses including effect sizes, p-values to three decimal places and sample sizes, and open access to raw data, which they say does not prevent p-hacking but makes researchers accountable for marginal results [[head-2015]].

Bishop and Thompson name pre-registration of protocols and analyses as a recommended solution to publication bias which scientists have been slow to adopt, and say the wider problem also requires changes in methods training and in the incentive structure of science [[bishop-2016]].

Bruns and Ioannidis make the same recommendation for observational research that tests hypotheses, asking for careful pre-specification of the analysis plan [[bruns-2016]]. They cite a survey of registered observational protocols as finding that pre-specification of the statistical analysis almost never happens [[bruns-2016]]. For studies that are hypothesis-generating rather than hypothesis-testing they ask instead that the exploratory character be reported transparently, that results under different models be acknowledged, and that the model chosen for emphasis be interpreted with great caution [[bruns-2016]].

Fraser and colleagues, reporting a self-report survey rather than proposing a method of their own, recommend preregistration as "a promising tool for individual researchers," stating that a thorough preregistration specifies hypotheses, sample-size decisions, data-exclusion criteria and planned analyses in advance, and that this protects against HARKing, cherry-picking and p-hacking, without setting out what makes a given preregistration thorough [[fraser-2018]]. They also recommend registered-report formats to minimise HARKing, and note mandatory data-archiving policies already adopted at some journals as an existing institutional lever, while conceding that compliance with such policies falls short of complete [[fraser-2018]].

Agnoli and colleagues, also reporting a self-report survey, name "the prior specification (pre-registration) of research hypotheses and detailed analyses plans" as one of several changes, alongside higher statistical power and reviewers being more open to imperfect results, that they say will help lower QRP use, without setting out what such a preregistration must contain [[agnoli-2017]].

The six sources agree on the direction. They differ in scope: Head et al. and Bishop and Thompson state the recommendation without saying what a preregistration must contain [[head-2015]] [[bishop-2016]], Fraser and colleagues and Agnoli and colleagues likewise recommend it without a standard of thoroughness beyond the general descriptions above [[fraser-2018]] [[agnoli-2017]], Bruns and Ioannidis specify the analysis plan for observational designs [[bruns-2016]], and Wicherts and colleagues set out the standard in detail for experiments analysed by significance testing [[wicherts-2016]].

## What to do when a study is not preregistered

Wicherts and colleagues offer two fallbacks, while stating that preventing bias is better than treating it after the event [[wicherts-2016]]. The first is to report all potentially relevant analyses, either as traditional sensitivity analyses or as a multiverse analysis. The second is to make the data available for independent reanalysis after publication, which they say is not always possible because sharing rates are low [[wicherts-2016]]. They also offer the checklist itself as a way of gauging the potential for bias in an unregistered study [[wicherts-2016]].

Bruns and Ioannidis propose a statistical fallback for large observational datasets: calibrating p-values against an empirical null distribution built from comparisons believed to have no causal link, rather than judging them against theoretical null distributions and the 0.05 threshold, while conceding that this is not always feasible because a sufficient set of uncontested true positives and true negatives may not exist [[bruns-2016]].

Head et al. propose checks that a meta-analyst can run on a set of already-published studies; those are on [[p-hacking-and-meta-analysis]] [[head-2015]].

## A difference in framing

The sources do not dispute each other here, but they describe the same choices differently. Head et al. treat the practices as p-hacking driven by the incentive to publish significant results, and judge that eliminating it is unlikely while careers are assessed by publication output [[head-2015]]. Wicherts and colleagues report sympathy with Gelman and Loken's argument that the term questionable research practices is not always apt, because the majority of the choices they list are arbitrary ones that researchers simply have to make and could, but will not necessarily, use opportunistically [[wicherts-2016]]. What matters on their account is not that all researchers exploit the choices but that the data could have been collected and analysed differently, and that the reported analyses could have been chosen differently had the results come out differently [[wicherts-2016]].

The practical consequence is a difference in what the remedy is for. On the incentive framing the target is researcher behaviour [[head-2015]] [[bishop-2016]]; on the arbitrary-choice framing the target is the record, so that the flexibility available to a study is visible whether or not anyone exploited it [[wicherts-2016]]. No source addresses the other's framing directly, so the wiki records this as a difference of emphasis rather than as a disagreement.

## Limits acknowledged by the sources

Wicherts and colleagues state that their list of researcher degrees of freedom is not exhaustive, that other routes to bias are outside it (confounded designs, biased samples, invalid measurements, erroneous analyses, data dependencies that inflate significance levels), and that the list was built for null hypothesis significance testing, so some entries do not apply to other statistical frameworks and the degrees of freedom specific to those frameworks, such as the choice of prior, are missing [[wicherts-2016]]. The list was assembled qualitatively, by the authors' own discussion and revision [[wicherts-2016]]. A preregistration built on it is therefore only as complete as the list.

Bishop and Thompson note that pre-registration has been slow to be taken up [[bishop-2016]], and Bruns and Ioannidis report that registered observational protocols almost never pre-specify their statistical analysis [[bruns-2016]]. None of the sources reports evidence on whether preregistration, once adopted, reduces p-hacking.

## Related pages

- [[what-p-hacking-is]] for the choices a preregistration would have to close off.
- [[p-curve-as-evidence]] for attempts to detect the exploitation of those choices after publication.
- [[p-hacking-and-meta-analysis]] for what meta-analysts can do with studies that were never preregistered.
