# Corpus

Approved by Daryl Lee on 2026-09-03. Fifteen papers: eleven form the base vault, one is ingested live during the workshop, one is reserved for the model comparison, two are spares. The list is open, so papers may still be added or removed if they prove unsuitable.

## Licence verification, 2026-09-03

Every paper was selected under an OpenAlex `best_oa_location.license:cc-by` filter, then confirmed against the publisher's own statement. "Publisher page" means the licence line on the article's landing page at the publisher; "publisher JATS" means the licence element in the publisher-deposited full-text XML held at Europe PMC, used where the publisher's site blocks automated reads (PeerJ, Royal Society). Crossref is the publisher-deposited metadata record. The licence line printed in each PDF is checked again on download (build step 3.2).

Fourteen papers are CC BY 4.0. One, Hartgerink (2017), is **CC0 1.0**, a public-domain dedication rather than an attribution licence. CC0 is more permissive than CC BY and permits derivative works without restriction, so it satisfies the reason for the CC BY rule (the recording is a derivative work distributed by FORRT). Kept in the base, with the licence recorded accurately.

| # | Paper | DOI | Licence | Confirmed by | Role |
|---|---|---|---|---|---|
| 1 | Head et al. (2015) | 10.1371/journal.pbio.1002106 | CC BY 4.0 | publisher page, Crossref | base, Theme A |
| 2 | Bishop & Thompson (2016) | 10.7717/peerj.1715 | CC BY 4.0 | publisher JATS, Crossref | base, Theme A |
| 3 | Hartgerink (2017) | 10.7717/peerj.3068 | **CC0 1.0** | publisher JATS, Crossref | base, Theme A |
| 4 | Bruns & Ioannidis (2016) | 10.1371/journal.pone.0149144 | CC BY 4.0 | publisher page, Crossref | base, Theme A |
| 5 | Wicherts et al. (2016) | 10.3389/fpsyg.2016.01832 | CC BY 4.0 | publisher page | base, bridge |
| 6 | Fraser et al. (2018) | 10.1371/journal.pone.0200303 | CC BY 4.0 | publisher page, Crossref | base, Theme B |
| 7 | Agnoli et al. (2017) | 10.1371/journal.pone.0172792 | CC BY 4.0 | publisher page, Crossref | base, Theme B |
| 8 | Gopalakrishna et al. (2022) | 10.1371/journal.pone.0263023 | CC BY 4.0 | publisher page, Crossref | **live ingest**, Theme B and C |
| 9 | Hardwicke et al. (2018) | 10.1098/rsos.180448 | CC BY 4.0 | publisher JATS | base, Theme C |
| 10 | Vasilevsky et al. (2017) | 10.7717/peerj.3208 | CC BY 4.0 | publisher JATS, Crossref | base, Theme C |
| 11 | Haven, Bouter, et al. (2019) | 10.1371/journal.pone.0217931 | CC BY 4.0 | publisher page, Crossref | base, Theme C |
| 12 | Haven, Tijdink, et al. (2019) | 10.1371/journal.pone.0210599 | CC BY 4.0 | publisher page, Crossref | base, Theme C |
| 13 | Bartoš et al. (2023) | 10.1098/rsos.230224 | CC BY 4.0 | publisher JATS | model comparison, held back |
| 14 | Nissen et al. (2016) | 10.7554/elife.21451 | CC BY 4.0 | publisher API, Crossref | spare |
| 15 | Munafò et al. (2017) | 10.1038/s41562-016-0021 | CC BY 4.0 | publisher page, Crossref | spare |

Crossref's licence field for the two Royal Society papers points to the Society's data-mining policy page rather than a Creative Commons URL. That is a Crossref deposit quirk, not a licence difference; the Society's own JATS states CC BY 4.0 for both.

## Themes

