# Starter

An empty wiki with the schema used in the workshop. Copy this folder, rename it, and make it yours.

## Before the first paper

1. Open `CLAUDE.md`. In the first paragraph, replace the bracket with one line saying what the wiki is for, for example "questionable research practices" or "the testing effect in education".
2. Read the rest of `CLAUDE.md` once. It is the contract between you and the agent, and everything the agent does follows from it. Change what does not suit you. Section 6 (style) is the part most people adjust.
3. Copy `CLAUDE.md` over `AGENTS.md`, so the two are identical. The Claude app reads the first and Codex reads the second.

## Adding a paper

1. Make a folder under `sources/` named for the paper, for example `sources/Head et al. (2015)/`.
2. Put the PDF in it. The agent works best from a text copy, so ask it, as a separate request before the ingest: "Convert the PDF in sources/Head et al. (2015) to a markdown file in the same folder. Do not summarise; extract the text." After that, nothing in `sources/` is edited again.
3. Add a row for the paper to `corpus.md`.
4. Paste the ingest prompt from `prompts.md`, with the folder name filled in.

The first ingest creates the first few concept pages. Later ingests extend them.

## What the folders are for

| Folder or file | Who writes it | What it holds |
|---|---|---|
| `sources/` | You | The papers. Never edited after they arrive. |
| `wiki/sources/` | The agent | One summary page per paper. |
| `wiki/concepts/` | The agent | One page per topic, drawing on several papers. |
| `wiki/questions/` | The agent | Saved answers to your queries. |
| `wiki/judgements/` | The agent, only at your dictation | Your own views, kept apart from the summaries. |
| `wiki/index.md`, `wiki/log.md` | The agent | The map of the wiki and the record of every run. |
| `corpus.md` | You | The list of papers. |
| `CLAUDE.md`, `AGENTS.md` | You | The schema. |

## Three habits worth keeping

1. **Run lint often, and more than once.** Each run finds a different set of problems.
2. **Read what the lint reports against the paper before you confirm a repair.** The checker is a model too, and it is sometimes wrong.
3. **Mark a page `stable` only after you have checked it yourself.** Until then it is a draft, however good it looks.
