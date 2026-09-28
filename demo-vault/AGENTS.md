# Schema for this wiki

This folder is a personal literature wiki on questionable research practices, maintained jointly by a human maintainer and an AI agent. The maintainer supplies the papers and the judgement; the agent does the reading, writing, linking and checking. This file is the contract between them. Read it in full before touching anything under `wiki/`.

## 1. Three layers

```
corpus.md        the list of papers, their licences and roles; human-owned, do not edit
sources/         one folder per paper: PDF, extracted markdown, figures; IMMUTABLE
wiki/            every page the agent writes; the wiki proper
CLAUDE.md        this schema (AGENTS.md is a byte-identical copy for other tools)
prompts.md       the exact prompts used to run the three workflows
```

`sources/` is never edited, renamed or added to by the agent. If an extraction is wrong, say so in the ingest log and work around it; do not fix the source.

## 2. What lives in `wiki/`

```
wiki/index.md            one line per page, grouped by type; the map of the wiki
wiki/log.md              one entry per workflow run, newest first, headed `## [YYYY-MM-DD] <ingest|query|lint|build> | <subject>` (the subject of an ingest is the paper's slug; `build` is reserved for the maintainer's own housekeeping entries)
wiki/sources/            one page per paper, named by slug (head-2015.md)
wiki/concepts/           one page per concept, question-shaped where possible
wiki/questions/          one page per answered query
wiki/judgements/         the maintainer's recorded views; the agent writes here only on instruction
```

### Page types and what belongs in each

**Source page** (`wiki/sources/`). One per paper. What the paper did, what it found, what it claims, and what it concedes, in the paper's own terms and with its own numbers. It is a faithful summary, not an assessment: no comparison with other papers, no verdict on whether the paper is right. Include the paper's stated limitations. Wiki pages carry text only: describe a figure or table in words rather than embedding an image from `sources/`. The figure images under `sources/` may be consulted when the extracted text lacks what a figure shows; a number read from an image is marked as taken from the figure. Include the exact figures that a reader would want to cite, with the qualification that the paper attaches to them (population, measurement window, denominator, item set). A number without its qualification is a wrong number.

**Concept page** (`wiki/concepts/`). One per topic. Normally a topic that more than one paper speaks to; while the wiki is small, a concept page may rest on a single paper, and then carries `provisional: true` in its frontmatter until the page cites a second source, at which point the flag is removed. This is where synthesis happens. State what the sources agree on, where they disagree, and what the disagreement turns on. Every claim carries a citation. Where papers disagree, present both sides and name the disagreement as a disagreement; never resolve it by picking a side. If the maintainer has recorded a judgement on the disagreement, link to it under a heading of its own (see section 4).

**Question page** (`wiki/questions/`). The answer to a query put to the wiki. Dated. Cites the concept and source pages it drew on. Marked at the top as generated from the wiki on that date, so a reader knows it can go stale. If the answer draws on a judgement page, it says so and attributes the view to the maintainer, never to a paper.

**Judgement page** (`wiki/judgements/`). The maintainer's own view on a question the sources leave open: which side of a dispute they find persuasive, why, and what evidence would change his mind. Written by the agent only when the maintainer dictates it, and only in `wiki/judgements/`. A judgement cites sources but is not a source. Nothing in a judgement page is ever restated elsewhere as a finding.

### Required frontmatter

Every content page (everything under `wiki/sources/`, `wiki/concepts/`, `wiki/questions/` and `wiki/judgements/`) starts with YAML frontmatter. Missing or malformed frontmatter is a lint failure. `index.md` carries only a title and date; `log.md` has no frontmatter.

```yaml
---
type: source | concept | question | judgement
title: Human-readable title
description: One sentence saying what the page covers.
created: YYYY-MM-DD
updated: YYYY-MM-DD
sources: [head-2015, bishop-2016]     # slugs of every paper the page cites; a source page lists its own slug; empty list allowed only for judgements
status: draft | stable                 # stable = the maintainer has verified the page against its sources; the agent sets it only when told to
generated:
  by: <tool>/<model>                   # e.g. claude-code/claude-fable-5-1 or codex/gpt-5-6
  at: YYYY-MM-DD
verified:                              # present only when status is stable; added on the maintainer's instruction
  - by: human:<maintainer's identifier>
    at: YYYY-MM-DD
