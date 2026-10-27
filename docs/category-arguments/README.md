# Category Arguments & Founder Perspectives

**Before you decide what to say in a category, you need to know what the people in it are already arguing about, and what each founder actually thinks. This skill maps those arguments from public sources, with every interpretation linked back to what was said.**

Category Arguments & Founder Perspectives is a skill for AI agents: a folder of instructions your agent reads and follows. It researches public conversations, reconstructs the arguments behind them, and produces source-linked category maps and founder briefs. It includes a helper that collects X posts with their parent and quoted posts, so a reply is never read without what it replied to.

## When to use it

- Get oriented in an unfamiliar category before positioning or narrative work.
- Prepare for a founder interview or a new client engagement.
- Develop thought leadership grounded in a founder's actual reasoning.
- Revisit a category map after a significant event or a new statement.

Start from the category, from particular founders, or both. Use live public research or material you already have.

## What you get

- **Category argument map.** The substantive questions, the competing positions, who holds them, the strongest reasoning on each side, shared ground, and the evidence behind each argument.
- **Founder perspective briefs.** Each person's positions, distinctive contributions, recurring explanations, standards of evidence, qualifications and changes over time.
- **Research handoff.** A navigable evidence collection, implications for the original brief, open questions, and the assumptions behind proposed next steps.

Sources stay connected to the analysis. Founder evidence can correct the category map, and full conversations stay available behind short excerpts.

## How it works

1. **Establish the brief:** company, working category, people, purpose and evidence boundary.
2. **Collect and organise:** search company, founder, reply, competitor and wider-category sources; recover each post's context; keep the source records.
3. **Map the arguments:** what participants claim, why they disagree, and where they share ground.
4. **Develop founder perspectives:** each person's thinking and distinctive contribution across their statements.
5. **Check and hand off:** verify the interpretations that drive conclusions, compare the two analyses, correct errors, and connect the findings to the next task.

Collection also follows relevant interviews, talks, essays and documentation; X is one source, not the boundary. The map grows from the evidence rather than from a preset number of arguments or camps.

## Try it

Copy the complete [`skills/category-arguments`](../../skills/category-arguments/SKILL.md) folder into the skills directory your agent reads (for example `.claude/skills/` or `.agents/skills/`), keeping its references and scripts. Then:

```text
Use the category-arguments skill to research [company] in [category], focusing on
[founder names]. The research should inform [an interview, positioning work,
or a thought-leadership brief]. Cover [date range] and use public sources.
Start by establishing the research brief.
```

For a guided run, add: "Work with me stage by stage: brief, collection, category arguments, founder perspectives, and handoff. Pause for my review between stages." To work from material you already have, say "Use only these sources." To update an earlier map, supply the new statements and ask what changed and which interpretations need revision.

## Design decisions

- **Context before attribution.** A reply is read with its parent and any quoted post before anyone decides what its author believes.
- **Separate axes stay separate.** "Publish specifications openly" and "validate every release" are two positions on two questions, not opposing camps. The skill won't force independent issues into one pro/anti line.
- **Silence is not a position.** "Pricing position not observed in the collected window" is the finding, not "the founder avoids pricing". A failed search is not an empty conversation.
- **People are not their company.** Each founder gets their own brief and their own attribution. Related technical comments don't automatically add up to a broad thesis someone never stated.
- **Loud is not common.** A position found in a few posts is not a measured share of the market. The map reports who said what, not how widespread a view is.

## X access

Live X collection needs **Python 3.10 or newer**, an authenticated **Grok CLI with X search**, and network access to the FxTwitter mirror. Grok finds candidate posts; the mirror supplies the verbatim text used as evidence. Analysis of an existing corpus needs none of this.

The helper finds Grok through `--grok`, `GROK_BIN`, your PATH, or the current user's `.grok/bin/grok.exe`, and reuses the CLI's existing sign-in. From the installed skill folder:

```text
python scripts/x_access.py doctor
python scripts/x_access.py search --query "[public search terms]" --lane category --since 2026-01-01 --until 2026-10-27 --limit 10 --out research/x/search-01
python scripts/x_access.py fetch --search-dir research/x/search-01 --depth 3 --max-posts 40 --out research/x/corpus-01
```

Use a new output directory for each run, and keep generated research outside the installed skill folder. Each collection includes full source records, readable pages, the queries that found each post, parent and quote links, and a navigation index. The helper is read-only. It follows a post's parents and quoted posts upward; it doesn't list the replies that came after. See the [X access instructions](../../skills/category-arguments/references/x-access.md) for configuration and every command.

## Package

- [Skill entrypoint](../../skills/category-arguments/SKILL.md)
- [Reading and synthesis](../../skills/category-arguments/references/analysis.md)
- [Evidence notes](../../skills/category-arguments/references/ledger.md)
- [Review and handoff](../../skills/category-arguments/references/review-handoff.md)
- [X access](../../skills/category-arguments/references/x-access.md)
- [Python helper](../../skills/category-arguments/scripts/x_access.py)
- [How it was built](how-it-was-built.md)

[MIT license](../../LICENSE), copyright 2026 Nicholas Woo. The license covers this package's instructions, documentation and code; material retrieved during research stays with its owners.
