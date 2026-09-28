---
type: source
title: "Wicherts et al. (2016), Degrees of freedom in planning, running, analyzing, and reporting psychological studies: A checklist to avoid p-hacking"
description: A review article listing 34 researcher degrees of freedom across the hypothesizing, design, data collection, analysis and reporting phases of a psychological study, offered as a teaching tool and as a checklist for assessing preregistrations and the potential for bias in unregistered studies.
created: 2026-09-04
updated: 2026-09-04
sources: [wicherts-2016]
status: draft
generated:
  by: claude-code/claude-opus-5
  at: 2026-09-04
doi: 10.3389/fpsyg.2016.01832
licence: CC BY 4.0
---

# Wicherts et al. (2016), Degrees of freedom in planning, running, analyzing, and reporting psychological studies: A checklist to avoid p-hacking

Wicherts, Veldkamp, Augusteijn, Bakker, van Aert and van Assen, Methodology and Statistics, Tilburg University. Frontiers in Psychology 7, 1832, received 30 July 2016, accepted 4 November 2016, published 25 November 2016. Submitted to the Quantitative Psychology and Measurement section. Supported by grants 406-13-050, 406-15-198 and 452-11-004 from the Netherlands Organization for Scientific Research. No competing interests declared. The article is a review, not an empirical study: it reports no data, no simulation and no numerical results beyond the size of its own list.

## What the paper set out to do

The paper presents a list of 34 researcher degrees of freedom that arise in formulating hypotheses and in designing, running, analysing and reporting psychological studies. Three uses are stated for the list: research methods education, a checklist for assessing the quality of preregistrations, and a way of gauging the potential for bias due to arbitrary choices in unregistered studies. The authors describe the list as a charting of what Gelman and Loken (2014) called the garden of forking paths.

The list was created qualitatively. The authors describe themselves as a group of methodologists studying researcher degrees of freedom, publication bias, meta-analysis, misreporting of results and reporting biases, who assembled a large list, discussed it, and reduced it to a manageable one over several rounds of revision. Most of the entries have been described in earlier publications, which the paper cites; the entries are said to be inspired by actual research the authors encountered as researchers, replicators, re-analysers and readers, but no researchers, projects or papers are identified, on the stated ground that the issues are general.

The list was built with null hypothesis significance testing in mind, because that is the framework most used in psychology. The paper says most of the entries are relevant to other frameworks as well, but that some would have to be replaced or omitted (it gives power analysis, D6, as defined within the significance-testing framework) and others added (it gives the choice of prior in Bayesian statistics), and it therefore recommends using the list primarily for research that uses significance testing.

The paper focuses on the experiment as the most basic and most widely used design in psychology, and presents it as an archetype for discussing choices in other designs, including quasi-experimental and correlational studies.

## How the paper defines researcher degrees of freedom

Researcher degrees of freedom, a term the paper attributes to Simmons et al. (2011), are the choices involved in a study that are often arbitrary from a substantive or methodological point of view but that can affect the outcome of significance tests and hence the conclusions drawn. The paper uses the singular "researcher DF" for one such choice and the plural "researcher DFs" for several.

Two reasons are given for the recent interest in them. First, opportunistic use of them greatly increases the chance of a false positive, or Type I error; the paper cites Ioannidis (2005), Simmons et al. (2011) and DeCoster et al. (2015). Second, strategic use of them may inflate effect sizes; the paper cites Ioannidis (2008), Bakker et al. (2012), Simonsohn et al. (2014) and van Aert et al. (2016). On the paper's account this is why researcher degrees of freedom are central to the creation of published findings that are hard to reproduce in a reanalysis of the same data and hard to replicate in independent samples.

The paper does not define p-hacking separately from this. Its abstract describes the problem as the opportunistic use of researcher degrees of freedom aimed at obtaining statistically significant results, and its title offers the checklist as a way to avoid p-hacking.

## The checklist

The list holds 34 entries in five phases, each carrying a code: 2 in hypothesizing (T1 to T2), 7 in design (D1 to D7), 4 in data collection (C1 to C4), 15 in analysis (A1 to A15) and 6 in reporting (R1 to R6). Table 1 also records which entries are paired with which: T1 with R6, D1 with A8, D2 with A10, D3 with A5, D4 with A7, D5 with A12, and D7 with C4. The pairings run between a choice created in the design and the same choice exploited in the analysis, or between a choice made at the start of a study and its counterpart in the report.

### Hypothesizing

