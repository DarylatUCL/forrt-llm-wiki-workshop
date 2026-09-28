---
type: source
title: "Gopalakrishna et al. (2022), Prevalence of questionable research practices, research misconduct and their potential explanatory factors"
description: The Dutch National Survey on Research Integrity (6,813 completing respondents across all fields and ranks), reporting the three-year prevalence of frequent engagement in 11 questionable research practices, randomised-response estimates of fabrication and falsification, and their associations with background characteristics and 11 explanatory factor scales including publication pressure.
created: 2026-09-28
updated: 2026-09-28
sources: [gopalakrishna-2022]
status: draft
generated:
  by: claude-code/claude-opus-5-5
  at: 2026-09-28
doi: 10.1371/journal.pone.0263023
licence: CC BY 4.0
---

# Gopalakrishna et al. (2022), Prevalence of questionable research practices, research misconduct and their potential explanatory factors

The paper reports the National Survey on Research Integrity (NSRI), a cross-sectional, web-based, anonymised survey of academic researchers in the Netherlands across all disciplinary fields and academic ranks. It asks about engagement in 11 questionable research practices (QRPs) and in fabrication and falsification (FF) over the previous three years, and relates these to five background characteristics and a set of explanatory factor scales. It is a self-report survey; it reports no analysis of published p-values. Results on responsible research practices from the same survey are reported in a separate paper.

## Survey design and sample

All academic researchers working at or affiliated with at least one of 15 universities or 7 University Medical Centers in the Netherlands were invited by email. To be eligible a respondent had to do on average at least 8 hours of research-related work a week, belong to one of four fields (life and medical sciences; social and behavioural sciences; natural and engineering sciences; arts and humanities), and hold one of three ranks (PhD candidate or junior researcher; postdoc or assistant professor; associate or full professor). The survey was run by a third party, Kantar Public, which sent the invitations and reminders and passed the research team an anonymised dataset only after the full data analysis plan had been preregistered. It was open for seven weeks, with three reminders.

Eight of the 22 institutions supported the survey and supplied email addresses; addresses at the others were taken from public sources such as university websites and PubMed. Of 63,778 emails sent, 9,529 eligible respondents started the survey after the screening questions and 6,813 completed it. A response percentage could be calculated reliably only for the supporting institutions: 21.2% in the Results (21.1% in the limitations section). There was no item non-response, since respondents had either to complete the survey or withdraw. Male and female respondents are in about equal proportions; nearly 90% do empirical research.

## Instrument

Every respondent received the same 11 QRP items and two FF items, all referring to their own behaviour in the last three years; the three-year window was chosen to limit recall bias. The QRPs were adapted from an earlier survey of participants at World Conferences on Research Integrity (Bouter et al., 2016), in which 60% of participants came from biomedicine, and checked for applicability across fields in discipline-specific focus groups. Each QRP was scored on a 7-point scale from 1 (never) to 7 (always), with no intermediate labels, plus a "not applicable" option. The 11 QRPs, as labelled in Table 2, are:

1. insufficient attention to the equipment, skills or expertise
2. insufficiently supervised or mentored junior co-workers
3. inadequate research designs or unsuitable measurement instruments
4. unfairly reviewed manuscripts, grant applications or colleagues
5. conclusions not sufficiently substantiated
6. improper referencing of sources
7. inadequate notes of the research process
8. failed to report important study details in publications
9. not submitting or resubmitting valid negative studies for publication
10. insufficient inclusion of study flaws and limitations in publications
11. selectively cited references to enhance findings or convictions

Fabrication ("making up of data or results") and falsification ("manipulating research materials, data or results") were asked with the randomised response technique, yes or no only. The paper describes the technique as well validated for eliciting more honest answers to sensitive questions, and restricted it to these two items because it lengthens the survey.

Twelve explanatory factor scales were selected from psychometrically tested scales in the research integrity literature: scientific norms, peer norms, perceived work pressure, publication pressure, funding pressure, mentoring (responsible and survival), competitiveness, organisational justice (distributional and procedural), and perceived likelihood of QRP detection by collaborators and by reviewers. Some were used verbatim, some adapted and one (funding pressure) newly created; the funding pressure scale could not be piloted but had a Cronbach's alpha of 0.76 in the survey. The publication pressure scale is described as used previously in highly similar samples. To shorten the survey, each invitee received one of three random subsets of 50 of the 75 explanatory factor items ("missingness by design"), and the missing items were handled by multiple imputation (50 imputed datasets). Distributional and procedural organisational justice correlated above 0.8 and were merged into one scale, so the regression tables carry 11 scales.

## Outcomes and definitions

The paper analyses three outcomes:

- **Prevalence of a QRP**: the percentage of respondents scoring that QRP 5, 6 or 7, among respondents who did not answer "not applicable" to it. The paper chose this cut-off for comparability with other studies.
- **Any frequent QRP**: a score of 5, 6 or 7 on at least one of the 11 QRPs.
- **Overall QRP mean**: the average score across the 11 QRPs, with "not applicable" recoded to 1 (never).
- **Any FF**: admitting at least one instance of fabrication or falsification.

