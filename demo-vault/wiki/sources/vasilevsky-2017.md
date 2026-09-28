---
type: source
title: "Vasilevsky et al. (2017), Reproducible and reusable research: Are journal data sharing policies meeting the mark?"
description: A landscape survey of the data sharing policies of 318 biomedical journals, scoring each on a six-level rubric adapted from Stodden, Guo and Ma, and testing the association of policy strength with journal impact factor, publishing volume and open-access status.
created: 2026-09-04
updated: 2026-09-28
sources: [vasilevsky-2017]
status: draft
generated:
  by: claude-code/claude-sonnet-5
  at: 2026-09-04
doi: 10.7717/peerj.3208
licence: CC BY 4.0
---

# Vasilevsky et al. (2017), Reproducible and reusable research: Are journal data sharing policies meeting the mark?

Vasilevsky, Minnier, Haendel and Champieux. *PeerJ* 5, e3208, submitted 10 November 2016, accepted 20 March 2017, published 25 April 2017. The authors are based at Oregon Health & Science University (OHSU), in the OHSU Library, the Department of Medical Informatics and Clinical Epidemiology, and the OHSU-PSU School of Public Health.

## What the paper set out to do

The paper investigates the pervasiveness and quality of data sharing policies among biomedical journals, as reflected in the journals' own editorial policies and instructions to authors. It is motivated by the view, attributed to several funders, professional societies and publishers, that data availability is one necessary component for assessing replication and validation studies, and by publishers' position as a "leverage point" through which data sharing norms could be enforced.

## Sample and method

The sample was drawn from Thomson Reuters' InCites 2013 Journal Citation Reports (JCR), restricted to journals classified in the Web of Science categories Biochemistry and Molecular Biology, Biology, Cell Biology, Crystallography, Developmental Biology, Biomedical Engineering, Immunology, Medical Informatics, Microbiology, Microscopy, Multidisciplinary Sciences, and Neurosciences, chosen to capture the journals publishing most peer-reviewed biomedical research. The original pull covered 1,166 journals publishing 213,449 articles. This list was filtered to the top quartile by impact factor (IF) or by number of 2013 articles published, and manually reviewed to exclude short-report and review journals and titles judged outside basic medical or clinical research. The final sample was 318 journals, which published 130,330 articles in 2013: 27% of the original journal list and 61% of its citable articles. The 2014 JCR was used alongside the 2013 data in the analyses below; the sample itself was not revised when the 2014 report appeared. A check against the 2015 JCR found no significant differences in the distribution of IF or citable items by year, or in subsets defined by data sharing mark; the 2015 results are reported only on the paper's GitHub repository, not in the extracted text.

Two independent curators divided the journal list and manually reviewed each journal's online author instructions and editorial policies between February and June 2016, then spot-checked each other's work. The review was restricted to information communicated directly to submitting authors; peripheral, footnoted links to further pages were not considered unless authors were specifically directed to consult them to understand or comply with the policy.

Each journal's data sharing policy was ranked on a rubric adapted from Stodden, Guo and Ma (2013), reproduced here as the paper's own measurement instrument (Table 3):

- **Data sharing mark (DSM).** 1: required as a condition of publication, barring exceptions. 2: required, but no explicit statement of the effect on publication or editorial decisions. 3: explicitly encouraged or addressed, but not required. 4: mentioned indirectly. 5: only protein, proteomic and/or genomic data sharing addressed. 6: no mention.
- **Journal access mark** (whole-journal model, hybrid publishing not considered): 1 open access, 0 subscription.
- **Protein, proteomic or genomic data sharing required with deposit to a specific data bank:** a yes, b no.
- **Recommended sharing method:** A public online repository, B journal hosted, C by reader request to authors, D multiple methods equally recommended, E unspecified.
- **If journal hosted:** a will host regardless of size, b has a file-size limit, c unspecified.
- **Copyright or licensing of data:** a explicitly stated or mentioned, b no mention.
- **Archival or retention policy** (how long data should be retained): a explicitly stated, b no mention.
- **Reproducibility or an analogous concept noted as a purpose of the policy:** a explicitly stated, b no mention.