T1 is conducting explorative research without any hypothesis. The paper says exploratory studies that lack a priori theorising are virtually guaranteed to yield support for something interesting, citing Wagenmakers et al. (2011), and that since results in psychology are usually presented within the hypothetico-deductive model it is tempting to present exploratory findings as though they had been hypothesised in advance, which is HARKing (Kerr, 1998) and reappears as R6. The statistical evidence for a found pattern is described as often much weaker than it appears, because the evidence should be read in the context of the size and breadth of the exploration and corrected for multiple testing, which is usually not done. The paper adds that a preregistered study may still include exploratory analyses without difficulty, provided they are clearly distinguished from the confirmatory ones.

T2 is studying a vague hypothesis that fails to specify the direction of the effect. A hypothesis of the form "X is related to Y" allows the data to be analysed one way to obtain a positive effect and another way to obtain a negative one, which the paper calls a special case of HARKing. Specifying the direction also bears on whether a one-tailed test may be used: the paper states that one-tailed tests can only be used to reject the null hypothesis when the a priori hypothesis was directional and the result came out in the predicted direction.

### Design

The design phase entries turn on redundancy built into a study, which creates room for manoeuvre later.

D1, creating multiple manipulated independent variables and conditions, covers crossed experimental factors that can be selected or discarded afterwards, by pooling over the levels of a factor or by selecting particular levels. The paper's worked illustration is a factor with three conditions (0, 1 and 2), which it says already yields seven different operationalisations for the analysis: the three levels together, any two of the three, or conditions 0 and 1 combined against condition 2.

D2 is measuring additional variables that can later be selected as covariates, independent variables, mediators or moderators. The example given is measured age, which can serve as a predictor of age differences, as a moderator of another independent variable, or as a control variable, and can be cut into two or three groups on many different thresholds or used continuously.

D3 is measuring the same dependent variable in several alternative ways, for instance measuring anxiety with several self-report scales or with physiological measures. D4 is measuring additional constructs that could potentially act as primary outcomes; the paper notes that in the medical trial literature this is called outcome switching and the resulting bias outcome reporting bias, citing Chan et al. (2004), Kirkham et al. (2010) and Weston et al. (2016). D4 is said to allow HARKing, whereas D3 concerns the same target construct.

D5 is measuring additional variables that enable later exclusion of participants, such as awareness checks, alertness checks or manipulation checks. The paper argues that an ideal preregistration must state which participants will be excluded and also state that those rules are the only ones that will be used, because naming one exclusion rule does not preclude excluding on other ad hoc grounds.

D6 is failing to conduct a well-founded power analysis. The paper states that most studies using significance testing do not report a formal power analysis, citing Sedlmeier and Gigerenzer (1989), Cohen (1990) and Bakker et al. (2012), and that researchers' intuitions about power are typically overly optimistic, citing Bakker et al. (2016). Its argument is that underpowered studies are themselves more susceptible to bias because sampling variability is larger, so that analytic choices have proportionately larger effects and using researcher degrees of freedom to obtain significance is more effective with smaller samples.

D7 is failing to specify the sampling plan and allowing for running multiple small studies. A rigorous preregistration is said to require the targeted sample size, when data collection starts and ends, how participants are sampled, the population sampled from, the end point of collection, and what happens if the target is not met. The paper adds that running several small studies and presenting only the best is an effective though problematic route to a significant result, citing Bakker et al. (2012), and that small underpowered studies can also be pooled by an ad hoc meta-analysis to obtain significance, citing Ueno et al. (2016).

### Data collection

C1 is failing to randomly assign participants to conditions. The paper notes that randomisation techniques are often not specified in articles, and gives as examples an experimenter running treatment participants only in the evening, or assignment based on observable characteristics that bear on the outcome.

C2 is insufficient blinding of participants and of experimenters. The paper describes both types of blinding and the ways they can fail, including the use of non-naive participants and the inadvertent conveying of expectations.

C3 is correcting, coding or discarding data during data collection in a non-blinded manner. The example is an experimenter who witnesses a slowly working participant in a condition expected to yield quick responses and discards that participant for not participating seriously, with no protocol dictating the decision. The paper notes that making such corrections deliberately might go beyond questionable practice and amount to falsification, but that doing it unawares in a poorly structured setting can still cause considerable bias.

C4 is determining the data collection stopping rule on the basis of desired results or intermediate significance testing, that is, continuing after a non-significant result or stopping early after a significant one. The paper cites John et al. (2012) for the practice and Wagenmakers (2007) for the point that sequential testing without formal correction raises Type I error rates. C4 is paired with D7.

### Analysis

The paper introduces this phase by observing that blinding is treated as crucial during data collection while the analysis is typically done by someone who knows the hypotheses and benefits directly from corroborating them.

