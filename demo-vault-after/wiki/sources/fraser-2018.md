---
type: source
title: "Fraser et al. (2018), Questionable research practices in ecology and evolution"
description: A self-report survey of 807 ecology and evolutionary biology researchers on ten questionable research practices, comparing self-reported and estimated rates of use with two published psychology surveys.
created: 2026-09-04
updated: 2026-09-04
sources: [fraser-2018]
status: draft
generated:
  by: claude-code/claude-sonnet-5
  at: 2026-09-04
doi: 10.1371/journal.pone.0200303
licence: CC BY 4.0
---

# Fraser et al. (2018), Questionable research practices in ecology and evolution

The paper reports a survey of 807 researchers (494 ecologists and 313 evolutionary biologists) on their use of Questionable Research Practices (QRPs), including cherry picking, p hacking and HARKing, and on their estimates of how often colleagues use each practice. It is a self-report prevalence survey, not a text-mining, p-curve or meta-analytic study, and reports no distributional analysis of p-values.

## What the paper counts as a QRP

The paper defines cherry picking as failing to report dependent or response variables, or relationships, or conditions or treatments, that did not reach statistical significance or another threshold. It defines p hacking as a set of activities: checking statistical significance before deciding whether to collect more data; stopping data collection early because results reached significance; deciding whether to exclude data points only after checking the impact on significance and not reporting that impact; adjusting statistical models, for instance by including or excluding covariates, based on the resulting strength of the effect of interest; and rounding a p-value to meet a significance threshold (for example presenting 0.053 as p < .05). It defines HARKing as presenting ad hoc or unexpected findings as though predicted all along, and presenting exploratory work as though it were confirmatory hypothesis testing, attributing the first sense to Kerr (1998) and the second to Wagenmakers et al. (2012).

The survey instrument (administered via Qualtrics) asked about ten specific practices, listed here in the paper's own numbering: (1) not reporting studies or variables that failed to reach statistical significance or another desired threshold; (2) not reporting covariates that failed to reach significance or another desired threshold; (3) reporting an unexpected or exploratory finding as having been predicted from the start; (4) reporting a subset of tested statistical models as the complete set; (5) rounding off a p-value or other quantity to meet a pre-specified threshold; (6) deciding to exclude data points after first checking the impact on significance; (7) collecting more data after first inspecting whether results are significant; (8) changing to another statistical analysis after the first choice failed to reach significance; (9) not disclosing known problems in the method, analysis or data quality that could affect conclusions; (10) filling in missing data points without identifying them as simulated. Questions 1 to 9 were shown in random order; question 10 was always shown last because the authors judged it particularly controversial and did not want it to influence responses to the others.

For each practice, researchers were asked to estimate the percentage of colleagues in their field who had used it at least once, to state how often they had used it themselves (never, once, occasionally, frequently, almost always), and to state how often they believed it should be used (never, rarely, often, almost always), with an open-ended comment box after each.

For the practices that overlap with the other sources' lists, see [[what-p-hacking-is]]; for what the paper reports about prevalence specifically, see [[prevalence-from-self-report]].

## Survey participants

Corresponding-author email addresses were collected from articles in 11 ecology and 9 evolutionary biology journals, chosen as the highest-impact journals (by 5-year impact factor, ISI 2013 Journal Citation Reports) that publish a broad range of work. Ecology-journal addresses were drawn from issues between January 2014 and May 2016; evolutionary-biology and Journal of Applied Ecology addresses were added later, from issues between January 2015 and March 2017, after the authors decided, before looking at the initial data, to expand the sample. A trial release began 5 December 2016; the ecology-journal invitations were reportedly sent by 6 March (the paper does not give the year for this date, and it appears inconsistent with the December 2016 trial date; not checked against the PDF); the evolution-journal invitations went out on 19 May 2017.

After deduplication, 5,386 researchers were emailed and 807 responded (response rate 15%). The paper states that 71% (n = 573) of responses came from the ecology-journal sample and 37% (n = 299) from the evolution-journal sample; these two percentages sum to more than 100%, which the paper does not explain (not checked against the PDF). After researchers self-identified their sub-discipline (411 did so) and were reclassified accordingly, with the remainder (n = 396) left in their original journal-based category, the final sample was 61% (n = 494) ecology and 39% (n = 313) evolution.

Only 69% (558–560 of 807) completed the demographic questions. Of those, 69% identified as male, 29% as female, 0.2% as non-binary and 1% preferred not to say; 6% were graduate students, 33% postdoctoral researchers, 24% mid-career researchers or academics and 37% senior researchers or academics; ages were distributed as under 30 (11.5%), 30–39 (46.7%), 40–49 (25.9%), 50–59 (9.8%), 60–69 (4.8%) and over 70 (1.3%).

Analyses were preregistered after data collection had commenced but before the data were viewed, and run in R 3.3.3. Confidence intervals throughout are Wilson score intervals except for those on Kendall's Tau, which are bootstrapped from 1,000 samples.

## Headline prevalence figures

