# Research and Analysis

**Positioning is only as strong as the understanding underneath it. This skill builds that understanding pass by pass: each pass names what is still unknown, and the passes that follow close those gaps before anyone writes a position.**

Research and Analysis is a skill for AI agents: a folder of instructions your agent reads and follows. Given a company, it investigates five areas in order: the product, the buyers, the alternatives, what a rival would find hard to copy, and the current marketing. It works from public sources unless you give it internal ones. It is the first step of the [three-skill workflow](../../WORKFLOW.md), followed by [positioning](../dunford-positioning/README.md) and [narrative](../narrative-design/README.md), and it also works alone.

## The problem

Say you must position a company that sells path-planning software for factory robot cells. Its site calls the system "adaptive". A feature list can't tell you whether that means correcting a part's position before a run or reacting during one. It can't tell you what the buyer's engineer must prove before finance signs. A tracking script on the homepage doesn't mean anyone measures anything. Position on top of that and you build on guesses you can't see.

## When to use it

Use it before a positioning exercise, or for one focused question, such as "does this rival really have that integration?" It is built for company research ahead of positioning, so general topic research and standalone buyer studies are better handled elsewhere. It stops at the research summary and contacts no one.

## What you get

- **Five write-ups**, one per area, each ending with "What this pass revealed we don't know" and a route to close each gap.
- **A gap register** that tracks every open question from the pass that raised it to its resolution.
- **A diagnosis** that joins them into one explanation.
- **A confidence audit.** Each important claim is checked four ways: does it exist, does it perform, how common is it, and why does it happen?
- **A research handoff**: the summary for whoever positions next. It lists what is known, what is only a hypothesis, and what to check first.

## The gap loop

The heart of the skill is what happens to the things it doesn't know yet.

1. **Every pass ends with "What this pass revealed we don't know".** Each gap is named with the decision it affects, where the agent has already looked, the next place to look, and the observation that would settle it.
2. **Gaps go into a shared register** with the pass that raised them, so nothing is lost between passes.
3. **Each pass starts from the open gaps.** Before a pass begins, the agent reads the earlier conclusions and the open gap routes, and goes deeper where it can. A product pass that stays at feature level goes back for operational evidence instead of moving on with more citations.
4. **New answers flow back.** When a later finding overturns an earlier premise, the pass it came from reopens, along with everything built on it: parked notes, the diagnosis and the handoff. The live record always holds one current answer.
5. **Every gap ends with a route:** search better, ask someone with access, or record it as not established in what was searched, with the coverage stated.

Before the handoff, a completion check confirms the loop ran: every pass ends with actionable unknowns, and gaps from shallow early passes got follow-up wherever scope allowed. Understanding deepens with each pass instead of stopping at the first plausible answer.

## How it investigates

Each pass has its own investigative moves. A few of them:

- **Break vague verbs apart.** "Adaptive", "autonomous" and "integrated" each hide several possible mechanisms. The skill names the mechanisms and maps each to evidence, version and tier.
- **Do the buyer's arithmetic.** Specifications are converted into the units the buyer cares about, with the calculation shown.
- **Read release notes as evidence of limits.** A fixed defect, a hard ceiling and an undocumented behaviour are different findings, and each gets a date.
- **Compare complete alternatives.** Rivals are compared on the same application, current version and full purchase scope, not feature by feature.
- **Check with a method that can see.** A plain page fetch can miss analytics tags that load after cookie consent, so marketing findings are verified with a method able to observe them.

## Try it

Copy the whole `skills/research-and-analysis` folder into the skills directory your agent reads (for example `.claude/skills/` or `.agents/skills/`), then ask:

```text
Use the research-and-analysis skill to research [company] ahead of a positioning
exercise. Use public sources, reuse anything I've already collected, and start
with the product pass.
```

**Illustrative example**, from [`references/examples.md`](../../skills/research-and-analysis/references/examples.md). ForgeMap is fictional. This is one pass, shortened by quotation.

> **Question:** Can fictional ForgeMap meet a buyer's 0.20 mm complete-system tolerance on a large workpiece, and what does its "adaptive" claim mean?
>
> The documented adaptation handles pose before execution; it does not establish geometry regeneration, force compensation or within-pass feedback.
>
> `0.02 / 100 × 1200 mm = 0.24 mm`. Label this a derived component-linearity bound. It is not resolution, complete-system accuracy or a measured finished-part tolerance.
>
> **Usable verdict:** documented pre-run pose correction, configuration-dependent sensor limits and an unresolved full-system acceptance claim.

In plain words: the sensor's datasheet gives ±0.02% of a 1200 mm range, so its stated error alone (0.24 mm) exceeds the buyer's 0.20 mm. That is a reason to find a whole-system acceptance test, not proof the product fails. The skill keeps those two apart.

## Design decisions

- **Check each claim four ways before handing it on.** A tracking script that exists says nothing about whether attribution works. Existence, performance, prevalence and cause are separate questions with separate evidence.
- **Keep marketing out until the marketing pass.** A product analysis should read like one a product person would write: mechanisms, limits, responsibilities. Marketing ideas that come up early are parked as notes, and the skill won't move on just because it has piled up citations.
- **"No proven difference" is a valid answer.** The skill won't claim a moat the evidence doesn't show, and it won't call a company undifferentiated just because a free tool exists. In one shipped example, architecture alone is not an established moat, but documented configuration work may be a strength whose durability is still open.
- **No trend from numbers that count different things.** Two figures from different populations can look like a decline. The skill computes each quantity on its own terms and refuses the trend.

## Where it stops

The skill works from documents, not conversations. It can say that the reasons deals are won or lost are unknown, and point to where that answer lives (sales records, win/loss interviews). Choosing the positioning, contacting people and running campaigns are separate tasks; the handoff passes the work to them.

## Read more

- [`SKILL.md`](../../skills/research-and-analysis/SKILL.md): the instructions the agent follows.
- [How it was built](how-it-was-built.md): the research workflow behind the skill and the calls that shaped it.
- [MIT license](../../LICENSE), copyright 2026 Nicholas Woo.
