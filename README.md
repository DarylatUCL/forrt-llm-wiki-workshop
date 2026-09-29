# Keep the reading, delegate the bookkeeping

Materials for the workshop "Keep the reading, delegate the bookkeeping: an AI-maintained wiki for your literature", FORRT AI in Metascience Conference, 30 September 2026. Facilitators: Daryl Y. H. Lee and Tao Ma (University College London). The materials in this repository were prepared by Daryl Y. H. Lee, who is responsible for any errors in them.

The workshop shows a personal wiki over a body of research literature, written and maintained by an AI agent and checked by the researcher. The pattern is Andrej Karpathy's "LLM Wiki" ([his one-page description](https://gist.github.com/karpathy/442a6bf555914893e9891c11519de94f)). What this repository adds is a schema written for research use: claims trace to papers, the researcher's own judgement is recorded apart from the summaries, disagreements between papers are shown and not settled, and the checking step reports before it repairs.

No programming is needed. You need an agentic coding tool (the workshop uses the Claude desktop app; Codex works with the same files) and, optionally, [Obsidian](https://obsidian.md) to read the pages.

## What is in this repository

| Folder or file | What it is |
|---|---|
| `demo-vault/` | The wiki as it stands at the start of the demo: eleven papers ingested, one waiting to be ingested, one error planted on purpose. Open this to follow along. |
| `demo-vault-after/` | The wiki pages after all the demo steps were run once (28 September 2026), planted error repaired, otherwise as the agent wrote them. For reading and comparing; it holds no papers. |
| `starter/` | An empty wiki with the same schema, for building your own. |
| `prompts.md` | Every prompt used in the demo, ready to paste. |
| `CHANGES.md` | What each demo step changed, in plain words. |
| `resources.md` | Links: the original idea, tutorials and tools. |
| `ATTRIBUTION.md` | The fifteen papers, their authors and licences. |
| `LICENSE.md` | Licence for the materials. |

To get everything, use the green **Code** button on GitHub and choose **Download ZIP**, then unzip.

## Follow the demo

1. Unzip anywhere, for example your desktop. Do not put it inside a folder that already has its own `CLAUDE.md` or `AGENTS.md`.
2. Open your agent on the `demo-vault` folder.
   - Claude desktop app: Code tab, set the folder to `demo-vault`. The workshop uses Opus 5.5, effort Low, permission mode Auto.
   - Codex: open `demo-vault` as the workspace and accept the prompt to trust the folder. It reads `AGENTS.md`, which is identical to `CLAUDE.md`.
3. Optionally open `demo-vault` in Obsidian as a vault, to watch pages change.
4. Paste the prompts from `prompts.md`, one at a time, in one session. The ingest takes about four minutes, the lint about three, the others about a minute.

Three papers in `demo-vault/sources/` are deliberately not ingested (Bartoš et al. 2023, Nissen et al. 2016, Munafò et al. 2017). Try an ingest of your own on one of them with the same prompt.

## Start your own

Two routes.

1. **From the starter.** Copy `starter/` somewhere, rename it, and open `CLAUDE.md`. Replace the bracket in the first paragraph with one line saying what your wiki is for, then copy `CLAUDE.md` over `AGENTS.md` so the two stay identical. Put each paper in its own folder under `sources/`, then run the ingest prompt on it. `starter/README.md` has the details.
2. **From Karpathy's page.** Tell your agent: "Read Karpathy's LLM Wiki gist at https://gist.github.com/karpathy/442a6bf555914893e9891c11519de94f, then set up a wiki for my reading on [your topic]." It builds a skeleton and a schema of its own. You will not get the research-specific rules that way; sections 3 to 5 of `starter/CLAUDE.md` are where to find them.

## The planted error

One error was planted on purpose in `demo-vault/wiki/concepts/text-mined-p-values.md`. The page says Hartgerink's reanalysis found a proportion of .583 in Results sections, with a surplus of p-values just below .05. The paper's Table 1 gives .417 and no surplus. The lint step should report it and wait for your confirmation before repairing it.

## How far to trust these pages

Every wiki page here is agent output, and every page is marked `status: draft`. No page has been verified by a human against its paper, so none is marked `stable`.

What has been done:

- A second model (Codex) read every page against the papers on 4 September 2026 and reported ten errors. Each was checked against the paper and corrected.
- Three lint runs by the agent itself (24 and 28 September) reported seventeen further errors in the starting pages. Each was checked against the paper and corrected. The three runs found largely different errors, and two of their reports were wrong.
- The checking and correcting was done by AI assistants under the maintainer's direction. `wiki/log.md` records every correction.

So the pages have been inspected and repaired, repeatedly, by models. That is not verification. Further errors are likely, and `demo-vault-after/wiki/log.md` lists the ones the agent found in its own fresh output. Treat the vault as a worked example of the method, not as a reference on metascience. For anything you would cite, read the paper.

The page in `wiki/judgements/` records the lead facilitator's own view on one published dispute. It is his opinion, labelled as such, and is there to show how a judgement is kept apart from summaries.

## Licence and credit

The wiki pages, schema, prompts and documentation are released under CC BY 4.0; see `LICENSE.md`. The papers in `demo-vault/sources/` belong to their authors and are redistributed under their own licences (fourteen CC BY 4.0, one CC0 1.0); see `ATTRIBUTION.md`. The pattern is Andrej Karpathy's.

Questions: open an issue on this repository.