Across the full sample of 807, 64% of researchers reported that they had, at least once, failed to report results because they were not statistically significant (cherry picking); 42% had collected more data after inspecting whether results were significant (a form of p hacking); and 51% had reported an unexpected finding as though it had been hypothesised from the start (HARKing). These are whole-sample figures across both ecology and evolution respondents combined, as stated in the abstract and conclusion; the paper does not give a single combined confidence interval for them there (the by-discipline breakdowns, with CIs, are in Table 2, described below).

## Comparison with two psychology surveys

For the six QRPs that overlap with two earlier surveys of psychologists, the paper's Table 2 (n = 555–626) reports the percentage (with 95% CI) of researchers who had used each practice at least once, separately for Agnoli et al.'s Italian psychologists, John et al.'s US psychologists, and the paper's own ecology and evolution samples:

| Practice | Psychology, Italy (Agnoli et al.) | Psychology, USA (John et al.) | Ecology | Evolution |
|---|---|---|---|---|
| Not reporting non-significant outcome variables | 47.9 (41.3–54.6) | 63.4 (59.1–67.7) | 64.1 (59.1–68.9) | 63.7 (57.2–69.7) |
| Collecting more data after checking significance | 53.2 (46.6–59.7) | 55.9 (51.5–60.3) | 36.9 (32.4–42.0) | 50.7 (43.9–57.6) |
| Rounding off a p-value or other quantity | 22.2 (16.7–27.7) | 22.0 (18.4–25.7) | 27.3 (23.1–32.0) | 17.5 (13.1–23.0) |
| Excluding data points after checking significance | 39.7 (33.3–46.2) | 38.2 (33.9–42.6) | 24.0 (19.9–28.6) | 23.9 (18.5–30.2) |
| Reporting an unexpected finding as predicted | 37.4 (31.0–43.9) | 27.0 (23.1–30.9) | 48.5 (43.6–53.6) | 54.2 (47.7–60.6) |
| Filling in missing data without identifying it as simulated | 2.3 (0.3–4.2) | 0.6 (0.0–1.3) | 4.5 (2.8–7.1) | 2.0 (0.8–5.1) |

The paper notes that the first five items began "in a paper," in the two psychology surveys, and that the last item was called "falsifying data" in those surveys rather than the softer wording used here, which it flags as a possible influence on the response rate. It reports the results as broadly similar across the three populations, with two exceptions it names explicitly: ecologists were less likely than psychologists or evolution researchers to report collecting more data after checking significance, and both ecology and evolution researchers were less likely to report excluding data points after checking significance than either psychology sample. It also states, in the Discussion, that both ecology and evolution researchers were more likely than both psychology samples to report presenting an unexpected finding as predicted.

On the fabrication-like item (10), the paper is explicit that the comparison is confounded by wording: it asked the softer "filling in missing data points without identifying those data as simulated" rather than the psychology surveys' direct "falsifying data," and states that this change in wording, following Fiedler and Schwarz (2016), likely elevated its own reporting rate relative to the psychology figures. It declines to interpret the higher ecology-versus-evolution figure (4.5% versus 2.0%) further, noting the counts are small and the 95% CIs overlap considerably.

## Frequency of use, and doubts about integrity