Beyond the DSM itself, the curators also recorded the recommended sharing method, any copyright or licensing recommendation, any statement about how long data should be retained, and any mention of reproducibility or an analogous concept, on the stated rationale that these characteristics relate to a growing body of best-practice recommendations for data sharing, including the TOP Guidelines. Each journal was further classified as open access or subscription, based on inclusion in the Directory of Open Access Journals and confirmed against the journal's own website; where the two sources disagreed the website's own statement was used, though the paper does not report how often this occurred beyond calling it rare.

Four independent curators were randomly assigned to re-score a 12.5% subsample (40 journals, 10 each) for reliability. Percentage agreement across the rubric's dimensions ranged from 92.308% to 100%, and Cohen's kappa ranged from .629 to 1.0 (full breakdown by dimension in Table 5, "Curator reliability"; see the extraction defect on table numbering below).

Continuous variables (IF, total citable items) are summarised with medians and interquartile ranges rather than means, because a Shapiro-Wilk test found both non-normally distributed (p < 0.001 for both); nonparametric tests were used throughout. The association between IF and the six-level DSM was tested with a Kruskal-Wallis one-way ANOVA, separately for 2013 and 2014 JCR data, with post-hoc pairwise two-sample Wilcoxon tests (Holm-adjusted for multiple comparisons) comparing the two-level collapse of DSM (required vs not required). The association between the two-level DSM and open-access status was tested with Pearson's chi-squared test; the six-level DSM against open-access status was tested with Fisher's exact test instead, because of low cell counts in some DSM categories. The association between open-access status and data sharing weighted by publishing volume was tested by counting citable items per category and applying Pearson's chi-squared test. All analyses were run in R 3.2.1; code and data are on the authors' GitHub repository, not part of the extracted source.

## Results

### How common and how strong are the policies

Of the 318 journals, 38 (11.9%) required data sharing as a condition of publication (DSM 1) and 29 (9.1%) required it without an explicit statement of the consequences for publication decisions (DSM 2). A further 74 (23.3%) explicitly encouraged or addressed data sharing without requiring it (DSM 3), 29 (9.1%) mentioned it only indirectly (DSM 4), and 47 (14.8%) addressed only protein, proteomic or genomic data sharing (DSM 5). The remaining 101 (31.8%) made no mention of data sharing at all (DSM 6).

### Publishing volume by policy strength

The median number of citable items per journal was 243.0 in 2013 and 237.5 in 2014, across a total of 130,330 citable items in 2013 and 131,107 in 2014. Only 67 journals (21.1%) required data sharing (DSM 1 or 2), but these published 42.1% of the citable items in each of 2013 and 2014; with PLOS ONE (a very high-volume DSM 1 journal) removed, the required-journal share of citable items falls to 23.6% (2013) and 24.9% (2014).

### Impact factor and policy strength

