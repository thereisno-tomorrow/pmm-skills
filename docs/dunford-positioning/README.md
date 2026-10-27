# Dunford Positioning

**Good positioning is a chain of decisions, each resting on the one before. This skill runs April Dunford's sequence one stage at a time, shows the evidence and the strongest objection behind each decision, and stops for your call.**

Dunford Positioning is a skill for AI agents: a folder of instructions your agent reads and follows. It runs a positioning exercise in the order April Dunford's framework sets: what customers would do without you, what you do that those options can't, the value that creates, who cares most, and only then the category. The numbered stages (0 to 12), the review after each and the safeguards between them are my implementation. It is an independent implementation, not an official workbook ([attribution](../../ATTRIBUTION.md)). It is the middle step of the [three-skill workflow](../../WORKFLOW.md), after [research](../research-and-analysis/README.md) and before [narrative](../narrative-design/README.md), and it also works alone.

## The problem

Here is one way a positioning exercise goes wrong. The assistant decides your best customer is the one with budget, a project and a test ready to run, because that makes a tidy story. A few steps later "ideal customer" means "ready to buy this quarter", and strong-fit customers who aren't ready yet have dropped out. Nobody chose that. It slid in.

## When to use it

Use it to start, continue or revise a positioning exercise. It has two modes. **Internal mode** is for when you can reach the company's customers and deal records. **Outside-in mode** works from public sources and states what they can and can't establish. It is built for the strategy underneath copy, decks and websites, and it scales to the time you have. The pace is yours: a stop after each stage is the default, and you can explicitly change the review arrangement, for example to review several stages together.

## What you get

A small `positioning/` folder with an index and one write-up per stage. Each write-up (the skill files call it a packet) holds the proposed answer and reasoning, the strongest objection, and the decision it needs. You reply Approve, Revise, Reopen or Branch.

At Stage 9 you get a detailed positioning document, a one-page summary, and a canvas that chains an alternative, the capability that sets you apart, the customer value, the fit and the proof. Stage 10 challenges the result, Stage 11 plans the materials that put it to work (a sales narrative, website message architecture, qualification and proof requirements), each reviewed on its own, and Stage 12 says who must test and own it.

## Try it

Copy the whole `skills/dunford-positioning` folder into the skills directory your agent reads (for example `.claude/skills/` or `.agents/skills/`), then ask:

```text
Use the dunford-positioning skill to start a positioning exercise for [company].
The research is in [folder]. Begin at Stage 0 and stop for my review.
```

**What the first stages produce**, drawn from the [stage guide](../../skills/dunford-positioning/references/stages.md) and the [hard cases](../../skills/dunford-positioning/references/lineage.md#hard-cases):

- **Stage 0** writes the exercise contract: what is being positioned and for what use, what evidence exists, what is out of bounds, and the scope decisions it needs from you. Given only a homepage, it presents Stage 0 and stops rather than generating the whole chain.
- **Stage 1** looks for customer evidence to anchor on. With no actual customers, it proposes a bounded hypothesis or a skip, with the consequence stated. Public logos are not treated as proof of enthusiastic customers.
- **Stages 3 and 4** map the alternatives, separating ones seen in real buying decisions from ones that are merely plausible, then compare complete alternatives rather than feature lists.

## Design decisions

- **One stage, then stop. Never self-approve.** A later broad "keep going" doesn't waive the stop. Approval means "usable at the stated evidence level", not "customer truth checked", so a provisional finding can't quietly harden into a requirement for later stages.
- **Keep four customer questions apart:** strategic fit, technical applicability, opportunity readiness (trigger, budget, approval) and proof readiness. "Best fit" never collapses into "ready to buy now".
- **A narrow claims check can't veto an idea before its value is tested.** Proving claims matters, but a strict proof filter applied too early shrinks a promising position to "only a small number of meaningful differences".
- **Missing customers can't be fixed with stricter desk research.** More proof demanded from public pages won't produce win/loss evidence. The skill carries on with a clearly labelled provisional model and says which judgments depend on it.
- **Keep the inconvenient competitor.** If a rival has a real integration that weakens your preferred differentiator, it stays in the comparison and confidence drops. It is never removed to make the focal product win.
- **Say what "done" means.** Analysis approved, publication permitted, customer-tested and company-adopted are four different states, and every artifact carries the one it has reached.

## Hard cases

The skill ships with a table of [hard cases](../../skills/dunford-positioning/references/lineage.md#hard-cases): situations where positioning work commonly goes wrong, each with the behaviour the skill requires. Examples: a founder's list of target industries is treated as intent, not measured best fit; every feature is matched somewhere but the integrated offer still differs, so the combination is investigated rather than dismissed; a new fact breaks an approved Stage 3 premise while Stage 7 is under way, so Stage 3 reopens and the affected stages are flagged.

## Read more

- [`SKILL.md`](../../skills/dunford-positioning/SKILL.md): the instructions the agent follows.
- [How it was built](how-it-was-built.md): the positioning workflow behind the skill and the rules it earned.
- [MIT license](../../LICENSE), copyright 2026 Nicholas Woo.
