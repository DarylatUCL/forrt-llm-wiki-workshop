---
type: source
title: "Agnoli et al. (2017), Questionable research practices among Italian research psychologists"
description: A self-report survey of 277 Italian research psychologists (208 completing), directly replicating John et al.'s (2012) US survey of ten questionable research practices, comparing Italian and US self-admission rates, defensibility judgements, prevalence estimates and doubts about research integrity.
created: 2026-09-04
updated: 2026-09-28
sources: [agnoli-2017]
status: draft
generated:
  by: claude-code/claude-sonnet-5
  at: 2026-09-04
doi: 10.1371/journal.pone.0172792
licence: CC BY 4.0
---

# Agnoli et al. (2017), Questionable research practices among Italian research psychologists

The paper reports a survey of 277 members of the Italian Association of Psychology (AIP), 208 of whom completed it, on their use of ten questionable research practices (QRPs). It is a direct replication of John, Loewenstein and Prelec's (2012) US survey: the same ten QRPs, in the same wording, translated into Italian, with the same four questions asked about each. It is a self-report prevalence survey, not a text-mining, p-curve or meta-analytic study, and reports no distributional analysis of p-values.

## What the paper counts as a QRP

The ten QRPs are John et al.'s (2012) own items, translated by three native Italian speakers with psychology expertise (including two of the paper's authors), checked by a back-translation from a native English speaker. In the paper's own numbering: (1) in a paper, failing to report all of a study's dependent measures; (2) deciding whether to collect more data after looking to see whether the results were significant; (3) in a paper, failing to report all of a study's conditions; (4) stopping data collection earlier than planned because the result one had been looking for was found; (5) in a paper, "rounding off" a p value (for example, reporting p = .054 as p < .05); (6) in a paper, selectively reporting studies that "worked"; (7) deciding whether to exclude data after looking at the impact of doing so on the results; (8) in a paper, reporting an unexpected finding as having been predicted from the start; (9) in a paper, claiming that results are unaffected by demographic variables when actually unsure or knowing that they do; (10) falsifying data. For how these items map onto the practices named by other sources, see [[what-p-hacking-is]]; for the prevalence findings, see [[prevalence-from-self-report]].

For each QRP, four questions were asked, in an order randomised per participant: a prevalence estimate (the percentage of Italian research psychologists the respondent believed had ever used the practice), an admission estimate (the percentage of those users the respondent believed would admit to it), a self-admission (yes/no, whether the respondent had personally ever used it), and a defensibility judgement (no / possibly / yes, whether using the practice is defensible). The paper did not use John et al.'s "Bayesian Truth Serum" manipulation, reasoning that John et al. found little difference between that condition and the control condition; the survey therefore replicates only John et al.'s control-condition design.

## Survey method and participants

An invitation was emailed in October 2014 to the 1,167 members of the AIP mailing list (802 of whom were dues-paying AIP members for that year). 277 people answered at least part of the questionnaire (24% response rate on the 1,167 invited) and 208 (75% of the 277) completed it. All 277 respondents were included in the reported analyses, including partial completions, because the QRPs were presented in random order. Participants gave informed consent after being told the study's purpose and assured of anonymity; the procedure was approved by the AIP executive board and by a University of Padova ethics committee. The questionnaire was built in Qualtrics and hosted on a Tilburg University server; the anonymous data are posted at the paper's OSF page.

## Self-admission rates and the US comparison

Table 1 gives the self-admission rate (percentage answering "yes" to ever having used the practice) and 95% CI for each QRP, for the US sample from John et al.'s (2012) control condition (US CIs supplied to the authors by an author of that paper) and for the Italian sample:

| QRP | Self-admission, US (%) | 95% CI, US | Self-admission, Italy (%) | 95% CI, Italy |
|---|---|---|---|---|
| 1. Failing to report all of a study's dependent measures | 63.4 (n=486) | 59.1–67.7 | 47.9 (n=219) | 41.3–54.6 |
| 2. Deciding whether to collect more data after checking significance | 55.9 (n=490) | 51.5–60.3 | 53.2 (n=222) | 46.6–59.7 |
| 3. Failing to report all of a study's conditions | 27.7 (n=484) | 23.7–31.7 | 16.4 (n=219) | 11.5–21.4 |
| 4. Stopping data collection early on finding the looked-for result | 15.6 (n=499) | 12.4–18.8 | 10.4 (n=221) | 6.4–14.4 |
| 5. Rounding off a p value | 22.0 (n=499) | 18.4–25.7 | 22.2 (n=221) | 16.7–27.7 |
| 6. Selectively reporting studies that "worked" | 45.8 (n=485) | 41.3–50.2 | 40.1 (n=217) | 33.6–46.6 |
| 7. Excluding data after checking the impact on significance | 38.2 (n=484) | 33.9–42.6 | 39.7 (n=219) | 33.3–46.2 |
| 8. Reporting an unexpected finding as predicted | 27.0 (n=489) | 23.1–30.9 | 37.4 (n=219) | 31.0–43.9 |
| 9. Claiming results unaffected by demographic variables | 3.0 (n=499) | 1.5–4.5 | 3.1 (n=223) | 0.9–5.4 |
| 10. Falsifying data | 0.6 (n=495) | 0.0–1.3 | 2.3 (reported in text) | not extractable |

