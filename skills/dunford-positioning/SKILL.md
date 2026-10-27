---
name: dunford-positioning
description: "Conduct an interactive April Dunford positioning exercise, from scope and customer evidence through alternatives, differentiation, value, best-fit customers, category, challenge, and activation. Supports internal and outside-in work, with human review between stages. Use to start, continue, or revise a positioning exercise; a quick copy edit or standalone product summary does not require the full workflow."
metadata:
  bundle-version: 0.2.0
---

# Dunford positioning

Help the user make and understand positioning decisions. Follow the stage and review structure in this skill, generalised to the actual product and customers. Keep Dunford's causal sequence: alternatives → relative capabilities → value → who cares most → category.

This workflow encodes a practitioner's methodology, refined through repeated hands-on positioning exercises across multiple companies. Its review structure and reasoning controls incorporate lessons from those exercises, rejected approaches and retrospectives.

## Start or resume

1. Establish the positioning object, intended use, existing work, evidence access, and review authority. Use supplied context before asking questions. Distinguish customer positioning from investor and partner-recruitment arguments.
2. Use **internal** mode when the operator has company access; use **outside-in** mode for external analysis. Access is not proof: record what is actually available. Internal runs can still lack customer or deal evidence; outside-in runs may have directly supplied company material. See [reasoning.md](references/reasoning.md#evidence-and-access).
3. Reuse the host's suitable positioning workspace. Otherwise create a small `positioning/` folder in the requested company workspace; a vault manifest, knowledge graph, special browser, or custom server is not a prerequisite. If the current workspace is just the method library, ask for the subject/output location before creating company work there. Never overwrite an existing run or import another company's answers.
4. For a new run, create only a run index and the current stage packet. Record the stage sequence, scope/mode, source locations, review decisions, and next action in the index. Create later packets as needed. Use existing evidence ledgers; create a sources file only if none exists. Keep sourced company evidence in the host's appropriate workstream.
5. To resume, read the index, the active packet, and the approved inputs it depends on. Stage packets govern status and evidence permissions; the host's decision log governs durable choices. Resolve material conflicts before progressing. Never reconstruct approval from polished copy or a previous assistant's assertion.
6. Read [reasoning.md](references/reasoning.md) at run entry, then the relevant section of [stages.md](references/stages.md) before each stage. Read only the evidence needed for the active decision. These references are self-contained; no access to the original project files is required.

## Sequence

These are **this skill's workflow stage numbers**, not a claim that Dunford's book has thirteen steps. Do not introduce a second phase-numbering system during a run.

| Stage | Decision |
|---|---|
| 0 | Scope, evidence access, participants, and exercise contract |
| 1 | Reference customers or explicitly bounded public customer circumstances |
| 2 | Vocabulary and positioning baggage |
| 3 | Competitive alternatives |
| 4 | Strategic differentiation |
| 5 | Differentiated value and proof |
| 6 | Best-fit customers and champions |
| 7 | Market category and winning style |
| 8 | Trend and point of view, including a decision to omit them |
| 9 | Assemble the positioning system |
| 10 | Challenge and test |
| 11 | Select and plan operating artifacts |
| 11A | Primary sales narrative |
| 11B | Additional audience adaptation, when needed |
| 11C | Website message architecture |
| 11D | Qualification, proof, and content requirements |
| 12 | Validation, ownership, and maintenance |

## Review contract

**Run one review unit, present its complete packet, and stop.** Never self-approve or begin the next stage while a decision is pending. This includes Stages 3–7 individually and each selected Stage 11 artifact. Approval of this skill, a plan, or the whole exercise is not approval of future analytical findings.

Each packet contains:

- Proposed answer and intelligible reasoning, followed by source/evidence handles.
- Accepted upstream inputs and the disposition of each material candidate: retained, conditional, branched, rejected, or reopened. Preserve conditions without copying the entire prior packet.
- Strongest materially different counter-reading and what would change the answer.
- Claims rejected or downgraded, material unknowns, and exact downstream permissions and limits.
- A concrete requested decision, with consequences for the next stage.

Lead the conversation with the recommendation, rationale, strongest objection, and decisions needed. Keep the detailed reasoning reviewable in the packet. A packet is not complete merely because it contains the required headings.

The user may **Approve**, **Revise**, **Reopen**, or **Branch**. Accept clear equivalent language. Approval permits use at the stated evidence level; it does not validate customer truth. A proposed **Skip** needs an explicit decision and a recorded consequence/reopening condition. Never inherit another exercise's historical skips or approvals. Later broad continuation instructions do not silently waive this review contract; the user must explicitly change it.

After an actual decision, update the authoritative packet and index, and the host decision log when its rules require it. Mark retained review requests and gate text as historical where they appear; keep standalone summaries' status and next action current so they do not request an already completed review. If a premise changes, identify affected downstream packets and mark them for revision; do not keep treating their approvals as current. Keep valid evidence separate from superseded conclusions. Resume without repeating unchanged approved work.

## Research and human participation

Use the existing company/product/buyer/competitor record first. Obtain enough neutral subject understanding to scope the exercise before selecting a segment, value theme, or category. Do not demand an exhaustive company-research project as a default entrance fee.

When a gap could change a decision, state the question, the evidence required, and the consequence of leaving it unknown. Use already-authorised public research proportionately, make new evidence visible in its owning ledger, and return to the same stage. Propose a bounded research round before expanding the assignment. Ask for unavailable private inputs when material; do not fabricate them or treat an interview guide as completed research. A source that fails must not silently terminate its analytical function: seek another appropriate source or record the unresolved question.

In internal mode, involve the accountable business owner and relevant product, sales, marketing, and customer-success holders of evidence. The LLM facilitates; it does not impersonate their participation or decisions. No outreach, interviews, private-data upload, publication, or deployment is implied by running this skill.

Outside-in, public cases are not an ecstatic-customer cohort, public vendor availability is not an observed shortlist, and founder intent is not customer preference. Recommend a strategy when warranted, with its hypotheses and rivals intact. Do not claim company validation.

## Output and finish

At Stage 9 produce an understandable detailed positioning document, a dependency canvas, and a one-page internal summary. Each canvas chain connects a real or explicitly hypothetical alternative, relative capability/system, customer consequence/value, fit condition, and proof/status. Category and optional trend must reconcile with that chain. A slogan is an optional memory aid after the reasoning, never the method.

Stage 10 must receive an explicit review decision before Stage 11 work begins. An explicitly skipped challenge leaves artifacts labelled untested drafts, not validated activation material. Stage 11 plans only artifacts appropriate to the user's purpose; optional units require explicit omission/skip decisions rather than automatic production. Stage 12 identifies remaining tests and owners. Distinguish **analysis approved**, **publication permitted**, **customer-tested**, and **company-adopted**; none implies the others.

Do not build a plugin, runtime validator, multi-agent fleet, resume subsystem, or automatic export mechanism as part of a positioning run. Carry continuity in the ordinary packets and index. Tooling may be added only for a demonstrated task need.

For methodological provenance and example failure cases, consult [lineage.md](references/lineage.md). Historical company conclusions are examples of reasoning failures or corrections, never defaults for a new subject.

## Bundled research coordination

When the companion research-and-analysis skill is available, read
[research handoff and return loop](references/research-loop.md) at entry from
research and before requesting a focused research round. Reuse its existing
evidence and candidate analyses. Return the focused result to the pending decision,
or reopen the earliest invalid upstream stage. Preserve this skill's review
contract. With no companion installed, use the research guidance above.

## Narrative handoff in the three-skill bundle

When narrative-design is selected, pass the current reviewed positioning assembly,
challenge disposition, branches, evidence and use limits into its entry check. An
approved optional trend is a candidate, not proof of a historical change. Record
whether narrative develops the existing 11A artifact or a separate scoped job; keep
one current assembly and avoid duplicate competing narratives. A narrative factual
gap can return to research; a strategic conflict returns to the earliest affected
positioning decision. Neither handoff approves findings or grants public-use rights.
The user may explicitly alter stage review arrangements; otherwise preserve them.
