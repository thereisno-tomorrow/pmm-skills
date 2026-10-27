# Reasoning for PMM

**Good marketing calls follow from what the evidence actually shows. This skill has the agent trace the link from evidence to claim before it answers, so a comprehension test is read as comprehension, a stalled deal is diagnosed before it is discounted, and the option with more profit wins over the one with more deals.**

Reasoning for PMM is a skill for AI agents: a folder of instructions your agent reads and follows. It handles three kinds of product marketing question and gives the strongest answer the evidence supports. That can mean keeping a conclusion, narrowing it, changing a recommendation, or leaving a question open with the specific check that would settle it.

| PMM question | What the skill does |
| --- | --- |
| Does our research support this positioning claim? | Separates understanding, preference, differentiation and buying, and finds the missing link without throwing away what the research did show. |
| Why did these opportunities stall? | Compares plausible explanations using evidence that would tell them apart, instead of treating the objection buyers repeat as the cause. |
| Which segment, offer or action should we choose? | Compares feasible options against the owner's objective, with outcomes, periods, costs and constraints on the same footing. |

## How it works

Shared rules apply to every answer: reconstruct the evidence and the argument faithfully, carry corrections through the conversation, and check the consequential claims in the finished answer against their sources. On top of that, five method cards cover specific moves, and the agent reads only the one a question needs:

- **Conditional inference:** what follows from "if A then B", and what doesn't.
- **Absence evidence:** when "no record" can and can't mean "it didn't happen".
- **Assumption sensitivity:** which assumptions the answer rests on, and what happens if they move.
- **Discriminating diagnosis:** looking for evidence that would differ between explanations, rather than evidence that fits the favourite.
- **Intervention comparison:** comparing actions with consistent populations, assignment, denominators and follow-up.

Answers lead with the judgment, then the reasoning, in plain English. How the skill explains is a design choice in its own right, grounded in research on how explanations are written and read (see [how it was built](how-it-was-built.md#making-answers-easy-to-follow)). Routine edits and arithmetic stay routine.

## When to use it

Use it for substantive evidence, causal or trade-off questions: before a claim goes into positioning, before a pricing change is made to fix stalled deals, before a campaign budget is split. Rewording, settled summaries and simple arithmetic don't need it. Formal proofs, specialist statistical estimation, forecasting and optimisation are outside its scope, and a recommendation is input to a decision rather than permission to act on it.

## Try it

Copy the whole [`skills/reasoning`](../../skills/reasoning) folder into the skills directory your agent reads (for example `.claude/skills/` or `.agents/skills/`), keeping `references/` alongside `SKILL.md`. Then include the evidence you want assessed:

```text
Use the reasoning skill to review this positioning recommendation.
What does the research support, and what would change your assessment?
[Paste the recommendation and relevant findings.]
```

```text
Use the reasoning skill to help explain these stalled opportunities.
Here are the buyer comments, approval records and CRM definitions.
Recommend the next useful check before we change pricing.
```

**Illustrative example**, from the [worked examples](examples.md). A team randomly assigned 120 accounts each to current outreach and a new offer. The offer won more deals; the rule is to choose the higher net contribution.

> Choose current outreach under the stated rule. It produced fewer wins but $200 more observed net contribution.
>
> | Sixty-day result | Current outreach | New offer |
> | --- | ---: | ---: |
> | Wins | 10 | 16 |
> | Contribution from wins | 10 × $900 = $9,000 | 16 × $550 = $8,800 |
> | Setup cost | $600 | $600 |
> | Net contribution | **$8,400** | **$8,200** |
>
> This applies the decision method of **incremental analysis**: compare the difference in consequences between the alternatives.

Then Finance corrects the offer's contribution per win to $600:

> Choose the offer. Its corrected result is 16 × $600 − $600 = **$9,000**, compared with **$8,400** for current outreach: a $600 advantage. The recommendation changes because Finance corrected one input, not because the objective or win counts changed.

## Design decisions

- **Explanations a reader can follow.** The answer comes first, with the condition that controls it. A technical concept arrives after the concrete problem it explains: named for what it is (a principle, a method or a bias), defined once in plain words, and tied to this decision. Construct validity, for example, enters only once the reader has seen that understanding a headline and preferring it are different things.
- **Precision the evidence can carry.** Every piece of evidence, probability, score, weight or stakeholder preference in an answer comes from what was provided or found. There is no scoring engine. Options are compared on their actual consequences.
- **Agreement is not verification.** "Self-agreement is not independent verification." The final check on a claim goes back to the original values and units, not to the agent's own draft.
- **Keep what the research did show.** Nine of twelve prospects understanding a headline supports comprehension, not preference. The skill keeps the comprehension finding, drops the preference claim, and names the study that would test preference.
- **Diagnose before prescribing.** "Hard to justify" can mean a budget cap, a missing executive sponsor or a weak business case. Each calls for a different fix, and a price cut solves only one of them.
- **Corrections touch only what they change.** When a fact is corrected, the skill recomputes the affected result and keeps every unaffected finding, instead of restarting the review.
- **Ask for access only when it matters.** Judging an interviewer's question wording needs the questions. Judging whether a summary's conclusion follows from the summary doesn't, so the skill won't demand recordings it doesn't need.

## Requirements

No scripts, packages, API keys or extra services. Your agent needs to read the skill's Markdown files. Supply the claim or question, the relevant evidence and any access limits; for a decision, add the objective and hard constraints where you know them. Checking sources yourself requires whatever source-reading tools your agent already has.

## Read more

- [`SKILL.md`](../../skills/reasoning/SKILL.md): the instructions the agent follows.
- [Worked examples](examples.md): four illustrative cases, including corrections and missing evidence.
- [Method lineage](../../skills/reasoning/references/lineage.md): the research behind each method card.
- [How it was built](how-it-was-built.md): how the skill was scoped and which methods were left out.
- [MIT license](../../LICENSE), copyright 2026 Nicholas Woo. Sources named in the lineage keep their own rights and don't endorse this skill.
