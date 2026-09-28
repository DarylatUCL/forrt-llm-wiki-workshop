---
type: source
title: "Perceptions of research integrity climate differ between academic ranks and disciplinary fields: Results from a survey among academic researchers in Amsterdam"
description: A survey of 1,298 academic researchers across four Amsterdam institutions measuring perceived research integrity climate with the Survey of Organizational Research Climate (SOuRCe), and how its seven subscales differ by academic rank and disciplinary field.
created: 2026-09-04
updated: 2026-09-28
sources: [haven-2019b]
status: draft
generated:
  by: claude-code/claude-sonnet-5
  at: 2026-09-04
doi: 10.1371/journal.pone.0210599
licence: CC BY 4.0
---

# Perceptions of research integrity climate differ between academic ranks and disciplinary fields

## Research question and definition

The paper asks whether academic researchers from different academic ranks and disciplinary fields experience the research integrity climate differently, in two university medical centers and two universities in Amsterdam; the aim is stated as descriptive, so no direction of difference was specified in advance. Organizational climate is defined, quoting Schneider, Ehrhart and Macey, as "the shared meaning organizational members attach to the events, policies, practices, and procedures they experience and the behaviors they see being rewarded, supported, and expected." The paper situates its instrument, the Survey of Organizational Research Climate (SOuRCe), in two conceptual frameworks it names explicitly: organizational justice theory, under which people who regard their organization's decisions as fairer are more likely to trust it, abide by its decisions and refrain from questionable behaviour, while perceived injustice is reasoned to make researchers more likely to compensate by engaging in misconduct or questionable research practices; and the Institute of Medicine's *Integrity in Scientific Research* report, which frames the research environment as an open system in which factors such as ethical leadership and the visibility of integrity policies can stimulate or diminish responsible research. The paper cites a finding by Crain, Martinson and Thrush that a more favourable organizational research climate is associated with lower self-reported questionable research practices, and cites Wells et al.'s prior SOuRCe study finding that researchers in different career stages, and different organizational subunits (with disciplinary field one contributing factor), perceive the climate differently; neither finding is independently measured or restated as this paper's own result. The paper states this is the first study to investigate research integrity climate in the Netherlands.

## Participants and procedure

The institutions were Vrije Universiteit Amsterdam, University of Amsterdam, and the two Amsterdam University Medical Centers. After securing endorsement from each institution's deans and rectors and a data-sharing agreement, each institution supplied email addresses for all its researchers and PhD students; researchers were eligible if doing research at least one day a week on average (>0.2 FTE). The electronic survey, built in Qualtrics, was distributed in May 2017. An information email was sent first; one week later the official invitation with a unique survey link and a link to a non-response survey followed, with three reminders to non-responders. The online survey opened with informed consent and an inclusion check, and concluded with three demographic items: gender, academic rank, and disciplinary field. The survey contained three instruments: SOuRCe, the Publication Pressure Questionnaire, and a 60-item list of major and minor research misbehaviours; this article presents only the SOuRCe results (see "Related instruments" below). The study was approved by the Scientific and Ethical Review board of the Faculty of Behaviour & Movement Sciences, Vrije Universiteit Amsterdam (Approval Number VCWE-2017-017R1), and the intended statistical analyses were preregistered on the Open Science Framework under the title "Academic Research Climate Amsterdam."

## Instrument

