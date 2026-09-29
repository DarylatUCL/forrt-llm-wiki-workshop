# Prompts

The exact prompts used in the workshop demo. Paste them one at a time, in order, in one session, with your agent's folder set to `demo-vault`.

None of the prompts names the schema file. The Claude app loads `CLAUDE.md` and Codex loads `AGENTS.md` from the folder on their own, and the two files are identical.

## Step 1, ingest one new paper

```
Follow this vault's schema. Ingest the paper in sources/Gopalakrishna et al. (2022) following the Ingest workflow exactly. Report every page you created or modified and what changed in each.
```

About four minutes. Expect one new source page and changes to several concept pages. The report at the end lists them, and `wiki/log.md` gains an entry.

## Step 2, a judgement

Nothing to run. Open `wiki/judgements/judgement-p-curve-dispute.md` and read it. It has three parts: the verdict, the reason, and what would change the maintainer's mind.

It was recorded with a prompt of this form:

```
Follow this vault's schema. Record the following judgement in wiki/judgements/ as <slug>, following section 4. Do not change its substance; you may tidy the wording. Verdict: <...> Reason: <...> What would change my mind: <...>
```

## Step 3, the query

```
Follow this vault's schema. Answer the following question from the wiki, following the Query workflow: What do published p-values actually establish about how common p-hacking is, and what do I think follows?
```

About one minute. The answer should give both sides of the published dispute with citations, and give the maintainer's view separately, attributed to the maintainer. It is saved as a page under `wiki/questions/`.

The agent may notice the planted error while reading and offer to repair it. In the workshop the reply is: "Not now, leave it for the lint."

## Step 4, lint

```
Follow this vault's schema. Run the Lint workflow over the whole wiki. Report every issue before repairing anything, then fix the mechanical issues and stop.
```

About three minutes. Expect around ten judgement issues, and a different set each time you run it. In our runs on the demo model (Opus 5.5) the planted error in `text-mined-p-values` was among them each time. In one run on a different model it was missed, so if your lint does not report it, ask about that page directly. One check is a sample, not an audit.

## Step 4b, the repair

After the lint report, in the same session:

```
Repair the text-mined-p-values issue you reported. Check the figure against the paper first, change only that page, and log the repair.
```

About thirty seconds. The page should change from .583 to .417, and the log gains one entry.

## Prompts for your own wiki

```
Follow this vault's schema. Ingest the paper in sources/<folder name> following the Ingest workflow exactly. Report every page you created or modified and what changed in each.
```

```
Follow this vault's schema. Answer the following question from the wiki, following the Query workflow: <question>
```

```
Follow this vault's schema. Run the Lint workflow over the whole wiki. Report every issue before repairing anything, then fix the mechanical issues and stop.
```
