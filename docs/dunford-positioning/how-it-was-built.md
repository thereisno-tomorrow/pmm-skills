# How Dunford Positioning was built

This skill comes from a positioning workflow I built and ran on multiple companies with AI agents. It follows April Dunford's sequence, with a research protocol and a review after every stage.

## The workflow behind it

Each stage ended the same way. The agent wrote up one decision in full and stopped. I approved, revised, reopened or branched it, and the decision went into a log.

To improve the method itself, I set up a loop. One agent ran a stage of the exercise, and a second agent critiqued it. The lessons were written down as guidelines, the stage ran again under them, and a final review closed the round. For some stages I also had a separate agent look for leaps of logic, blind spots and fallacies before the work came to me.

The most complete run supplied the skill's structure: the Stage 0 to 12 sequence, separate reviews for each of the materials that put the positioning to work, and a habit of reasoning about whole alternatives rather than feature lists. That run also kept a register of what went wrong and a retrospective. Both fed the safeguards.

## Rules the work earned

When lessons moved from one company to the next, one test decided what carried over: a rule stays only if it still makes sense with every company-specific name removed. These are some of the rules that passed.

| What the work showed | The rule now | Where it lives |
|---|---|---|
| A strict check on which claims could be proven passed only a few narrow ones, and the positioning drifted toward "only a small number of meaningful differences". I asked whether the checks themselves had caused the narrowing. | "A narrow claims audit must not veto potentially important hypotheses before value testing." | [`stages.md`](../../skills/dunford-positioning/references/stages.md), Stage 4 |
| Findings approved as provisional started acting as entry conditions for later stages. | Four tests before a premise is reused (removal, permission, rival, fresh warrant), and "Merely repeating a premise, obtaining approval, adding an evidence label, or producing polished copy is not a new warrant." | [`reasoning.md`](../../skills/dunford-positioning/references/reasoning.md) |
| A fixed scope built around one kind of product made the later steps circular. I had the work cleared back to the scaffolding and rebuilt. | "Scope authorises examination. It does not prove a situation is prevalent, urgent, preferred, or commercially primary." | [`reasoning.md`](../../skills/dunford-positioning/references/reasoning.md) |
| High-fit customers were treated as ready-to-buy ones. | Strategic fit, technical applicability, opportunity readiness and proof readiness are assessed separately. | [`stages.md`](../../skills/dunford-positioning/references/stages.md), Stage 6 |
| A product being publicly available was read as customers actively considering it. | "Public availability supports possibility, not frequency or rank." Each alternative must pass: could this customer literally choose this complete route? | [`reasoning.md`](../../skills/dunford-positioning/references/reasoning.md) |
| One pass that demanded more proof from public sources returned no themes at all. | "Missing customer evidence cannot be repaired by stricter desk-research gates." | [`reasoning.md`](../../skills/dunford-positioning/references/reasoning.md) |
| Revised outputs left older versions looking current. | "Mark historical outputs with their governing replacement. Keep a single identifiable current assembly." | [`reasoning.md`](../../skills/dunford-positioning/references/reasoning.md) |

## From workflow to skill

The skill turns that practice into instructions any agent can follow. It works in two modes: internal, for teams with their own customer interviews and deal records, and outside-in, for work from public sources. The lessons from the register appear in generic form as the [hard cases](../../skills/dunford-positioning/references/lineage.md#hard-cases) table.

I designed the review structure, made every approval, skip and reset in the original work, and decided which rules the skill keeps. AI agents built the stage scaffolding from my reference run and drafted the files.

[Back to the guide](README.md)