SOuRCe evaluates the perceived research climate on a 5-point scale from 1 ("not at all") to 5 ("completely"), plus a "No basis for judging OR not relevant to my field of work" option (the paper extended this option from the original SOuRCe's "No basis for judging" alone, and slightly reworded three of the original 28 items, in consultation with the SOuRCe design team, to make them applicable outside biomedicine; two of the original 28 items were, the paper states, inadvertently omitted from the distributed questionnaire owing to a programming error). A subscale score is the mean of its valid non-missing items, valid provided at least half the subscale's items were answered with a substantive response; higher scores mean a more favourable perception throughout, which required reverse-coding the Integrity Inhibitors items (originally phrased as the presence of inhibiting conditions) so that, like every other subscale, a higher score means a better climate. The seven subscales, drawn from the paper's Table 1:

| Subscale | Level | Items | What it measures |
|---|---|---|---|
| RCR Resources | Institutional | 6 | Perceived educational opportunities, available policies and professionals to consult, and leaders who actively support responsible conduct of research (RCR) |
| Regulatory Quality | Institutional | 3 | Fairness of regulatory committees such as the Medical Ethical Testing Committee |
| Integrity Norms | Departmental | 4 | Whether norms about research integrity exist in one's department |
| Integrity Socialization | Departmental | 4 | Whether the department effectively socializes junior researchers into research integrity |
| Supervisor/Supervisee Relations | Departmental | 3 | Fairness, availability and respect between supervisors and supervisees |
| (Lack of) Integrity Inhibitors | Departmental | 6 | Whether resource shortages, suspicion or competition among colleagues make responsible research harder (reverse-scored) |
| Expectations | Departmental | 2 | Fairness of the department's expectations for publishing and obtaining external funding |

## Statistical method

Analyses were preregistered on the OSF. The paper first computed overall and rank/field-stratified mean subscale scores; for subscales significantly associated with rank or field, it ran post-hoc Bonferroni-corrected F-tests and pairwise mean differences (MD) with 95% CIs between rank or field groups; it then fitted association models (rank or field as independent variable, subscale score as dependent variable), checking for confounding (e.g. by gender) and effect modification, reporting confounder-adjusted estimates where applicable. A separate post-hoc sensitivity analysis, described under "Limitations" below, corrected the standard errors of these association models for clustering (respondents nested in departments, disciplines and institutions) using an estimated Variance Inflation Factor built from unpublished intraclass correlations supplied by the Wells et al. study authors, since privacy constraints meant the paper's own data carried no institution-, department- or field-level identifiers finer than the four broad disciplinary categories.

## Response rate

From Fig 1 (percentages against the total population of 7,548 Amsterdam academic researchers): 7,548 email addresses were collected; 83 bounced as undeliverable; 109 researchers asked to be unsubscribed; 2,274 (30%) opened the questionnaire; of those, 1,298 (17% of the total sample; 57% of those who opened it) answered enough to complete at least one SOuRCe subscale. Only 2% of invitees completed the brief non-response questionnaire.

## Differences between academic ranks

For the six subscales significantly associated with rank (Integrity Norms, Integrity Socialization, Integrity Inhibitors, Supervisor-Supervisee Relations, Expectations and RCR Resources), the paper reports both a regression model against associate/full professors as reference category (Table 2) and Bonferroni-corrected pairwise mean differences read from Fig 2's lettered brackets (recovered from the figure image and cross-checked against Table 4's effect sizes; see extraction defects below for the sign and punctuation errors found in the caption text and corrected here):

Table 2 regression (Beta, SE, 95% CI, relative to associate & full professors, N = 210 reference):

| Subscale (F, p, df) | PhD students (N = 481) | Postdocs & assistant professors (N = 294) |
|---|---|---|
| Integrity Norms (3.21, .041, 2) | -.108 (.058), CI [-.221, -.005] | -.138 (.062), CI [-.259, -.016] |
| RCR Resources (14.043, <.001, 2) | -.386 (.102), CI [-.586, -.186] | -.476 (.110), CI [-.691, -.260] |
| Integrity Inhibitors (4.908, .008, 2) | -.195 (.063), CI [-.317, -.073] | -.150 (.068), CI [-.283, -.017] |
| Integrity Socialization (19.584, <.001, 2) | -.394 (.065), CI [-.522, -.266] | -.368 (.071), CI [-.507, -.228] |
| Supervisor-Supervisee Relations (11.552, <.001, 2) | -.284 (.062), CI [-.405, -.162] | -.278 (.068), CI [-.411, -.144] |
| Expectations (11.772, <.001, 2) | -.202 (.070), CI [-.340, -.064] | -.335 (.075), CI [-.482, -.189] |