The self-admission rates were highly correlated between countries (r = .94, 95% CI [.76, .99]). The mean self-admission rate across all ten QRPs was 27.3% in Italy and 29.9% in the US. Nearly all respondents who finished the survey admitted at least one QRP: 88% in Italy, 91% in the US. Comparing confidence intervals, the US rate was significantly higher than the Italian rate for QRPs 1 and 3; the Italian rate was significantly higher only for QRP 8. QRP 9 (demographic-variable claims) had low self-admission in both countries (3.0% US, 3.1% Italy), which the paper suggests may reflect how rarely researchers examine demographic variables at all rather than a low rate of the practice itself. For QRP 10 (falsifying data), the paper states in its Discussion that 2.3% of Italian and 0.6% of US respondents admitted it ("three US and five Italian researchers"); see the extraction note below on why this is taken from the Discussion text rather than the garbled Table 1 cell for Italy.

## Defensibility judgements

Table 2 breaks the "no / possibly / yes" defensibility responses down three ways: for US respondents who admitted the QRP, for Italian respondents who admitted it, and for Italian respondents who did not admit it, with chi-squared tests (df = 2, criterion 5.99 at alpha = .05) comparing the US distribution against each Italian group (not computed for QRPs 9 and 10, where too few respondents in either country admitted the practice). For QRPs 1 through 8, fewer than 10% of admitting US respondents and fewer than 20% of admitting Italian respondents called the practice "not defensible"; admitting US respondents most often answered "yes" (defensible), while admitting Italian respondents most often answered "possibly" for seven of the eight. Italian respondents who had not admitted a QRP most often answered "no" for seven of the eight, the exception being QRP 2 (deciding whether to collect more data after checking significance), where only 28% of non-admitting Italians called it "not defensible" and over half of all Italian respondents had admitted using it; the paper reads this as evidence that the statistical consequences of the practice are not well understood in this sample.

Self-admission rates in both countries approximated a Guttman scale (a participant's exact pattern of yes/no answers is largely predictable from the count of "yes" answers alone): the coefficient of reproducibility was .87 for the Italian sample and .80 for the US sample (from John et al., 2012), which the paper reads, following John et al., as evidence of rough consensus on which practices are more unethical alongside considerable individual variation in where researchers themselves draw the line.

## Prevalence estimates

Following John et al.'s method, the paper derives three estimates of QRP prevalence from the survey, and states explicitly that none of the three is a precise estimate of actual prevalence. The self-admission rate (mean 27.3%) is expected to underestimate true prevalence, since some users will not admit using a practice. The prevalence estimate (mean 47.5%: respondents' own estimate of what percentage of Italian psychologists have used each QRP) and the derived prevalence estimate (mean 82.3%, capped at 100% where the calculation exceeded it: self-admission rate divided by the admission estimate) are both larger. As one illustration, respondents estimated that 18.7% of Italian psychology researchers had falsified data at least once, against a 2.3% self-admission rate for the same practice. The paper argues, citing participants' own comments about the difficulty of estimating others' behaviour, that the prevalence estimate and the derived prevalence estimate are not valid measures of actual prevalence, only of what researchers believe about their colleagues and about the honesty of colleagues who use these practices; it recommends self-admission as the more defensible (if conservative) figure. Italian prevalence estimates (mean 47.5%) were significantly higher than the equivalent US figure (mean 39.1%). Self-admission rates were highly correlated with both prevalence estimates (Italy: .94; US: .92) and admission estimates (Italy: .88; US: .90).

## Doubts about research integrity

Respondents were also asked how often they had doubted the research integrity of themselves, their collaborators, graduate students at their institution, researchers at their institution, and researchers at other institutions, on a four-point scale (never / once or twice / occasionally / often). About 35% of Italian and 31% of US respondents reported having doubted their own integrity on at least one occasion. About half of respondents in both countries (51% Italy, 49% US) reported occasional or frequent doubts about the integrity of researchers at other institutions; most respondents expressed strong confidence in the integrity of their collaborators and of themselves. The full response distribution is shown in Fig 2, described in the text rather than read from the image.

## Temptation to use QRPs

The paper asked a question John et al. (2012) had not asked: whether, in the past year, the respondent had been tempted to use one or more QRPs to improve their chances of publication or career advancement. Of 202 respondents to this item, 53% said never, 37% once or twice, 7% occasionally, and 3% often.

## Demographics

