# How Grounded Skeptical Agents was built

This skill started with simulated readers for a crypto media product. AI agents built a panel of readers to react to the product before real people did.

I noticed the panel didn't match the real world. Crypto participants are jaded and skeptical: they have seen many products like this one and distrust most of them. The simulated readers were trusting newcomers who needed the offer far too conveniently. That gap inspired this skill. If simulated audiences can drift that far from real ones in crypto, any product marketing review that relies on them needs the same grounding.

## The correction at its core

I had the personas checked for naivety and told the agent to ground itself first in how jaded and watchful crypto participants really are, then rebuild the personas and check them against that. The rebuilt audience described what readers already knew, the trigger that might bring them to a new source, the workaround they used today, the compromise they would accept, the marginal value on offer, and the condition under which they would walk away.

That correction became the skill's shared grounding, and its first instruction: "audit whether the imagined audience conveniently needs the offer."

## What else carried over

- **Expert and skeptical can coexist with yes.** Experienced buyers can be wary and still knowingly accept a risk. Skepticism is a judgment, not a default no.
- **Alternatives are not all competitors.** Existing sources the audience trusts can be collaborators as easily as rivals, and the market is never assumed to be empty.
- **Observation stays apart from inference.** A public thesis or a follower graph says something about attention, not about what an audience will pay for.

## From one review to four

The grounding became the shared core, and four review procedures were written around it for four recurring audience decisions in product marketing: whether a buyer should switch, how a champion can make the internal case, whether a page or pitch earns its next step, and which claims survive a move to a new segment. Each has its own reference file, and the agent reads only the one a request needs.

The reason to package it as a skill is reuse. The method is easy to state once and easy to forget the next time; as a skill, it can be called by name and applied the same way on every review, without rewriting a long prompt or organising a panel of agents.

I made the correction above, set the scope of the four reviews, and decided what the skill keeps. AI agents built the simulated audiences and drafted the files.

[Back to the guide](README.md)