A1 to A4 concern data cleaning and processing: choosing between options for incomplete or missing data on ad hoc grounds (listwise deletion, pairwise deletion, multiple imputation, full information methods and others, citing Schafer and Graham, 2002); specifying pre-processing in an ad hoc manner, which the paper says is especially open-ended for neuroimaging data where regions of interest, head motion, slice timing, spatial smoothing and normalisation create a large number of analytic paths, citing Poldrack et al. (2016); deciding how to deal with violations of statistical assumptions in an ad hoc manner, by non-parametric analysis, transformation, or simply ignoring the violation; and deciding how to deal with outliers in an ad hoc manner, since outliers can be defined and detected in various ways and kept or deleted on many alternative criteria.

A5 to A7 concern the dependent variable: selecting it out of several alternative measures of the same construct (paired with D3); trying out different ways to score the chosen primary dependent variable, since items can be dichotomised, discarded for low item-rest correlations, summed unweighted, weighted by an item response model, or replaced by factor scores from a principal components analysis, and response time data involve further choices about slow responses; and selecting another construct as the primary outcome (paired with D4). The paper's point about A6 is that naming the measure in a preregistration, its example being the Rosenberg Self-Esteem Scale, is not specific enough, because the scores can be computed in different ad hoc ways.

A8 to A11 concern independent variables: selecting independent variables out of a set of manipulated ones (paired with D1); operationalising manipulated independent variables in different ways, by discarding or combining levels of factors (paired with D1); choosing to include different measured variables as covariates, independent variables, mediators or moderators (paired with D2), with the example of adding big five personality measures to a one-way design so that every trait can be tried as a moderator, a covariate or a predictor; and operationalising non-manipulated independent variables in different ways, for instance using extraversion as a linear predictor, as a factor score, or as a comparison of arbitrarily chosen high and low scorers. The paper observes that combining many predictors, interactions and control variables with alternative operationalisations leads to a very large number of regressions, citing Sala-i-Martin (1997), and creates a massive multiple testing problem.

A12 is using alternative inclusion and exclusion criteria for selecting participants in the analyses (paired with D5). The paper notes that a specific, precise and exhaustive plan not to include particular participants would also spare resources, since participants who fail the criteria need not be run at all.

A13 to A15 concern the model and the inference: choosing between different statistical models (linear regression, ANOVA, MANOVA, robust or non-parametric analyses); choosing the estimation method, software package and computation of standard errors, since packages implement the same techniques in slightly different ways, a standard ANOVA already requires a choice between types of sum of squares (the paper says three are available in SPSS and that this choice is typically not described in articles), and advanced models can be estimated by maximum likelihood, ordinary least squares, weighted least squares, mean and variance adjusted weighted least squares, partial least squares or restricted maximum likelihood, with or without robust standard errors; and choosing inference criteria such as Bayes factors, the alpha level, the sidedness of the test and corrections for multiple testing, which a researcher can pick after seeing the outcomes, for instance switching to a one-sided test if that is the only route to significance.

### Reporting

R1 is failing to assure reproducibility, meaning verification of the steps from data collection to the final report, including pre-processing, the statistical model, the estimation technique, software package and computational details, data exclusions, missing data, violated assumptions and outliers. The preferred way to assure it, the paper says, is to share data and analytic code in or alongside the paper, citing Nosek et al. (2015).

R2 is failing to enable replication, meaning that the report or its supplements must include sufficient detail on procedures and all materials used. The paper mentions online repositories and platforms such as the Open Science Framework.

R3 is failing to mention, misrepresent or misidentify the study preregistration. The paper cites Chan et al. (2004) as finding that preregistrations in the medical literature are often not followed in the final report, and suggests that reviewers compare the preregistration with the submitted article.

R4 is failing to report so-called failed studies that were originally deemed relevant to the research question. The paper notes that such studies are often those with non-significant results, citing Cooper et al. (1997) for non-publication, and argues that a study seen in advance as valid and rigorous cannot be considered failed and should count as evidence, which is the idea underlying registered reports.

R5 is misreporting results and p-values, for instance presenting a non-significant result as significant; the paper cites Bakker and Wicherts (2011) and describes this and similar misreporting, such as incorrectly stating a lack of moderation by demographic variables, as quite common, citing John et al. (2012) and Nuijten et al. (2015).

R6 is presenting exploratory analyses as confirmatory, that is, HARKing, which the paper relates back to T1 and describes as apparently quite commonly practised by psychologists, citing John et al. (2012).

## What the paper says a preregistration must do