provisional: true                      # concept pages only, while the page rests on a single source
---
```

Source pages additionally carry `doi:` and `licence:`, copied from `corpus.md`. Judgement pages additionally carry `author: maintainer`.

`type`, `status`, `generated` and `verified` borrow their shape and values from the Open Knowledge Format (OKF) v0.2 trust and lifecycle fields, so that verification status is machine-readable and recognisable to anyone who knows OKF. The wiki is **not** a conformant OKF bundle and does not claim to be: OKF requires markdown links rather than wikilinks, full ISO datetimes, `sources` entries carrying a `resource`, and its own index and log layouts, and this wiki keeps Obsidian links and plain dates because people read these pages. Converting the wiki into a bundle is a mechanical step for anyone who wants one.

### Naming

Slugs are lower-case, hyphenated, first author surname plus year: `head-2015`, `bishop-2016`, `haven-2019a`. Concept and question pages use a short descriptive slug: `p-curve-as-evidence.md`, `prevalence-from-self-report.md`. Filenames and wikilink targets are the same string.

## 3. Citation and linking rules

1. **Every source-derived claim on a concept, question or judgement page carries a citation**, written as a wikilink to the source page: `[[head-2015]]`. A claim with no citation is a lint failure. This includes numbers, directions of effect, and characterisations of what a paper argues. A source page does not cite itself inline; its provenance is the paper named in its frontmatter. On a judgement page the Reason cites sources; the Verdict and the defeater are the maintainer's own and need none.
2. **Cite only papers in `sources/`.** A wikilink citation requires a source page under `wiki/sources/`; a corpus paper that has not yet been ingested is named in plain text like any other outside work, and the link is added on concept, question and judgement pages when its source page exists. Source pages never wikilink other source pages, so a plain-text name on a source page stays as it is. If a source page mentions a paper the corpus does not contain (in its own literature review, say), name it in plain text without a wikilink and do not attribute findings to it. A source page may say that the paper argues from other work, naming that work ("the paper cites a survey by John et al., 2012"), but it does not restate that work's findings or numbers as if the wiki had read them. Where the paper's own argument rests on a figure it relays from other work, the source page may give that figure attributed to the paper's citation ("the paper relies on Schuemie et al.'s estimate that ..."); concept pages do not carry such relayed figures. The wiki knows what it has read and nothing else.
3. **Numbers travel with their qualifications.** A prevalence figure is stated with its population, measurement window and denominator. Two figures from different surveys are never placed in a ranking or a single sentence of comparison unless the qualifications are stated in the same place and the comparison is explicitly marked as loose. Surveys that use different items, windows and populations do not measure the same thing.
4. **Distinct constructs stay distinct.** Two papers that use the same word for different instruments (publication pressure measured two different ways, for instance) are not merged into one figure or one claim. Name the instrument.
5. **Link both ways.** A concept page that cites a source links to it, and the source page lists the concept pages that cite it under `## Cited by`. A content page with no inbound links from another content page is an orphan and a lint failure; a link from `index.md` does not count. Question pages are exempt: they are answers, listed in `index.md` and dated, and nothing need link to them. `index.md` and `log.md` are not content pages and need none.
6. **Update `index.md`** whenever a page is created or renamed. Update `log.md` on every workflow run.
7. **Disagreements are shown, not settled.** Where papers conflict, the concept page presents each position with its citation and states what the conflict is about. The agent never decides who is right.

## 4. The maintainer's judgement is kept separate

This is the rule the whole wiki depends on.

- The maintainer's own views live only in `wiki/judgements/`, one page per judgement, with `type: judgement`, `author: maintainer` and an empty `sources` list allowed in the frontmatter.
- A concept page may refer to a judgement, but only under its own heading, `## Maintainer's judgement`, and only as a link with a one-line pointer: "The maintainer has recorded which side they find persuasive; see [[judgement-p-curve-dispute]]." The content of the judgement is not copied into the concept page.
- A question page that draws on a judgement attributes it explicitly: "The maintainer's recorded view is that ..." It never writes "the evidence shows" or "the literature concludes" for anything that comes from a judgement page.
- A judgement page states three things, each under its own heading: **Verdict** (which side, in one sentence), **Reason** (why, citing sources), **What would change my mind** (the evidence that would reverse it). Dated. Revised in place with the date updated, not appended to.
- The agent never writes, extends or paraphrases a judgement unprompted. If a query seems to call for one, the answer says the wiki has no recorded judgement on that question.

## 5. Workflows

### Ingest

Input: the slug of a folder under `sources/`. Steps, in order:

1. Read the extracted markdown in full. If the source folder holds a `known defects.md`, read it too; it lists extraction faults found at QA, is not exhaustive, and does not replace reading the extraction. Note any extraction defect that affected what you wrote (garbled numbers, missing sections) in the log entry rather than guessing what was meant.
2. Write the source page per section 2, with frontmatter.
3. Read every existing concept page. For each one the paper bears on, update it: add the paper's contribution with citations, add or sharpen a disagreement if the paper creates or joins one, and keep every existing qualification. Never delete a qualification or a citation to make room. Never duplicate a page that already covers the topic; extend it. A concept page's `description` is revised whenever an ingest widens its scope. Any page you edit gets its `updated` and `generated` fields set to this run, its `status` set back to `draft`, and any `verified` entry removed: verification does not survive an edit, and the maintainer re-verifies. Adding or removing a link under `## Cited by` is not an edit for this purpose and leaves the page's metadata alone.
4. Create new concept pages only for topics that no existing page covers. Prefer extending. On an empty or nearly empty wiki, seed a small number of concept pages (three to five) on topics that other papers in `corpus.md` are likely to speak to, rather than one page per section of the paper.
5. Add `## Cited by` links on **every** source page that a created or modified concept page now cites, not only the new source page.
6. Update `index.md` and add a log entry headed `## [YYYY-MM-DD] ingest | <paper slug>` listing every page created or modified, with one line on what changed in each. Keep the entry short: one bullet per page, then extraction defects only if they affected what was written, then genuine unresolved ambiguities in the schema, each in a line or two. The log is a record of what changed, not a report; long reasoning belongs in the run's reply to the maintainer. Query and lint runs use the prefixes `query` and `lint`. The fixed prefix makes the log searchable with a one-line grep.
7. Do not touch `wiki/judgements/`.

### Query

Input: a question. Steps: read `index.md`; read the concept and source pages that bear on the question; write a question page per section 2 that answers with citations, presents any disagreement as a disagreement, and, where it draws on a judgement page, retrieves and attributes all three of its parts (the verdict, the reason, and what would change the maintainer's mind); add it to the index and the log. If the wiki does not contain enough to answer, the page says so rather than filling the gap from general knowledge.

### Lint

Two layers, run in this order.

**Mechanical checks** (a script could do these; the agent does them by reading, but the answer is the same either way). They apply to the content pages, meaning everything under `wiki/sources/`, `wiki/concepts/`, `wiki/questions/` and `wiki/judgements/`; `index.md` and `log.md` have their own formats and are checked only for the last two bullets:

- every content page has valid frontmatter with all required fields
- every content page is listed in the index, and every page the index lists exists
- every source page has at least one inbound link from a concept page
- on concept, question and judgement pages, the `sources:` list matches the source-page wikilinks used as citations on that page (links under `## Cited by`, links to concept, question or judgement pages, and index links do not count); a source page's `sources:` is its own slug and is exempt from this match
- no citation to a slug that has no folder under `sources/`
- no headings with nothing under them (a heading followed directly by a sub-heading is not empty)
- every wikilink in `wiki/` resolves to an existing page
- `index.md` and `log.md` are well formed (the log's entries carry the dated prefix; the index may have empty sections for page types that do not yet exist)

**Judgement checks** (only a reader can do these):

- two pages that make incompatible claims about the same finding: report both, identify which one the source supports, and say which page should change
- a claim that has drifted from what its cited source says: report the claim, quote the source, propose the correction
- a number that has lost its qualification, or two survey figures placed in a comparison the sources do not license
- anything from a judgement page restated elsewhere as a finding
- a disagreement that a page has quietly resolved

Lint reports before it repairs. For every issue: the page, the problem, the evidence, the proposed fix. In the judgement layer, the evidence is the paper itself: before proposing a repair, open the extracted markdown under `sources/` and check the claim against it, and say which passage was checked. A wiki source page is agent output and is not evidence of what the paper says. Mechanical issues may be fixed in the same run. Judgement issues are fixed only after the maintainer confirms which page is wrong, because a confident repair in the wrong direction is worse than the original error.

## 6. Style

Plain English, short paragraphs, UK spelling. No em dashes. A concept page's title may be a question, since that is how a topic is best framed; sub-headings on every page are noun phrases or short sentences. Write for a reader who has not read the papers. Do not pad, do not editorialise, and do not describe the wiki's own process on its pages; that belongs in the log.