(313 respondents did not disclose academic rank.)

Fig 2 pairwise Bonferroni-corrected mean differences (MD, 95% CI), letters as labelled in the figure:

- RCR Resources: PhD students < associate/full professors, MD = -.23, CI [-.39, -.07]; postdocs/assistant professors < PhD students, MD = -.16, CI [-.30, -.02]; postdocs/assistant professors < associate/full professors, MD = -.39, CI [-.56, -.21].
- Integrity Norms: postdocs/assistant professors < associate/full professors, MD = -.15, CI [-.29, -.00].
- Integrity Socialization: PhD students < associate/full professors, MD = -.39, CI [-.55, -.24]; postdocs/assistant professors < associate/full professors, MD = -.37, CI [-.54, -.20].
- Supervisor-Supervisee Relations: PhD students < associate/full professors, MD = -.29, CI [-.43, -.14]; postdocs/assistant professors < associate/full professors, MD = -.28, CI [-.44, -.11].
- Integrity Inhibitors: PhD students < associate/full professors, MD = -.19, CI [-.35, -.05].
- Expectations: PhD students < associate/full professors, MD = -.23, CI [-.39, -.07]; postdocs/assistant professors < associate/full professors, MD = -.36, CI [-.53, -.18].

Effect modification: the rank-Expectations and rank-Integrity Norms associations were confounded by gender (adjusting for it weakened but did not remove the associations); RCR Resources showed effect modification by gender specifically, reported in Table 3 (means by rank and gender): PhD students, male 3.29 / female 3.10; postdocs and assistant professors, male 2.99 / female 3.01; associate and full professors, male 3.33 / female 3.50. Fig 2 and Table 2 display statistics already corrected for confounding or reporting effect modification where applicable.