The paper's central requirement is that a preregistration be specific, precise and exhaustive. Specific means a detailed description of all steps from hypothesis to final report. Precise means that each described step allows only one interpretation or implementation. Exhaustive means that the preregistration excludes the possibility that other steps may also be taken. For confirmatory parts of a study the paper says the word "only" is key, as in "we will test only Hypothesis A in the following unique manner".

Preregistration requires stipulating in advance the research hypothesis, the data collection plan, the specific analyses, and what will be reported. The paper prefers the term "planned research" to the commonly used "confirmatory research" but adopts the common term. It recommends that the analysis syntax preferably be written in advance and run once on the collected data to yield the final results.

The authors report from their own experience with preregistration that this specification is no easy task and that manoeuvrability remains when preregistrations are not sufficiently specific, precise or exhaustive. Their illustration is that naming the scale to be used as the main outcome measure does not stop a researcher trying many ways of scoring its items, and that stipulating a test of Hypothesis A does not preclude also testing Hypothesis B.

The paper reports that an increasing number of journals support preregistration for confirmatory research, citing Eich (2014), and that over two dozen journals use the registered reports format, citing Chambers (2013), in which the registration is peer reviewed and revised before data collection and the report is accepted for publication regardless of the direction, strength or statistical significance of the results. It names Cortex, Comprehensive Results in Social Psychology and Perspectives on Psychological Science (for Registered Replication Reports) as examples.

The paper describes a study it was conducting at the time of writing on a random sample of actual preregistrations on the Open Science Framework, scored with a protocol based on the checklist. The protocol assesses specificity, precision and completeness at the level of each researcher degree of freedom: a score of 0 if the degree of freedom is not limited, 1 or 2 if the description is partly or fully specific and precise, and 3 if it is also exhaustive, meaning that it excludes other steps. Authors can score their own preregistration in order to improve it, and reviewers of registered reports and registered studies can use the protocol too. No results from that study are reported here.

## What the paper claims

- Researcher degrees of freedom are numerous, arise at every phase of a study, and have strong potential to create bias, which is particularly severe for experiments studying subtle effects with relatively small samples.
- The list of 34 is a good starting point for a checklist that can assess the degree to which preregistrations truly protect against the biasing effects of researcher degrees of freedom, and can also be used in methods education and to gauge the potential for bias in unregistered studies.
- Preventing bias is better than treating it after it has occurred, so the preferred way to counter bias from researcher degrees of freedom is to preregister the study in a way that no longer allows researchers to exploit them.
- Where a study is not preregistered, one way to assess the relevance of the choices made is to report all potentially relevant analyses, either as traditional sensitivity analyses or as a multiverse analysis, citing Steegen et al. (2016). Another is to make the data available for independent reanalysis after publication, though the paper says this is not always possible because sharing rates are low, citing Wicherts et al. (2011).
- The paper sympathises with Gelman and Loken's (2014) argument that the term questionable research practices is not always apt for researcher degrees of freedom, because the majority of them involve choices that are arbitrary and that researchers could, but will not necessarily, use opportunistically. What matters, on the paper's account, is not that all researchers exploit these choices but that the data could have been collected and analysed differently, and that the analyses finally reported could have been chosen differently had the results come out differently.
- For future work the paper suggests adapting the list for studies planning to use confidence intervals, precision of effect size estimation, or Bayesian analyses, and developing and assessing protocols for open materials, open data and open workflows, which it says are gaining traction but are often insufficiently detailed or documented to allow others to reproduce and replicate results.

## What the paper concedes

- The list of 34 is in no way exhaustive. The authors state this twice, once when describing how the list was made and once in the discussion.
- Other ways of creating bias are not on the list, including poorly designed experiments with confounding factors, biased samples, invalid measurements, erroneous analyses, inappropriate scales and data dependencies that inflate significance levels. The paper says it focused on the degrees of freedom that are relevant even for well-designed and rigorously conducted studies.
- Some entries on the list are clearly related to others; the authors kept them separate anyway so that each could be listed under the phase of the study in which it arises.
- The list was built for null hypothesis significance testing. Some entries do not apply to other statistical frameworks and the specific degrees of freedom belonging to those frameworks, such as the choice of prior, are not included.
- In discussing the data collection phase the paper assumes the design is internally valid and the measures construct valid, while noting that actual studies do not always meet those assumptions.
- The list is qualitative in origin, produced by the authors' own discussion and revision rather than by a systematic procedure.

## Cited by

- [[what-p-hacking-is]]
- [[preregistration-as-a-remedy]]
- [[p-hacking-and-meta-analysis]]