The median 2013 IF was 8.2 for DSM 1 journals against 3.5 for DSM 6 (no-mention) journals. Impact factor was significantly associated with the six-level DSM (Kruskal-Wallis, 5 df, p < 0.001, in both 2013 and 2014 data). Pairwise Wilcoxon tests (Holm-adjusted) found DSM 1 journals had significantly higher IF than DSM 3, 4, 5 and 6 journals (p < 0.001, < 0.001, 0.04, < 0.001 respectively for 2013 data, similar in 2014); DSM 2 journals had significantly higher IF than DSM 3, 4 and 6 (p = 0.034, 0.0072, 0.0033); and DSM 5 journals had significantly higher IF than DSM 3, 4 and 6 (p = 0.0022, < 0.001, < 0.001). IF did not differ significantly between DSM 1 and 2, nor between DSM 2 and 5. Collapsing to a two-level required (DSM 1, 2; median 2013 IF 6.8) versus not-required (DSM 3-6; median 2013 IF 4.0) comparison, the difference remained highly significant (Wilcoxon, p < 0.001, both years). The paper's Figure 2 plots the median IF for each of the six DSM categories in both report years as boxplots; beyond the DSM 1 and DSM 6 medians given above, the paper's text does not state the other four categories' medians as numbers. Read from the figure itself (marked as taken from the figure, not the text): the boxplots for DSM 1 and DSM 2 sit at a similar, higher level; DSM 3 sits below them; DSM 4 lower still; DSM 5 rises again above DSM 3 and 4, consistent with the pairwise test result that DSM 5 significantly exceeds DSM 3, 4 and 6; and DSM 6 sits at the lowest level alongside DSM 4. No exact intermediate values are reported here beyond this ordering, since the figure does not carry printed values.

### Open access and data sharing