These were modelled with linear (overall mean), logistic (any frequent QRP) and ordinal (any FF) regression. Every model includes all five background characteristics (field, rank, gender, empirical research or not, supporting institution or not) and all explanatory factor scales, entered as z-scores.

## Prevalence of QRPs

All figures are percentages of respondents who deemed the QRP applicable, for the last three years, with 95% confidence intervals, from Table 2 (6,813 respondents overall).

| QRP | Overall prevalence (score 5 to 7) |
|---|---|
| 9. Not (re)submitting valid negative studies | 17.5 (16.4, 18.7) |
| 10. Insufficient inclusion of study flaws and limitations | 17.0 (16.1, 18.0) |
| 2. Insufficient supervision or mentoring of junior co-workers | 15.0 (14.1, 15.9) |
| 1. Insufficient attention to equipment, skills or expertise | 14.7 (13.8, 15.7) |
| 7. Inadequate notes of the research process | 14.5 (13.7, 15.5) |
| 11. Selective citation to enhance findings or convictions | 14.0 (13.2, 14.9) |
| 3. Inadequate designs or unsuitable instruments | 4.3 (3.9, 4.9) |
| 5. Conclusions not sufficiently substantiated | 4.0 (3.6, 4.5) |
| 8. Failed to report important study details | 2.8 (2.4, 3.3) |
| 4. Unfair review | 0.8 (0.6, 1.1) |
| 6. Improper referencing of sources | 0.6 (0.5, 0.9) |
| Any frequent QRP | 51.3 (50.1, 52.5) |

By field, any frequent QRP was 55.3% (53.4, 57.1) in life and medical sciences, 50.2% (48.0, 52.5) in social and behavioural sciences, 49.4% (46.8, 52.0) in natural and engineering sciences and 42.1% (38.3, 46.1) in arts and humanities. By rank it was 52.5% (50.3, 54.7) for PhD candidates and junior researchers, 52.3% (50.4, 54.2) for postdocs and assistant professors and 48.9% (46.7, 51.0) for associate and full professors. PhD candidates and junior researchers had the highest prevalence for 8 of the 11 QRPs.

"Not applicable" answers were common and uneven. QRP 9 had the highest share of "not applicable" in every field, highest in arts and humanities (72.3%). About half of PhD candidates and junior researchers (48.7%) answered "not applicable" to QRP 4. Arts and humanities respondents had the highest share of "not applicable" for 9 of the 11 QRPs, and PhD candidates and junior researchers for 10 of the 11.

## Prevalence of fabrication and falsification

Randomised-response estimates for the last three years, all respondents: fabrication 4.3% (2.9, 5.7), falsification 4.2% (2.8, 5.6), any FF 8.3% (6.2, 10.3). By field, any FF was 10.4% (7.1, 13.7) in life and medical sciences, 5.7% (1.8, 9.5) in social and behavioural sciences, 7.6% (3.1, 12.1) in natural and engineering sciences and 8.4% (1.6, 15.3) in arts and humanities. Arts and humanities respondents had the lowest fabrication estimate, 0.7% (0, 5.1), and the highest falsification estimate, 6.1% (1.4, 10.9). By rank, any FF was 8.9%, 7.3% and 8.9% for the junior, middle and senior groups respectively, with intervals spanning roughly 4 to 13 points.

## Explanatory factor scores by rank and field

Table 1 gives mean scale scores on a 1 to 7 scale. Postdocs and assistant professors had the highest scores of the three rank groups for publication pressure (4.2, against 3.8 for PhD candidates and junior researchers and 3.7 for associate and full professors), funding pressure (5.2) and competitiveness (3.7), and the lowest for peer norms (4.1) and organisational justice (4.1). Arts and humanities respondents had the highest field scores for work pressure (4.8), publication pressure (4.1, against 3.8 to 4.0 in the other fields) and competitiveness (3.8), and the lowest for mentoring, peer norms and organisational justice. Scientific norm subscription scores (overall 6.1) were much higher than peer norm scores (overall 4.2) in every field and rank. Table 1 is descriptive; the paper reports no significance tests for these differences.

## Associations with background characteristics

From Table 3, with postdocs and assistant professors as the reference rank: being a PhD candidate or junior researcher was associated with higher odds of any frequent QRP (OR 1.16, 95% CI 1.01 to 1.32), but not with a significantly different overall QRP mean (0.03, -0.01 to 0.07). Against men, women (OR 0.77, 0.69 to 0.85) and respondents who did not disclose gender (OR 0.65, 0.45 to 0.96) had lower odds of any frequent QRP and lower overall QRP means. Respondents not doing empirical research also had lower odds (OR 0.76, 0.64 to 0.91). Against life and medical sciences, all three other fields had lower odds of any frequent QRP, lowest in arts and humanities (OR 0.61, 0.50 to 0.74). None of the background characteristics was significantly associated with any FF; the intervals are wide.

## Associations with explanatory factors

From Table 4, per standard deviation increase on each scale, adjusted for all other scales and the background characteristics:

- **Publication pressure**: overall QRP mean +0.10 (0.08 to 0.12); odds of any frequent QRP multiplied by 1.22 (1.14 to 1.30); any FF OR 1.09 (0.75 to 1.59), not significant.
- **Scientific norm subscription**: overall QRP mean -0.12 (-0.13 to -0.10); any frequent QRP OR 0.88 (0.83 to 0.93); any FF OR 0.79 (0.63 to 1.00).
- **Peer norms**: overall mean -0.03 (-0.05 to -0.02) in Table 4 (-0.04 in the text); any frequent QRP OR 0.91 (0.86 to 0.97).
- **Organisational justice**: overall mean -0.04 (-0.06 to -0.02); any frequent QRP OR 0.91 (0.85 to 0.98).
- **Perceived likelihood of detection by reviewers**: no association with the QRP outcomes; any FF OR 0.62 in the abstract and text, 0.63 (0.44 to 0.88) in Table 4.
- **Survival mentoring**: overall mean +0.04 (0.02 to 0.06); no association with any frequent QRP or any FF. **Responsible mentoring**: overall mean -0.02 (-0.04 to 0.00).
- **Work pressure and competitiveness**: overall mean +0.02 each (0.00 to 0.04), described by the paper as only marginal.
- **Funding pressure and likelihood of detection by collaborators**: no association with any outcome.

## The paper's claims

The paper summarises its findings as one in two researchers engaging frequently in at least one QRP over the last three years, and one in twelve reporting having falsified or fabricated at least once. It states that publication pressure "appears to lead to the largest increase" in the odds of any frequent QRP and reads this as support for initiatives to change the "publish or perish" reward system. It reads the association between perceived detection by reviewers and lower FF as suggesting that reviewers may have an important role in preventing misconduct, and argues that open science practices such as data sharing are likely to raise the chance of detection. It reads the survival and responsible mentoring associations as showing that mentors can push behaviour either way, in line with an earlier study by Anderson et al. (2007). On junior researchers it relays, from an earlier Amsterdam study, the suggestion that inexperience and poor supervision may lead them to commit QRPs unintentionally, and calls for a safe learning environment with adequate supervision.

On prevalence, the paper says 51.3% suggests QRPs may be more prevalent than previously reported, citing other surveys that found self-reported QRPs in the range of 13 to 33%, and reports a higher prevalence of misconduct than earlier surveys, which it cites as around 2 to 3%. It immediately qualifies the QRP comparison: the high figure may be due to its cut-off, and differing cut-offs, answer scales and QRP sets make results between surveys not directly comparable. It says its FF estimates may be more valid than earlier ones because of the randomised response technique, and that it cannot tell whether the higher FF estimate in life and medical sciences reflects more misconduct or more willingness to report it. Its recommendations are greater emphasis on scientific norm subscription, strengthening reviewers as gatekeepers of research quality, and curbing the "publish or perish" incentive system.

## Concessions and limitations

- Response could be calculated only for the eight supporting institutions, since webscraped addresses at the others could not be checked against the eligibility criteria. With no reliable national figures matching the eligibility criteria, the paper cannot assess the sample's representativeness, even on the five background characteristics. It argues its results are nonetheless valid because its main findings align with other research integrity surveys.
- Recoding "not applicable" to "never" in the linear models does not distinguish a behaviour that does not apply from one intentionally avoided, so these analyses may underestimate true intentional QRPs. The paper reports trying other recodes and remains confident in its preregistered choice.
- The "any frequent QRP" definition (5, 6 or 7) is a choice; widening "frequent" would have given higher estimates. Other surveys used different numbers and definitions of QRPs, which hampers direct comparison.
- Respondents promoted within the three-year window may be misclassified by rank; years in rank were not collected for privacy reasons, so the impact cannot be assessed, though the paper believes it minor.
- The high share of "not applicable" in arts and humanities suggests the chosen QRPs may not capture what counts as a QRP in that field.

## Extraction and reading notes

- The extraction does not preserve the bold type that Tables 3 and 4 use to mark statistical significance; significance above is read from whether the 95% interval excludes 1 (odds ratios) or 0 (coefficients), and from the paper's own text.
- The table footnotes say the models contain "all 10 explanatory factor scales", while Table 4 lists 11 (12 scales with two merged). Reported as the tables give them.
- The text gives arts and humanities a mentoring score of 3.5; Table 1 gives 3.6 (survival) and 3.4 (responsible).
- The Discussion describes the survival and responsible mentoring associations as "moderate", while the summary of findings calls mentoring only weakly associated with the overall mean; the coefficients are given above as Table 4 prints them.
- The Discussion says PhD candidates and junior researchers "reported 10 of the 11 QRPs as being not applicable"; the Results say this group has the highest share of "not applicable" for 10 of 11. The Results wording is used above.
- The citation attached to the publication pressure scale's previous use points to a reference that is not a publication pressure instrument, and the extracted text does not name the scale; its items are in a supplementary table not included in the extraction. The page therefore does not name the instrument.

## Cited by

- [[prevalence-from-self-report]]
- [[publication-pressure-by-rank-and-field]]
- [[what-p-hacking-is]]
- [[factors-associated-with-qrp-use]]