- **Theme A, can p-hacking be detected from published p-values?** A four-paper published dispute. Head et al. infer widespread p-hacking from text-mined p-curves; Bishop and Thompson dispute that the method can support the inference; Hartgerink's reanalysis finds the result non-robust while declining to conclude that p-hacking is absent; Bruns and Ioannidis show the method misfiring in observational research. Carries the adjudication step.
- **Bridge.** Wicherts et al.'s checklist of researcher degrees of freedom, the mechanism both the p-curve work and the survey work are trying to measure.
- **Theme B, how common are these practices when researchers are asked?** Three self-report surveys in three populations: ecology and evolution (Fraser), Italian psychologists (Agnoli), Dutch researchers across disciplines (Gopalakrishna). Gopalakrishna is held back for the live ingest so the audience watches a third estimate land on a page already built from the first two.
- **Theme C, what produces these practices and what institutions do about them?** Two policy evaluations (Hardwicke on one journal's mandatory open-data policy; Vasilevsky on data-sharing policies across many journals) and two surveys of working conditions (Haven, Bouter, et al. on publication pressure; Haven, Tijdink, et al. on research integrity climate). Gopalakrishna also measures publication pressure, so the live ingest touches Theme C through that page specifically. It does not measure the research-integrity-climate construct of Haven, Tijdink, et al.

## References

Author lists and bibliographic details retrieved from OpenAlex and Crossref on 2026-09-03.

1. Head, M. L., Holman, L., Lanfear, R., Kahn, A. T., & Jennions, M. D. (2015). The extent and consequences of p-hacking in science. *PLoS Biology, 13*(3), e1002106. https://doi.org/10.1371/journal.pbio.1002106
2. Bishop, D. V. M., & Thompson, P. A. (2016). Problems in using p-curve analysis and text-mining to detect rate of p-hacking and evidential value. *PeerJ, 4*, e1715. https://doi.org/10.7717/peerj.1715
3. Hartgerink, C. H. J. (2017). Reanalyzing Head et al. (2015): Investigating the robustness of widespread p-hacking. *PeerJ, 5*, e3068. https://doi.org/10.7717/peerj.3068
4. Bruns, S. B., & Ioannidis, J. P. A. (2016). p-Curve and p-hacking in observational research. *PLoS ONE, 11*(2), e0149144. https://doi.org/10.1371/journal.pone.0149144
5. Wicherts, J. M., Veldkamp, C. L. S., Augusteijn, H. E. M., Bakker, M., van Aert, R. C. M., & van Assen, M. A. L. M. (2016). Degrees of freedom in planning, running, analyzing, and reporting psychological studies: A checklist to avoid p-hacking. *Frontiers in Psychology, 7*, 1832. https://doi.org/10.3389/fpsyg.2016.01832
6. Fraser, H., Parker, T., Nakagawa, S., Barnett, A., & Fidler, F. (2018). Questionable research practices in ecology and evolution. *PLoS ONE, 13*(7), e0200303. https://doi.org/10.1371/journal.pone.0200303
7. Agnoli, F., Wicherts, J. M., Veldkamp, C. L. S., Albiero, P., & Cubelli, R. (2017). Questionable research practices among Italian research psychologists. *PLoS ONE, 12*(3), e0172792. https://doi.org/10.1371/journal.pone.0172792
8. Gopalakrishna, G., ter Riet, G., Vink, G., Stoop, I., Wicherts, J. M., & Bouter, L. (2022). Prevalence of questionable research practices, research misconduct and their potential explanatory factors: A survey among academic researchers in The Netherlands. *PLoS ONE, 17*(2), e0263023. https://doi.org/10.1371/journal.pone.0263023
9. Hardwicke, T. E., Mathur, M. B., MacDonald, K., Nilsonne, G., Banks, G. C., Kidwell, M. C., Hofelich Mohr, A., Clayton, E., Yoon, E. J., Henry Tessler, M., Lenne, R. L., Altman, S., Long, B., & Frank, M. C. (2018). Data availability, reusability, and analytic reproducibility: Evaluating the impact of a mandatory open data policy at the journal *Cognition*. *Royal Society Open Science, 5*(8), 180448. https://doi.org/10.1098/rsos.180448
10. Vasilevsky, N., Minnier, J., Haendel, M., & Champieux, R. (2017). Reproducible and reusable research: Are journal data sharing policies meeting the mark? *PeerJ, 5*, e3208. https://doi.org/10.7717/peerj.3208
11. Haven, T., Bouter, L., Smulders, Y. M., & Tijdink, J. K. (2019). Perceived publication pressure in Amsterdam: Survey of all disciplinary fields and academic ranks. *PLoS ONE, 14*(6), e0217931. https://doi.org/10.1371/journal.pone.0217931
12. Haven, T., Tijdink, J. K., Martinson, B. C., & Bouter, L. (2019). Perceptions of research integrity climate differ between academic ranks and disciplinary fields. *PLoS ONE, 14*(1), e0210599. https://doi.org/10.1371/journal.pone.0210599
13. Bartoš, F., Maier, M., Shanks, D. R., Stanley, T. D., Sladekova, M., & Wagenmakers, E.-J. (2023). Meta-analyses in psychology often overestimate evidence for and size of effects. *Royal Society Open Science, 10*(7), 230224. https://doi.org/10.1098/rsos.230224
14. Nissen, S. B., Magidson, T., Gross, K., & Bergstrom, C. T. (2016). Publication bias and the canonization of false facts. *eLife, 5*, e21451. https://doi.org/10.7554/elife.21451
15. Munafò, M. R., Nosek, B. A., Bishop, D. V. M., Button, K. S., Chambers, C. D., Percie du Sert, N., Simonsohn, U., Wagenmakers, E.-J., Ware, J. J., & Ioannidis, J. P. A. (2017). A manifesto for reproducible science. *Nature Human Behaviour, 1*(1), 0021. https://doi.org/10.1038/s41562-016-0021
