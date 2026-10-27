# How Research and Analysis was built

This skill comes from the research I ran on companies before positioning them. I ran that research with AI agents doing the investigation and drafting, while I directed the work and reviewed the results.

## The workflow behind it

The workflow had five passes: product, buyer, competitor, advantage and marketing. A diagnosis then joined the passes into one explanation, and a confidence audit tested the claims everything else depended on.

The heart of it was the gap loop. Every pass exposed gaps in what the earlier passes had found, and the work went back to close them. Understanding deepened with each pass instead of stopping at the first plausible answer.

I ran it in depth on one company first. That run was the strongest, so I made it the template and reused it on later companies. The instruction for reuse was to follow the method of the first run, not its findings. The skill opens with the same rule: carry over the questioning and corrections from earlier analyses, never their conclusions.

## Calls that shaped it

**Product analysis stays product analysis.** An early product pass drifted into marketing advice and stopped at the feature level. I caught it and set the rule that a product analysis should read like one a product person would write. The skill now parks marketing ideas as notes for the marketing pass and requires a defensible product verdict before moving on.

**A trend needs comparable numbers.** One run turned up two ownership figures, 6.4% and 11.1%, that invited a story of decline. They counted different populations, so no decline was claimed. The skill now identifies exactly what each figure measures before any two are compared.

**"No moat" needs evidence too.** Two decisions from that work sit side by side in the skill. Architecture alone was not treated as a moat. A free alternative existing was not treated as proof there was none either. Both survive in the shipped examples, so the agent learns to hold the question open instead of forcing an answer either way.

**The audit comes before the handoff.** In the original workflow, the confidence audit came after the analysis was finished. In the skill it sits in front of the handoff, so nothing reaches positioning without its strength stated: high, moderate, low or not established, each with its reason.

## From workflow to skill

The skill makes the gap loop explicit. Every pass ends with "What this pass revealed we don't know", open gaps live in a shared register with the pass that raised them, each new pass starts from those gaps, and a failed premise reopens the pass it came from and everything built on it. It also packages the investigative moves from those runs as instructions any agent can follow: breaking vague product claims into mechanisms, converting specifications into the buyer's units, reading release notes as evidence of limits, and comparing complete alternatives rather than feature lists. A later refinement added version-aware reuse of earlier research, verdicts written so the next step can use them directly, and optional sampling controls for when public discussions matter in the buyer pass.

The examples in [`references/examples.md`](../../skills/research-and-analysis/references/examples.md) use fictional companies built to teach those moves.

I chose the template run, drew the line between product and marketing analysis, and decided what the skill keeps. AI agents drafted the files to that design.

[Back to the guide](README.md)
