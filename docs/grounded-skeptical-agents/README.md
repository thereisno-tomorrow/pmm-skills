# Grounded Skeptical Agents

**Simulated customers are most useful when they think like real ones. This skill grounds every simulated reaction in real audience evidence, so a review is as ready to say "go ahead" as "not yet".**

Grounded Skeptical Agents is a skill for AI agents: a folder of instructions your agent reads and follows. It runs evidence-grounded reviews for four specific product marketing situations. Ask for the review you need; the skill picks the right procedure and adapts it to the case, so you don't have to write a long prompt or organise a panel of agents.

Skepticism here is balanced. It recognises proof that is already good enough, compromises buyers knowingly accept, and good reasons to go ahead. Where the gap is a capability, a budget or an approval rather than the message, the review says so plainly, so the team can close it.

## When to use it

### 1. A buyer is deciding whether to switch

**The situation:** a prospect or customer is weighing your product against what they do today: a spreadsheet, an incumbent tool, another supplier, or nothing at all.

**Bring:** your offer and its real limits, how the buyer works today, and any interview or call notes.

**You get:** a clear judgment on whether to stay, defer, try or switch. The strongest case for staying is set against the strongest case for changing, with transition effort, ongoing work, cost and risk counted. Each decisive objection comes with the proof that would answer it, and the review ends with the smallest useful next step, such as a walkthrough or a reversible trial.

> "Here are our offer and interview notes. Would this team have a reason to replace its spreadsheet?"

### 2. A champion has to make the case internally

**The situation:** someone inside the buyer's company is taking your product to an internal decision, such as a requirements review, a pilot approval or a purchase request.

**Bring:** the approval they are seeking, the case they plan to make, and what you know about the people involved: who benefits, who pays, who implements and who signs off.

**You get:** a readiness judgment, the stakeholders' concerns in priority order with a truthful, evidence-backed answer to each, and a check of every commitment in the case (savings, dates, staff effort, systems replaced) against what the evidence supports. It also recommends the right size of ask for where the deal stands, from clarifying requirements to a bounded pilot or a purchase.

> "Help our champion prepare for this pilot approval meeting. Here are the finance and IT notes."

### 3. A landing page or sales pitch is about to go out

**The situation:** you have a page, a deck or a call script, and a specific next action you want the audience to take, such as booking a demo.

**Bring:** the copy or script, the audience, the channel and the action it asks for, plus whatever audience evidence you have.

**You get:** a judgment on whether the message earns that action, and a few prioritised findings tied to exact lines. Each finding is diagnosed as a communication issue (the value is there but obscured), an evidence issue (the claim outruns the proof) or a product-fit issue (the offer doesn't meet the requirement), with the smallest fix for each. You also get what to keep, and replacement lines where the real capability and proof support them.

> "Review this landing page for the buyers in these interviews. The next step is a ten-minute demo."

### 4. A message is moving to a new segment

**The situation:** messaging that works for one audience is being taken to another, for example from small agencies to regional firms.

**Bring:** the original message and who it was written for, evidence about the new audience, and the product's actual capabilities.

**You get:** a claim-by-claim decision: keep it, change its emphasis or wording, hold it until there is evidence, or flag a product applicability gap. Adapted copy comes where it is justified, along with the questions for real buyers in the new segment that would confirm the adaptation.

> "Adapt this message from small agencies to regional firms using these workflow interviews."

**Across all four:** rough notes are fine as evidence, and source labels help keep the review traceable. The skill asks only about gaps that would change the answer. Reviews can be combined, such as checking a pitch and then preparing the champion for the internal meeting that follows. To choose a segment or build positioning from scratch, use [Dunford Positioning](../dunford-positioning/README.md).

**No audience evidence yet?** Gather it first. [Category Arguments](../category-arguments/README.md) maps what an audience says in public, with every point linked to its source, and the buyer pass in [Research and Analysis](../research-and-analysis/README.md) works out who buys, what triggers the purchase and who signs off. Bring what they find into the review.

## Design decisions

- **Audit the convenient audience.** Before any reaction is simulated, the skill checks whether the imagined audience conveniently needs the offer. Real buyers have workarounds they value, alternatives they trust, and reasons to say no.
- **Label what you know.** Observations, self-reports, vendor claims, demonstrated capabilities and inferred reactions stay separate. Conflicting roles and segments stay visible rather than being blended into a consensus.
- **Trace every reaction.** Each material reaction runs from the audience's circumstance, through the specific claim or proof, to what it means for the decision, and says what evidence would change it.
- **Delivered value only.** Roadmap promises and narrow demos are kept apart from capabilities the buyer can rely on today, and suggested copy stays within real capability and proof.
- **End with a real-world check.** Every review closes with the smallest next step and what it would resolve. Simulated reactions generate hypotheses to check with real buyers; demand, willingness to pay and fit are settled by people.

## Install

Copy the complete `skills/grounded-skeptical-agents/` folder into the skills directory your agent reads (for example `.claude/skills/` or `.agents/skills/`). Keep `SKILL.md` and `references/` together. Check your agent's documentation for the exact location and how it discovers skills.

```text
Use the grounded-skeptical-agents skill to review this pitch for the attached audience evidence.
```

Once your agent has discovered the skill, ordinary requests like the examples above can select it from its description. Ask for it by name whenever you want this method specifically.

The skill needs only a text-capable agent that can read its reference files. You supply the evidence; there are no scripts, network calls, accounts or sub-agents.

## Read more

- [`SKILL.md`](../../skills/grounded-skeptical-agents/SKILL.md) and the four procedures: [switching review](../../skills/grounded-skeptical-agents/references/switching-review.md), [champion preparation](../../skills/grounded-skeptical-agents/references/champion-preparation.md), [message review](../../skills/grounded-skeptical-agents/references/message-review.md) and [new-segment messaging](../../skills/grounded-skeptical-agents/references/new-segment-messaging.md).
- [How it was built](how-it-was-built.md): the audience simulation it came from and the correction at its core.
- [MIT license](../../LICENSE), copyright 2026 Nicholas Woo.
