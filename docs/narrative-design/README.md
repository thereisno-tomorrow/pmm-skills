# Narrative Design

**The strongest product stories start from a real change in the customer's world. This skill finds that change in the evidence and builds the argument from it, one reviewed stage at a time.**

Narrative Design is a skill for AI agents: a folder of instructions your agent reads and follows. It builds a strategic narrative in five stages, one at a time, and stops for your review after each:

1. **Change:** what has shifted in your audience's world, and how we know.
2. **Impact:** what that shift does to their work and decisions.
3. **Adaptation:** a practical method they could adopt, one that works without your product.
4. **Difficulty:** what makes that method hard, and what help they would need.
5. **Solution:** where your product provides that help, described at its true size.

It then assembles a detailed argument and a short version: a storyboard or a message. It is the last step of the [three-skill workflow](../../WORKFLOW.md), after [research](../research-and-analysis/README.md) and [positioning](../dunford-positioning/README.md), and it also works alone.

## Where the method comes from

The skill builds on two practitioners. Andy Raskin's strategic narrative, set out in his essay ["The Greatest Sales Deck I've Ever Seen"](https://medium.com/the-mission/the-greatest-sales-deck-ive-ever-seen-4f4ef3391ba0), opens a story with a big change in the buyer's world rather than with the product, then shows who wins and who loses as that change plays out. Marcus Andrews developed that thinking into Narrative Design, crediting Raskin and HubSpot's Brian Halligan as the people who taught him most about it ([2020 article](https://marcusandrews.substack.com/p/why-narrative-design-will-replace), [2022 interview](https://www.launchnotes.com/blog/narrative-design-with-pendos-director-of-product-marketing-marcus-andrews)).

This skill organises their reasoning into five reviewed stages. The review rules and safeguards are my own implementation. It is independent work, not an official course or an endorsed version ([attribution](../../ATTRIBUTION.md)).

## When to use it

Use it after positioning, or any equivalent direction that says who the audience is, what the alternatives are and what the product can do. A focused repair updates only the affected stages. A storyboard comes as written claims and transitions, ready for whoever designs the slides.

## What you get

A write-up per stage (the recommendation, the reasoning, the strongest objection and the decision it needs), then the detailed argument and the short version. The finished work names its weakest premise and a small audience test that would confirm or overturn it, and it is labelled for what it is: a reviewed draft, a provisional hypothesis, or a deliberately reframed argument.

## Try it

Copy the whole `skills/narrative-design` folder into the skills directory your agent reads (for example `.claude/skills/` or `.agents/skills/`), then ask:

```text
Use the narrative-design skill to develop a narrative for [product] and [audience].
The positioning is in [file]. Go one stage at a time and stop for my review. I want a
detailed argument and a one-paragraph message at the end.
```

**Illustrative example**, from [`references/examples.md`](../../skills/narrative-design/references/examples.md). The plant and the product, ShiftLedger, are fictional. The plant moved from one shift to three and logged duplicate inspections and jobs with no incoming owner. The product records jobs, owners and acknowledgment but can't diagnose equipment. Paper handover books long predate it.

> **Change:** No industry trend is established. Retain the local operational change. [...]
>
> **Adaptation:** Manage transfer of responsibility, rather than merely leaving notes. [...] The product is unnecessary for understanding or beginning this method.
>
> **Solution:** A pilot could favor paper logs or a staffing change instead. Product fit remains conditional.
>
> **Faithful short message:** "Keep unresolved maintenance work and its next owner visible across shifts. ShiftLedger records jobs, ownership and acknowledgment. Test it at one shift boundary against your current process."

The story rests on the plant's own change, gives the plant a method it could start on paper today, and ends with a fair test against its current process. Every line is backed by the evidence given.

## Design decisions

- **A "why now" grounded in evidence.** The Change stage builds on a shift the evidence supports. When the real change is local, as with the plant's move to three shifts, the skill tells a focused story about the audience's own situation, or asks for the evidence a wider claim would need.
- **Precise about what is new.** The Change stage looks for an old, credible instance of any shift it proposes. That keeps the story exact about what has moved: often scale, cost or adoption rather than the idea itself.
- **A method the audience can use.** The Adaptation stage describes a way of working the audience could start with or without the product. Take the product name out and the method still makes sense. That is what makes the narrative valuable to the buyer, and what earns the product its place in it.
- **The product at its true size.** The Solution stage shows where the product helps and where the customer will still need other help. Real difficulties stay in the story, and the offer is described as it is. A narrative that is clear about its edges is one a skeptical buyer can believe.
- **Revise from the point of change.** When an upstream fact changes, the skill finds the earliest stage it affects, updates from there, and keeps one current version of the argument. It can also ask research for a single missing fact without restarting the study.

## Using the output

The scenes in a narrative illustrate the argument; customer proof comes from real customers. The finished argument is a reviewed draft, ready to put in front of real audiences, and publishing it stays your call.

## Read more

- [`SKILL.md`](../../skills/narrative-design/SKILL.md): the instructions the agent follows.
- [How it was built](how-it-was-built.md): the narrative workflow behind the skill and the calls that shaped it.
- [MIT license](../../LICENSE), copyright 2026 Nicholas Woo.