Effect sizes (Hedges' g, Table 4, Cohen's bands: .20 small, .50 medium, .80 large, 1.30 very large): RCR Resources, PhD < associate/full g = .29 (small), postdocs/assistant < PhD g = .19 (small), postdocs/assistant < associate/full g = .47 (small); Integrity Norms, postdocs/assistant < associate/full g = .22 (small); Integrity Socialization, PhD < associate/full g = .18 (small), postdocs/assistant < associate/full g = .87 (large); Supervisor-Supervisee Relations, PhD < associate/full g = .36 (small), postdocs/assistant < associate/full g = .43 (small); Integrity Inhibitors, PhD < associate/full g = .25 (small); Expectations, PhD < associate/full g = .27 (small), postdocs/assistant < associate/full g = .43 (small). (The paper's own band labels are reported as printed; the RCR Resources postdocs/assistant-versus-associate/full value of .47 is labelled "small" by the paper despite sitting close to its own .50 medium cutoff.)

## Differences between disciplinary fields

Disciplinary field was significantly associated with Regulatory Quality and Expectations (Table 5, humanities as reference, N = 100):

| Subscale (F, p, df) | Biomedical sciences (N = 557) | Natural sciences (N = 103) | Social sciences (N = 237) |
|---|---|---|---|
| Regulatory Quality (3.472, .016, 3) | .395 (.113), CI [.174, .617] | .391 (.164), CI [.070, .711] | .395 (.125), CI [.150, .640] |
| Expectations (9.709, <.001, 3) | .366 (.089), CI [.193, .540] | .483 (.113), CI [.261, .705] | .142 (.099), CI [-.052, .337], not significant |

(281 respondents did not disclose disciplinary field.)

Fig 3 pairwise Bonferroni-corrected mean differences, letters as labelled in the figure (sign and punctuation errors in the caption text corrected as above):

- Regulatory Quality: humanities < social sciences, MD = -.34, CI [-.66, -.01]; humanities < biomedical sciences, MD = -.38, CI [-.68, -.08].
- Expectations: social sciences < biomedical sciences, MD = -.26, CI [-.44, -.09]; social sciences < natural sciences, MD = -.38, CI [-.61, -.11]; humanities < biomedical sciences, MD = -.34, CI [-.57, -.10]; humanities < natural sciences, MD = -.45, CI [-.75, -.15].

The disciplinary-field associations with Regulatory Quality and Expectations were confounded by academic rank; the main effect of discipline remained significant after adjustment, and Fig 3 and Table 5 display the confounder-adjusted statistics.

Effect sizes (Table 4): Regulatory Quality, humanities < biomedical sciences g = .50 (medium), humanities < social sciences g = .42 (small); Expectations, social sciences < biomedical sciences g = .29 (small), social sciences < natural sciences g = .42 (small), humanities < biomedical sciences g = .39 (small), humanities < natural sciences g = .55 (medium).

Overall (across-rank and across-field) mean subscale scores are shown only as bars in Figs 2 and 3, without accompanying printed values in the running text; visually, in both figures, Integrity Inhibitors and Integrity Norms sit at the top of the "Total sample" bars and Integrity Socialization and RCR Resources at the bottom, with Regulatory Quality, Supervisor-Supervisee Relations and Expectations in between (taken from the figure; no numeric overall means are given anywhere in the extracted text, so none are reported here as numbers).

## The paper's own interpretation

Departmental Expectations were perceived more negatively by junior researchers, which the paper reasons may reflect junior researchers' career prospects depending more directly on meeting publication and funding expectations than senior researchers' do; the paper likens this to Martinson et al.'s (2006) finding that mid- and early-career scientists perceived more organizational injustice than senior scientists on a differently constructed measure (effort put in versus rewards received), a comparison the paper draws itself and which is reported here as the paper's own comparison, not independently verified.

On Supervisor-Supervisee Relations, the paper notes its own finding (junior researchers scoring lower) is the opposite of what Martinson et al. found in a US Department of Veterans Affairs sample (senior staff scoring the scale lower), and that Wells et al.'s more traditional US academic sample found no notable rank difference on this scale; the paper flags junior researchers' perception of suboptimal supervision as potentially alarming given the association, elsewhere in the literature it cites, between poor mentoring and emotional stress, and its independent characterisation as one of the more impactful research misbehaviours.

On Integrity Socialization, the paper contrasts its finding (juniors lower) with Wells et al., who found US junior researchers reporting the *highest* Integrity Socialization; the paper reasons this discrepancy may mean senior researchers acknowledge the importance of socializing junior researchers into research integrity in principle without this receiving sufficient attention in practice.

On RCR Resources, the paper reasons that policy communication in academia is often addressed to deans, department heads or principal investigators, which could explain why, matching Wells et al.'s finding, senior researchers in this sample also score higher. The gender effect modification (female researchers perceiving more RCR Resources except among PhD students, where males perceived more) is offered two tentative readings the paper does not adjudicate between: that female PhD students may be more willing to voice concern about resource availability, and a citation to evidence that women value procedural justice more than men in general, with the paper itself cautioning that no gender interactions have been reported elsewhere in the SOuRCe literature, so it is premature to conclude the general finding applies here.

On Integrity Inhibitors, the paper reads PhD students' lower score (indicating more perceived inhibiting conditions such as suspicion and competition among colleagues) as mirroring the same pattern in Wells et al., and suggests associate and full professors may have grown accustomed to inhibitors such as publication pressure and regard them as less threatening.

On Integrity Norms, the paper reasons postdocs and assistant professors scoring lower than senior researchers may indicate this group witnesses less responsible research and more questionable research practices, paralleling both Wells et al.'s finding that postdocs scored lowest on more than half the SOuRCe subscales in the US, and a separate citation (not restated here) that mid-career scientists admit to more misbehaviours than senior scientists.

On disciplinary field, the paper reasons humanities researchers score lowest on Regulatory Quality because regulatory bodies play a smaller role in fields like literature or philosophy than in fields like biomedicine where rules and regulation are more pivotal, so humanities researchers encounter such bodies less. On Expectations, the paper reasons that publishing norms in fields like philosophy or law (books, national or specialist journals) are not valued by departments the way journal publications are, which may explain humanities researchers' lower scores; both field findings are described as matching Wells et al.'s pattern (natural sciences highest, humanities lowest on Expectations).

## Strengths of the study, per the paper

The paper states this is the first publicly available study of research integrity climate in a European country, and that it is premature to compare its results to the US studies (Wells et al., Martinson et al.) because any difference could stem from a range of known and unknown unmeasured factors neither study captured; it frames its own data as a baseline for repeated future administration of SOuRCe to track developments over time. It also notes SOuRCe's focus on observable local-environment characteristics gives direct, actionable feedback to academic leaders, illustrating this with its own low Integrity Socialization finding as a target for institutional investigation into how socialization could be improved.

## Limitations the paper concedes

The paper states in its Study limitations section that "our completion rate of 18% is low," which does not match the 17%-of-total-sample figure given in the Results section from the same 1,298/7,548 count (see extraction defects; both figures are reported here as the paper states them, unreconciled). The paper argues an 18% completion rate is comparable to other online surveys and need not indicate response bias by itself, and reports that only 2% of non-responders completed the brief non-response questionnaire, too few, the paper states, to base solid conclusions on. Comparing sample demographics (excluding the two medical centers, for which comparable population data was unavailable) to publicly available population data for the two universities, the paper reports: 27% of the population are full or associate professors against 21% of the sample; 40% are assistant professor or postdoc against 38% of the sample; 32% are PhD students against 41% of the sample.

The paper reports a possible gender bias: 57% of the sample was female against a national academic figure of 39% and an Amsterdam figure of 42%, which the paper attributes mainly to overrepresentation of female PhD students (68% of the sample's PhD students against a national 45%), citing evidence of women's greater general willingness to participate in surveys; the paper reports having corrected for gender as a confounder where relevant (and separately reporting the RCR Resources gender-by-rank effect modification in Table 3), and concludes on this basis that the sample's selectivity is unlikely to have biased its results.

Because only gender, academic rank and disciplinary field were collected (to protect respondent and institutional privacy), the paper states it could not obtain institution-, department- or specific-field-level classification, so it may have missed meaningful variability within its broad disciplinary categories, and a standard multilevel model correcting for clustering was infeasible; it estimates the impact of clustering instead via a post-hoc Variance Inflation Factor correction to the standard errors, using unpublished intraclass correlations for institution that the Wells et al. study authors calculated for this paper. Applying this correction, rank was no longer significantly associated with Integrity Norms or Integrity Inhibitors (the paper names these two but refers to "these three subscales", and does not name a third), while the paper states that its other rank associations remained significant despite the correction; disciplinary field remained significantly associated with both Expectations and Regulatory Quality after the same correction (S2 and S3 Tables, not part of the extraction; the paper's own summary of their conclusions is reported here since the underlying tables are unavailable).

## Implications, per the paper

The paper concludes the research integrity climate is perceived differently by junior and senior researchers and by researchers from different disciplinary fields, and argues this stresses the need for tailored rather than one-size-fits-all interventions, citing Crain et al. for the latter point. It notes increased attention to research integrity education (tutorials, seminars, courses) sits uneasily with its own low Integrity Socialization and RCR Resources scores among junior researchers, and argues integrity needs to become embedded in daily departmental practice rather than taught in a single course. It flags PhD students' perception of integrity-inhibiting conditions (suspicion and competition among colleagues) as a particularly concerning finding, calling for thoughtful guidance from senior researchers.

## Related instruments used on the same sample, not reported here

The same survey also administered the revised Publication Pressure Questionnaire and a 60-item research misbehaviours inventory; the paper states these are reported in separate papers. One of those companion papers, on perceived publication pressure by academic rank and disciplinary field using the same Amsterdam sample, is Haven, Bouter, et al. (2019), which has its own source page in this wiki (`haven-2019a`); per section 3 of the schema, source pages never wikilink other source pages, so it is named here in plain text without a wikilink, and none of its findings are restated here. A second companion piece, on research misbehaviours, is cited in the paper's own Methods section as Bouter, Tijdink, Axelsen, Martinson and ter Riet (2016), "Ranking major and minor research misbehaviors," which is not one of the fifteen `corpus.md` papers and is named here without restating any finding, since it is outside the corpus.

## Extraction notes on figures and other defects

- Fig 2's and Fig 3's caption text, giving the lettered mean-difference (MD) and confidence-interval (CI) values for each pairwise rank or field comparison, contains a scattering of sign and punctuation errors: several MDs and CI lower bounds that should read as negative (since every described comparison states one group scored *lower* than another) are printed without their minus sign (e.g. "MD=.28,CI=-.44,-.11" for what must be MD = -.28; "MD=.26,CI=-.44,-.09" for MD = -.26; "MD=-.45,CI=.75,-.15" for CI lower bound -.75), and one value is printed with a double decimal point ("MD=..23,CI=..39,..07" for MD = -.23, CI [-.39, -.07]). These were corrected on the reasoning that a mean difference described in the same sentence as "X scored lower than Y" must be negative, and that a 95% CI must bracket its own MD; the corrected values are reported above. Both figure images were also opened directly to confirm which lettered bracket groups with which subscale (the image groups the letters as `abc / d / ef / gh / i / jk` for Fig 2's seven subscale panels and `ab / cdef` for Fig 3's two panels), which the caption text's lettering agrees with once the letter groupings are read off the image rather than assumed from the caption's own ordering. The bar heights in both images confirm the direction of every difference (the shorter bar is always the group stated to have scored lower) but carry no printed numeric values of their own, so the corrected MD/CI figures above are not independently confirmed to the decimal by the image, only their direction. Not checked against the PDF.
- The Study limitations section states a completion rate of "18%," while the Results section's own figures (1,298 of 7,548) give 17.2%, rounding to 17%; both figures are reported above as the paper states them in their respective sections, without deciding which is the paper's intended figure.
- Five of the thirteen files in `figures/` are referenced from the markdown (the journal masthead badge, Fig 1's flow diagram, and Figs 2 and 3, four images in total; a fifth near-duplicate hash was not separately referenced). The remaining eight are not referenced by name; by position and file size they are consistent with crops of Tables 1 through 5 (which are otherwise captured as HTML tables in the running text) and journal badges, so nothing appears to be lost, though this was not confirmed by opening each image individually.
- The Data Availability Statement is split by the intervening author-affiliation block, corresponding-author email and Abstract: "...To ease the possible exchange of data with fellow" is followed several blocks later by "researchers, a concept data sharing agreement can be found here...". No text appears lost, but the sentence must be read across the break; not load-bearing for any claim recorded here.
- A duplicate "(PDF)" line appears after the S3 Table caption in the Supporting Information list, with no accompanying caption text of its own; likely a formatting artefact of how the extraction rendered the supporting-information list rather than a second, uncaptioned file, but not checked against the PDF.
- The first author's ORCID icon is rendered as a literal "<sub>ID</sub>" superscript/subscript fragment after the name, appearing twice (Haven and, separately, Martinson and Bouter); a cosmetic extraction artefact of the ORCID badge, not a content loss.
- Journal furniture (an "## OPEN ACCESS" heading, "Citation," "Editor," "Received/Accepted/Published," and the Copyright line) is interleaved into the body ahead of the Abstract rather than rendered as metadata; the Copyright paragraph confirms the CC BY licence recorded in `corpus.md`.
- The Supporting Information list (S1 Appendix, S2 Appendix, S1 Protocol, S1-S3 Tables) is captioned but none of the underlying files is part of the extraction; the full pairwise and regression tables behind the VIF clustering correction (S2 and S3 Tables) are therefore known only from the paper's own prose summary of their conclusions, not from the underlying tables themselves.

## Cited by

- [[research-integrity-climate-by-rank-and-field]]
