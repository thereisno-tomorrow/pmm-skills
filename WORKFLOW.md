# Research → Positioning → Narrative

Three of the collection's six skills work as a sequence, taking a company from research to reviewed positioning to a strategic narrative. Use all three in sequence, or start at whichever stage your existing work supports.

| Skill | Job |
| --- | --- |
| [research-and-analysis](skills/research-and-analysis/SKILL.md) | Investigate the product, buyers, alternatives, defensibility and marketing; produce a diagnosis, a confidence audit and a research handoff. |
| [dunford-positioning](skills/dunford-positioning/SKILL.md) | Work through alternatives, differentiation, value, best-fit customers and category, one reviewed decision at a time, then plan the materials the positioning needs. |
| [narrative-design](skills/narrative-design/SKILL.md) | Develop Change, Impact, a practical Adaptation, Difficulty and a bounded Solution; assemble a detailed argument and a concise version. |

## How work moves between them

**Research to positioning.** Research findings enter positioning as evidence and candidate ideas, never as pre-approved strategy. The handoff says what is known, what is only a hypothesis, and what to check first.

**Positioning to narrative.** Reviewed positioning supplies the narrative's scope, audience, alternatives, value, branches and the limits on what can be claimed.

**Going back.** Narrative work can ask research for one missing fact without restarting the study. If a strategic premise fails, the earliest affected positioning decision reopens, and everything built on it is updated. Valid work is kept, and there is always one current version. The [research-return protocol](skills/dunford-positioning/references/research-loop.md) and the [narrative continuity guide](skills/narrative-design/references/continuity.md) describe these paths.

**Review stops.** Each skill stops for your review after every stage unless you explicitly change that arrangement. Nothing is approved, published or sent to anyone automatically. Work done from public sources is labelled that way, so it is never mistaken for customer evidence. When the evidence points to a local change rather than a market-wide one, the narrative tells a focused, situation-led story built on it.

## Install and use

Copy the three folders from `skills/` into your agent's skill directory, keeping folder names and `references/` intact. No server, script or API client is needed. Your agent needs file access and whatever research tools you allow it; internal company evidence is optional.

> Use research-and-analysis, dunford-positioning and narrative-design for this
> company. Reuse existing evidence, prepare the research handoff, then develop one
> reviewed positioning or narrative unit at a time. Return to research for a
> consequential factual gap and reopen strategy if a premise changes.

For positioning alone, invoke `dunford-positioning` with the current research. For narrative alone, invoke `narrative-design` with positioning or equivalent direction. These are marketing and strategy methods. They don't do general topic research, render decks or publish campaigns.

## Guides

- [Research and Analysis](docs/research-and-analysis/README.md)
- [Dunford Positioning](docs/dunford-positioning/README.md)
- [Narrative Design](docs/narrative-design/README.md)

MIT licensed ([LICENSE](LICENSE)). Framework credits are in [ATTRIBUTION.md](ATTRIBUTION.md).