Table 3 (n ranging from 488 to 539 per cell) reports the proportion of ecology and evolution researchers (combined) who had doubts, at the frequency "never," "once or twice" or "often," about the scientific integrity of five groups, split into QRPs and Scientific Misconduct. For QRPs: researchers at other institutions, never 8.9% (6.8–11.6), once or twice 56.6% (52.3–60.7), often 34.5% (30.6–38.6); research at their own institution, 27.9% (24.2–31.8) / 52.2% (47.9–56.4) / 20.0% (16.8–23.6); graduate-student research at their institution, 31.0% (27.2–35.1) / 48.6% (44.3–52.8) / 20.4% (17.1–24.0); senior colleagues or collaborators, 31.5% (27.6–35.5) / 50.8% (46.6–55.1) / 17.7% (14.7–21.2); their own research, 52.2% (48.0–56.4) / 44.6% (40.5–48.8) / 3.2% (2.0–5.0). For Scientific Misconduct the corresponding never/once-or-twice/often figures are lower throughout, for example 97.9% (96.2–98.8) never and 0.0% (0.0–0.8) often for their own research. The paper reports that concern about integrity at their own institution was roughly equal to concern about other institutions, that there was no notable difference in concern about graduate students versus senior colleagues, and that participants expressed the least concern about their own integrity, though 44.6% still reported doubts about their own QRP use (the paper's sentence; its Table 3 gives 44.6% as the "once or twice" share, with a further 3.2% "often").

Separately from Table 3, the paper reports on how often researchers who had used a practice used it at high frequency. It states that it was extremely rare for researchers to report "frequently" or "almost always" using any QRP, and that most reported usage was at low frequency ("once," "occasionally"), with many researchers reporting they had never engaged in a given practice (Figure 2, described below). Age and career stage were weak predictors of frequency of QRP use (Kendall's Tau = 0.05, 95% CI 0.001–0.069 for age; 0.04, 95% CI 0.011–0.058 for career stage), but there was a considerable correlation between how often a participant believed a practice should be used and how often they used it (Kendall's Tau = 0.6, 95% CI 0.61–0.65); those who used practices frequently were much more likely to say they should be used often.

## Disciplinary differences

The paper states that its results are most marked by how similar QRP rates were across ecology and evolution, but names one difference it interprets rather than simply reporting: ecology researchers were less likely than evolution researchers (or psychologists) to report collecting more data after checking significance (QRP7; Table 2 above). The paper's own interpretation is that this reflects the practical constraints of field versus laboratory research (field sites may be distant, and available sites or budgets exhausted) rather than a difference in researcher integrity, and it says this interpretation is supported by evidence that many ecologists who reported "never" using this practice nonetheless found it acceptable.

## Social acceptability, from the gap between self-report and estimated colleague use

For each QRP, the survey also asked researchers to estimate the percentage of colleagues who had used the practice at least once. The paper reports that self-reported use was broadly closely related to these estimates of colleague prevalence (Figure 1), but that for QRPs 2, 5, 6, 9 and 10 the estimated prevalence among colleagues was substantially higher than individual self-reported use; it reads this discrepancy as marking those five practices as the least socially acceptable in the set. Conversely, it reads little discrepancy between self-report and estimated colleague use, for QRPs 1, 4, 7 and 8, as marking those as more socially acceptable and, on that account, potentially harder to shift because researchers may not recognise them as problematic.

## Qualitative comments

At the end of each QRP question researchers could leave an open comment on why the practice should or should not be used; the paper reports that for some QRPs about half of researchers did so. Table 4 summarises, for cherry-picking (QRPs 1, 2, 4), HARKing (QRP 3) and p-hacking (QRPs 5–8), the complaints raised against each practice, the temptations researchers named, and the justifications offered, together with illustrative quotations. The most frequently offered justifications for engaging in QRPs, across the qualitative data as a whole, were publication bias, pressure to publish, and the desire to present a neat, coherent narrative. The paper reports having found no major differences between the ecology and evolution groups in a qualitative assessment of the comments, and treats the volume of comments as evidence of a research community engaged with these issues. A full qualitative analysis is referred to a supplementary document (S2) that is not part of the extracted source.

## The paper's claims

The paper's central claim, stated in the Discussion, is that QRPs are broadly as common in ecology and evolution as in psychology, and that this is unsurprising because publication bias and publish-or-perish culture operate across disciplines. It frames the QRP rate as important evidence for initiatives to improve research practice even in the absence of direct large-scale replication studies in ecology and evolution, arguing that the link between QRPs and irreproducibility is rooted in statistical theory (citing Ioannidis, 2005) so that a high QRP rate alone should be sufficient grounds for concern.

It argues that its frequency data (never/once/occasionally/frequently/almost always) are a novel contribution, because the psychology surveys it compares against asked only whether a practice had been used "at least once," and that its qualitative data offer new insight into the perceived acceptability of, and justifications for, QRPs. It recommends that journals in ecology and evolution adopt editing and reviewing checklists for complete and transparent reporting, that preregistration and registered-report formats be encouraged to minimise HARKing, and that open code and data be encouraged where possible. On preregistration specifically, it states that a thorough preregistration specifies hypotheses, sample-size decisions, data-exclusion criteria and planned analyses in advance, and that this helps protect against HARKing, cherry-picking and p-hacking; it also names mandatory data-archiving policies at some journals (citing Whitlock, 2011) as an existing institutional lever, with the qualification that compliance with such policies falls short of complete (citing Roche et al., 2015).

## Concessions and limitations

The paper states several limitations of its own work. Its sample may be biased because it contacted only researchers who had published in high-impact-factor journals, which it says likely limited the number of graduate-student respondents (6%) and means its results should be understood as reflecting mainly postdoctoral, mid-career and senior researchers rather than the discipline as a whole. It expects a self-selection bias among survey respondents, and reasons that if more methodologically confident researchers were more likely to respond, this would most likely produce an underestimate rather than an overestimate of QRP rates in the wider community. To protect anonymity it did not collect data on researchers' country of origin, and it notes that the two psychology surveys it draws on suggest QRP rates may vary by country, so it cannot speculate on this for ecology and evolution. It collected responses between November 2016 and July 2017 and allows that QRP rates could in principle have changed within that window, but suspects that its response categories (never/once/occasionally/frequently/almost always) would not have been sensitive enough to pick up any such change even if it occurred.

The paper also flags interpretive grey areas in its own data: for QRP 3 (HARKing), it notes that many ecology and evolution papers never overtly state hypotheses, so implying an expected result through how the introduction is framed may or may not count as HARKing; for QRP 6 (excluding data after checking significance), some respondents reported having done so but explained that the underlying reason was discovering a model error or an assumption violation rather than the significance check itself, leaving it unclear whether their case is "questionable" as recorded.

## Cited by

- [[prevalence-from-self-report]]
- [[what-p-hacking-is]]
- [[preregistration-as-a-remedy]]
- [[factors-associated-with-qrp-use]]
