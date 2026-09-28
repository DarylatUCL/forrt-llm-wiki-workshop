# Resources

Links checked on 28 September 2026. Inclusion is not endorsement; apart from the first two tools below, none of these was used in the workshop.

## The idea

- [Andrej Karpathy, "LLM Wiki"](https://gist.github.com/karpathy/442a6bf555914893e9891c11519de94f) (April 2026). The one-page description of the pattern. It is written to be handed to an agent: paste it, say what your wiki is for, and the agent builds a skeleton.
- ["LLM Wiki v2"](https://gist.github.com/rohitg00/2067ab416f7bbe447c1977edaaa681e2). A community follow-up with lessons from running the pattern.

## What the workshop used

- The Claude desktop app (Code tab) as the agent, and Codex as a second agent on the same files. Both need a paid plan or API access.
- [Obsidian](https://obsidian.md), free, as the viewer. It is optional: the wiki is a folder of plain text files and opens in any editor.

## A gentle walkthrough

- [Teacher's Tech, "Karpathy's LLM Wiki: Full Beginner Setup Guide"](https://youtu.be/iXd0t60YmMw) (YouTube, April 2026). A step-by-step setup on a non-academic example.

## Where the pattern leads

- [Open Knowledge Format](https://github.com/GoogleCloudPlatform/open-knowledge-format). A format standard for sharing wikis of this kind between agents. The frontmatter fields in this repository's schema (`status`, `generated`, `verified`) borrow their shape from it; the wiki here is not a conformant bundle.
- [qmd](https://github.com/tobi/qmd). Local search over markdown files, for when a wiki outgrows its index.
- [claude-obsidian](https://github.com/AgriciDaniel/claude-obsidian), [llmwiki](https://github.com/lucasastorian/llmwiki), [second-brain](https://github.com/NicholasSpisak/second-brain). Ready-made implementations with more automation.

## Costs and models

Prices and model line-ups change monthly, so none are given here. Three things hold regardless. First, an ingest is a few minutes of agent time per paper, which is modest on a subscription. Second, smaller models are faster and cheaper but follow the schema less reliably; in building this vault, the cheapest model tried finished first and broke the schema on a concept page. That is one run, an anecdote and not a comparison. Third, with a cloud model the provider sees the paper text and every page written, so for unpublished work, paywalled papers or participant data, check your provider's retention terms and your institution's guidance before you start.

## The sceptics

Two common objections, both fair: that an AI-curated wiki is not sustainable to maintain, and that errors compound until the wiki collapses. The honest answer is that the wiki stays sound only while the agent does the maintenance and the researcher keeps reading what matters. The lint step slows drift; only reading stops it.
