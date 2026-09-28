# What each demo step changed

`demo-vault/wiki/` is the wiki before the demo. `demo-vault-after/wiki/` is the wiki after the steps were run once with Opus 5.5 on 28 September 2026: steps 1 to 4 in the Claude desktop app at effort Low, the repair from the command line. This page says in words what changed between the two, so you do not need a diff tool. The agent's own record is at the top of `demo-vault-after/wiki/log.md`.

A live run will not match this one word for word. The agent writes differently each time, and the workshop run on 30 September is a separate run.

## Step 1, ingest of Gopalakrishna et al. (2022)

| Page | Change |
|---|---|
| `sources/gopalakrishna-2022.md` | Created. The summary of the paper in its own terms. |
| `concepts/factors-associated-with-qrp-use.md` | Created. A new topic no existing page covered. It records a disagreement with Agnoli and colleagues on career stage, shown as a disagreement. |
| `concepts/prevalence-from-self-report.md` | The third survey added. Its figure is not set beside the other two surveys' figures, because the three measure different things. |
| `concepts/publication-pressure-by-rank-and-field.md` | A second source added, with the two instruments kept distinct. The page stops being provisional. |
| `concepts/what-p-hacking-is.md` | The incentives section gains the measured association with publication pressure. |
| `sources/fraser-2018.md`, `sources/agnoli-2017.md` | "Cited by" lists gain the new concept page. |
| `index.md`, `log.md` | New pages listed; one log entry. |

## Step 2, the judgement

Nothing changed. The judgement page was recorded before the demo and is the same in both folders.

## Step 3, the query

| Page | Change |
|---|---|
| `questions/what-published-p-values-establish.md` | Created. The answer, with citations, and the maintainer's view attributed to the maintainer. |
| `index.md`, `log.md` | The question listed; one log entry. |

While answering, the agent noticed the planted error and recorded it in the log for the lint step. It did not repair it.

## Step 4, lint

Only `log.md` changed. The mechanical checks found nothing to fix. The judgement checks reported twelve issues and the agent waited for confirmation, as the schema requires.

Of the twelve: one is the planted error; eight are in text the agent had written minutes earlier in steps 1 and 3; three were in the starting pages. Those three were then checked against the papers and corrected in both folders, which is why the lint entry lists them as open while the pages already carry the correction. The entry dated 28 September and headed "build" records this.

The lint entry also says the extracted text of Bishop and Thompson drops a sentence. That report is wrong: the sentence is in the extracted text. It is left in the log as the agent wrote it.

## Step 4b, the repair

| Page | Change |
|---|---|
| `concepts/text-mined-p-values.md` | The planted error corrected. The Results-section proportion changes from .583 to .417, the claim that a surplus survived is replaced by no surplus in either section, and "no discipline significant" now covers both sections. |
| `log.md` | One entry recording the repair and the passage it was checked against. |

Nothing else changed. The agent checked the figure against the paper's Table 1 before editing. This step was run on the same day with the same model from the command line, in a fresh session, not in the app session that ran steps 1 to 4.

## What is left uncorrected on purpose

The eight issues the lint found in the agent's fresh output are still on the pages in `demo-vault-after/`. They show what unverified agent output looks like, and what a lint report is for.
