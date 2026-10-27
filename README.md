# PMM Skills

**Six skills that bring a product marketer's discipline to AI agents: evidence first, one reviewed decision at a time, and a clear line between what is known and what is assumed.**

Six skills for product marketing work with AI agents. A skill is a folder of instructions an agent reads and follows. Three of these form a sequence from company research to positioning to narrative. The other three are standalone tools: one for reasoning through evidence, one for mapping a category's debates, and one for reviewing messaging against what an audience actually thinks.

## The skills

| Skill | What it's for | Docs |
|---|---|---|
| **Research and Analysis** (`research-and-analysis`) | Works out how a company's product works, who buys it and why, what the alternatives are, what a rival would find hard to copy, and how the company markets today. Each pass names what it still doesn't know, and later passes close those gaps. | [Guide](docs/research-and-analysis/README.md) · [How it was built](docs/research-and-analysis/how-it-was-built.md) |
| **Dunford Positioning** (`dunford-positioning`) | Runs a positioning exercise in April Dunford's order (alternatives, differentiation, value, best-fit customers, then category) and stops for your decision after each stage. | [Guide](docs/dunford-positioning/README.md) · [How it was built](docs/dunford-positioning/how-it-was-built.md) |
| **Narrative Design** (`narrative-design`) | Builds a strategic narrative from reviewed positioning: what changed for the audience, what it means for them, what they can do about it, what stands in the way, and where the product helps. Delivers a detailed argument and a short version. | [Guide](docs/narrative-design/README.md) · [How it was built](docs/narrative-design/how-it-was-built.md) |
| **Reasoning for PMM** (`reasoning`) | Checks whether research supports a claim, explains why a commercial outcome happened, or compares possible actions against a stated objective. | [Guide](docs/reasoning/README.md) · [How it was built](docs/reasoning/how-it-was-built.md) |
| **Category Arguments & Founder Perspectives** (`category-arguments`) | Maps what people in a category disagree about and how each founder thinks, with every point linked to its public source. Includes a helper for collecting X posts with their context. | [Guide](docs/category-arguments/README.md) · [How it was built](docs/category-arguments/how-it-was-built.md) |
| **Grounded Skeptical Agents** (`grounded-skeptical-agents`) | Reviews a switching decision, a champion's internal case, a landing page or pitch, or messaging for a new segment, grounded in real audience evidence. | [Guide](docs/grounded-skeptical-agents/README.md) · [How it was built](docs/grounded-skeptical-agents/how-it-was-built.md) |

## How they fit together

**Research → Positioning → Narrative.** Research findings enter positioning as evidence and candidate ideas, never as decisions already made. Reviewed positioning then sets the narrative's audience, alternatives, value and limits. Work can also flow back: if the narrative needs a fact nobody has checked, it asks research for that one fact, and if a positioning premise turns out to be wrong, the affected decision reopens and everything built on it is updated. [WORKFLOW.md](WORKFLOW.md) describes the hand-offs. Each of the three also works alone.

The standalone tools fit wherever they help. Use Category Arguments before positioning in an unfamiliar market or before a founder interview. Use Reasoning when a claim, a diagnosis or a decision needs testing. Use Grounded Skeptical Agents before a page, a pitch or a move into a new segment goes out.

## What they have in common

- **One decision, then stop.** The workflow skills present one decision with its reasoning and the strongest objection, then wait for you. They never approve their own work.
- **Evidence keeps its label.** An observation, a vendor's claim, a calculation and an inference stay separate, and each conclusion carries the strength of what supports it.
- **Found is not working.** An analytics tag on a page shows that a tag exists. It doesn't show that campaigns run or attribution works. Claims are checked for existence, performance, prevalence and cause separately.
- **Fit is not readiness.** The customers who would gain most may have no budget or project yet. Strategic fit, technical fit, buying readiness and proof readiness are judged on their own terms.
- **A "why now" grounded in evidence.** The narrative builds on a change the evidence supports. When the real change is local, the story focuses on the audience's own situation.
- **Decisions on thin evidence.** When evidence is thin, the skills still make a call: a provisional answer, clearly labelled, with the next check that would firm it up.
- **Skepticism that can say yes.** The reviews look for what would change the judgment, and they recognise proof that is already good enough.

## Install

Copy the folder of each skill you want from `skills/` into the skills directory your agent reads (for example `.claude/skills/` or `.agents/skills/`). Keep `SKILL.md` and its `references/` folder together. Check your agent's documentation for the location and how it finds skills. Then ask by name: "Use the research-and-analysis skill to ...".

The skills need no extra software. The one exception is live X collection in Category Arguments, which needs Python 3.10 or newer and two outside tools listed in [its guide](docs/category-arguments/README.md#x-access).

## What's in this repository

```text
skills/          the six skills, ready to copy into your agent
docs/            a guide and a build note for each skill
WORKFLOW.md      how research, positioning and narrative pass work between them
ATTRIBUTION.md   credits for the frameworks behind the skills
```

## Credits and license

Dunford Positioning follows April Dunford's positioning sequence, and Narrative Design draws on Andy Raskin's strategic narrative and on Marcus Andrews' Narrative Design, which builds on Raskin's work. Both skills are independent implementations, not endorsed by any of these authors. See [ATTRIBUTION.md](ATTRIBUTION.md).

MIT licensed. See [LICENSE](LICENSE). Copyright (c) 2026 Nicholas Woo.