Table 3 breaks self-admission and defensibility down by AIP division and by career position. Self-admission rates were highest among researchers in the social, experimental and organizational divisions and lowest among developmental/education and clinical researchers; clinical psychologists were also least likely to call a QRP defensible. Self-admission rose monotonically with career stage (post-docs and PhD students 25.7%, assistant professors 25.9%, associate professors 26.3%, full professors 28.4%), though the paper notes the differences between levels are small and that researchers further into their careers have simply had more opportunities to use a QRP. No notable or systematic differences in defensibility judgements were found across career positions.

## Qualitative comments

52 of the 277 respondents left a free-text comment, ranging from 1 to 316 words, coded by two independent analysts using an open-coding grounded-theory method into eight categories (disagreements reconciled by discussion), yielding 80 category instances in total: QRP is okay (15), example of when a QRP is not inappropriate (10), publication-culture explanation, e.g. demands from reviewers or journals (12), compliment or complaint about the survey (5), question ambiguity (13), suggestion for revising the questionnaire (12), a limitation of the study's scope, e.g. that it covers only quantitative research (7), and difficulty estimating other researchers' behaviour (6). Twenty-three percent of all comments cited demands of the publication process (journals, editors or reviewers requiring the elimination of non-significant measures or conditions, or requiring an introduction rewritten to predict an unexpected finding) as a reason for having used a QRP.

## Comparison with the German replication

The paper also discusses Fiedler and Schwarz's (2016) replication among German psychologists, which reworded some QRP items for clarity and asked a different second question (in what percentage of a researcher's own published findings the practice was used, rather than a prevalence estimate about colleagues), yielding a distinct "prevalence in research" metric the paper states cannot be directly compared to the self-admission or John et al.-style prevalence estimates. The paper states that Fiedler and Schwarz mistakenly compared their German self-admission rates against the geometric means of John et al.'s three US prevalence estimates rather than against the US self-admission rates, and that once self-admission rates are compared like for like, the overall mean rates are similar across countries: 29.9% (US), 27.3% (Italy), 25.5% (Germany). The paper offers, as one possible explanation for the somewhat lower Italian and German rates, that those surveys were run later, after John et al. (2012) was published and public discussion of the reproducibility crisis had begun; the Italian survey was run in 2014, two years after John et al.

## The paper's claims

The paper's central claim is that QRP use in Italy is comparable in overall magnitude to the US, and that the consistency of self-admission rates across the US, Italian and German surveys is evidence that QRP use reflects systemic features of the international research and publication process (competitive pressure to publish, editors and reviewers favouring significant results, and the researcher choices these pressures reward) rather than a national or individual failing. It argues that defensibility judgements, however, differ more than self-admission rates: Italian respondents who admitted a QRP were much less likely than US respondents to call it outright defensible, more often saying only "possibly," and Italian respondents who had not used a QRP mostly called it indefensible, which the paper reads as evidence that Italian researchers view the practices as more clearly questionable than US researchers do, even while using them at a similar rate. It recommends greater emphasis on quality over quantity in research evaluation, preregistration of hypotheses and analysis plans, higher statistical power, and reviewers being more receptive to imperfect results.

## Concessions and limitations

The paper attributes the small but significant US/Italy differences in self-admission for QRPs 1, 3 and 8 to unknown causes, allowing that they could reflect sampling biases in either voluntary survey or a failure of the translated items to be measurement-invariant across the two languages. It notes the self-admission rate is likely an underestimate, though cites John et al.'s finding that their Bayesian Truth Serum manipulation raised self-admission by only 3.6 percentage points as evidence the underestimate is probably not large overall (while noting that underestimation may be larger specifically for the more socially disapproved practices). It explicitly disclaims the prevalence estimate and the derived prevalence estimate as valid measures of actual prevalence, for the reason given above. No chi-squared comparison was possible for QRPs 9 and 10 because too few respondents in either country admitted them. The paper offers one possible reason for the lower overall self-admission rates in Italy and Germany, namely that those surveys took place later, after the US survey was published and discussion of the reproducibility crisis had begun, while adding that the Italian survey was run in 2014, only two years after that publication.

## Extraction and reading notes

Table 1's row for QRP 10 (falsifying data) is garbled in the extraction: the label and the US 95% CI are merged into a single wide cell, and the Italian self-admission rate and CI for that row are not recoverable from the table at all. The Italian self-admission figure for QRP 10 given above (2.3%) is taken from the Discussion text instead ("2.3% of Italian research psychologists reported falsifying data as shown in Table 1... Similarly, 0.6% of US academic psychologists"), which is consistent with the paper's earlier statement that "three US and five Italian researchers admitted it." No Italian 95% CI for QRP 10 could be recovered from either the table or the body text. Table 1's CI for QRP 4 (Italy) is also garbled, printing as "6.414.4" with the dash lost; read as 6.4–14.4 by comparison with the other rows' formatting.

## Cited by

- [[prevalence-from-self-report]]
- [[what-p-hacking-is]]
- [[preregistration-as-a-remedy]]
- [[factors-associated-with-qrp-use]]
