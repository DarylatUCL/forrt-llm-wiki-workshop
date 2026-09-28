# Prompts

The exact prompts used to run the three workflows. Each is given verbatim, with the working directory set to the vault root, in a fresh session. The prompt only names the task and the input; the schema does the rest. It is not named in the prompt on purpose: Claude Code loads `CLAUDE.md` and Codex loads `AGENTS.md` from the vault root on their own, and the two files are identical, so the same prompt runs in either tool and the run tests that the tool is reading its own schema file.

## Ingest

```
Follow this vault's schema. Ingest the paper in sources/<folder name> following the Ingest workflow exactly. Report every page you created or modified and what changed in each.
```

## Query

```
Follow this vault's schema. Answer the following question from the wiki, following the Query workflow: <question>
```

## Record a judgement

```
Follow this vault's schema. Record the following judgement in wiki/judgements/ as <slug>, following section 4. Do not change its substance; you may tidy the wording. Verdict: <...> Reason: <...> What would change my mind: <...>
```

## Lint

```
Follow this vault's schema. Run the Lint workflow over the whole wiki. Report every issue before repairing anything, then fix the mechanical issues and stop.
```
