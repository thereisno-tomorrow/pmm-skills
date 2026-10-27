# How Reasoning for PMM was built

The other skills in this collection started as workflows I ran on companies. This one started as a research question: which methods from intelligence analysis, argumentation, causal inference and decision analysis help an agent reason well about marketing evidence, and which only look rigorous?

## Scoping it through the job

It began narrower, as an investigation of blind spots. I judged that too limited and widened it to reasoning as a whole: building, testing and revising an argument until the conclusion is defensible.

Then I scoped it back through product marketing itself. The PMM role was broken into 130 reasoning-dependent tasks across 26 areas of responsibility, and each task was mapped to the kinds of reasoning it depends on. Three kinds of work came up most: building or assessing a case, diagnosing an outcome, and comparing actions. Those became the skill's three applications, sharing one foundation of evidence rules.

## What went in, and what stayed out

The method choices rest on five research dossiers covering arguments, evidence, diagnosis, decisions and heuristics. From them the skill keeps claim-specific evidence checks, faithful reconstruction of the argument someone actually made, comparison of explanations by the evidence that would separate them, consequence-first decisions, and targeted bias checks.

Some well-known methods stayed out on purpose:

- **Mandatory ACH scoring.** Analysis of Competing Hypotheses is a staple of intelligence tradecraft, but [Mandel, Karvetski and Dhami (2018)](https://sjdm.org/~baron/journal/18/18803/jdm18803.html) found no overall accuracy benefit for it in their task. The skill borrows its idea of structured comparison and leaves out the scores.
- **Fixed thresholds and arbitrary scores.** PMM benchmarks and evidence scores add precision the evidence doesn't have.
- **Human debiasing as a model fix.** Studies of how people respond to bias training don't show that warning a model about a bias has the same effect, so the skill checks for specific distortions where they matter instead of reciting a bias list.

## Making answers easy to follow

Sound reasoning only helps if the reader can follow it. After reviewing and annotating early answers myself, I had the agent research how explanations are written and read. The sources included Gopen and Swan's [The Science of Scientific Writing](https://www.gatsby.ucl.ac.uk/~pel/misc/gopen_swan.pdf) on reader expectations, McNamara and colleagues on text coherence and prior knowledge, [Miller's review](https://konukcan.github.io/explanation-course/papers/miller-2019-explanation-in-ai.pdf) of how people explain things to each other, studies of jargon and comprehension by Bullock, Shulman and colleagues, the CDC's clear-communication guidance, and Scharrer and colleagues on how easy-to-read texts affect readers' confidence.

The main lesson was that the usual failure is a disconnected explanation: a technical term announced, defined, and left for the reader to connect to the decision. Short sentences and definitions alone don't fix that. The skill's explanation rules follow from it:

- Lead with the answer and the condition that controls it.
- Start from the concrete issue the reader already understands, then bring in the concept that explains it.
- Name the concept for what it is (a principle, a method, a bias), define it once in plain words, and show why it matters here. Explain it again when asked, not every turn.
- Use bullets for parallel examples, and leave out jargon piles, reflexive criticism and empty caveats.

Three of these came straight from my annotations: define a concept the first time it appears, say what kind of concept it is, and put the concrete point before the abstraction.

## How it grew

The skill reached its current form over four versions. The early versions set out the shared rules and the first method cards. Version 0.3.0 added evidence reconstruction, an update record that carries corrections through a conversation, and a final check on the consequential claims in each answer. Version 0.4.0 added two cards: discriminating diagnosis, built on [Klayman and Ha's](https://pages.ucsd.edu/~mckenzie/KlaymanHaPsychReview1987.pdf) distinction between positive testing and biased confirmation, and intervention comparison, adapted from the design ideas in [Hernán and Robins' *Causal Inference: What If*](https://miguelhernan.org/whatifbook).

The full source list, with the critiques that shaped each choice, is in the [method lineage](../../skills/reasoning/references/lineage.md).

I set the scope, widened it and narrowed it again, set the standard for how answers explain themselves, and decided what the skill keeps. AI agents gathered the research, built the task map to my brief and drafted the files.

[Back to the guide](README.md)