At the journal level, there was no significant association between the six-level DSM and open-access status (Fisher's exact test, p = 0.07), nor between the collapsed two-level DSM and open-access status (chi-squared, df = 1, p = 0.62): journals requiring data sharing were not more likely to be open access than journals that did not. At the citable-item level, however, the association was highly significant (chi-squared, df = 1, P < 2e-16): an open-access citable item was much more likely to have been published in a journal with a data sharing requirement. The paper's text states this as "the proportion of open access journals that require data sharing is much larger than the proportion of subscription journals (64.3% vs 11.3%)", but its Table 7 shows these are citable-item figures: 64.3% of the citable items in journals requiring data sharing were open access, against 11.3% in journals not requiring it, while the journal-level figures are 16.42% against 13.15%. With PLOS ONE removed, the citable-item figure for requiring journals falls to 16.0%, still above 11.3% (chi-squared, df = 1, P < 2e-16 again). By DSM category, 23.7% of DSM 1 journals were open access (9 of 38, though these 9 open-access journals accounted for 81.9% of DSM 1's citable items, or 31% with PLOS ONE removed); 6.9% of DSM 2 journals were open access (2 of 29); 14.9% of DSM 3 journals (11 of 74); none of the 29 DSM 4 journals; 14.9% of DSM 5 journals (7 of 47); and 14.9% of DSM 6 journals (15 of 101).

### Recommended sharing method

Among the 217 journals that addressed data sharing in some form (DSM 1 to 5, i.e. excluding the 101 DSM 6 journals), 57.6% (125) recommended a public online repository, 20.7% (45) a journal-hosted method, 1.8% (4) sharing by reader request to the authors, 5.1% (11) stated multiple methods as equally recommended, and 14.8% (32) did not specify a method. Among the 67 journals that required data sharing (DSM 1 or 2), 85% (57) recommended a public repository. Among journals recommending a journal-hosted method, 88.8% (40 of 45) did not specify any file-size limitation.

### Licensing, retention and reproducibility mentions

Of the 217 journals that addressed data sharing (DSM 1 to 5), only 7.3% (16) explicitly mentioned copyright or licensing considerations. Restricting to the 67 journals that required data sharing (DSM 1 or 2), only 16.4% (11) mentioned licensing, though these 11 journals published 31.9% of the 2013 citable items among the 217 journals that addressed data sharing at all. Only 2 journals, out of the full 318, addressed how long shared data should be retained.

Reproducibility or an analogous concept was mentioned by 16.9% (54) of the full 318-journal sample. Among the 67 journals requiring data sharing (DSM 1 or 2), 65.5% (44) mentioned reproducibility as a purpose of the policy.

## Discussion, in the paper's own terms

The paper reads its results as confirming earlier investigations (named in plain text: Piwowar, Chapman and Wendy, 2008; Barbui, 2016; McCain, 1995) that only a minority of biomedical journals require data sharing, while noting that the picture looks more promising when weighted by publishing volume, since the minority of journals that require sharing publish a disproportionate share of the literature. Like Piwowar and Chapman's earlier study, the paper reports finding that a large proportion of the journals examined, 40%, required deposition of omics data to a specific repository; this is the paper's own figure, given as a point of agreement with that earlier study rather than a number recomputed on the wiki's own reading of the rubric categories above.

The paper reads the significant association between higher IF and stronger data sharing requirements as consistent with several other studies (named in plain text: Piwowar, Chapman and Wendy, 2008; Stodden, Guo and Ma, 2012; Sturges et al., 2015; Magee, May and Moore, 2014), and offers as an interpretation that more prestigious journals may be better positioned, and more willing, to impose new requirements on authors.

On open access, the paper states that its finding, that open-access journals were no more likely than subscription journals to require data sharing, contrasts with an earlier finding from Piwowar and Chapman (2008); it offers as a possible explanation that its own sample covered more journals, including more open-access journals, than the earlier study, and suggests some open-access journals may be less willing to impose additional requirements for lack of the prestige, or the resources, of more established titles.

The paper frames its central result as a "two-pronged problem": first, that only a minority of the journals studied have a strong data sharing requirement; second, that among the policies that do exist, guidance is relatively ambiguous and does not specify the practices (licensing, retention, method) that would ensure shared data is maximally available and reusable. It reports that 65.7% of journals with a data sharing requirement addressed the concept of reproducibility, but that, consistent with earlier investigations (Piwowar, Chapman and Wendy, 2008; Sturges et al., 2015), most data sharing policies gave no specific guidance on the practices that would ensure maximal availability and reusability. It draws a parallel with its own earlier study (Vasilevsky et al., 2013), which found that most biomedical research resources are not uniquely identifiable in the literature regardless of a journal's impact factor.

## Limitations conceded by the paper

The sample was restricted to the top quartile, by publishing volume or by impact factor, of the Web of Science categories the authors judged to constitute the biomedical corpus, which the paper states introduced "inherent biases": the 2014 median IF for the sampled journals was 4.16, against 2.50 for all journals in the same Web of Science categories, and the median 2014 citable-item count was 237.5 for the sample against 94.0 for all such journals. In hindsight, the paper states it would have been valuable to have analysed more nuanced aspects of policy quality, such as whether minimal information or metadata standards were addressed, or whether shared data was itself reviewed during peer review. The paper is explicit that many of the policies reviewed were difficult to interpret, containing ambiguous or fragmented information, and that despite the authors' confidence in their scoring, there may be gaps between the score assigned to a policy and the journal's actual editorial intent. It also notes that some policies changed after the data collection window; Springer's July 2016 policy update (cited to a blog post by Freedman, 2016) is given as an example.

## Planned follow-up work described by the paper

The paper states an intention to maintain a community-curated, regularly updated public repository of journal data sharing policies extending beyond this study's sample, using a schema built on the rubric used here and on the TOP Guidelines and FAIR (and FAIR-TLC) principles, and to convene stakeholders to develop recommendations and template policy language. It also states, as a single sentence with no further detail, that "a follow-up study will look at the data availability for articles associated with the journals in this study." No further description, timeline or result of that follow-up study is given in the extracted text, and the extracted text does not name a resulting publication; it is not attributed to any other paper in `corpus.md`.

## Conclusions

The paper restates its two-pronged problem as its conclusion: first, that given the attention the benefits of data sharing have received, it is "problematic" that only a minority of the journals studied have implemented a strong data sharing requirement; second, that among the policies that do exist, guidelines vary and are "relatively ambiguous." It states plainly that the biomedical literature as a whole lacks policies that would ensure underlying data is maximally available and reusable, and that this is "problematic if we are to realize the outcomes and improvements that open data is supposed to facilitate."

## Cited by

- [[open-data-policy-effect-on-availability]]
