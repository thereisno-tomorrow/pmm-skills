# Worked PMM examples

These are illustrative examples of the behavior the skill is designed for, written for this documentation. The prompts work after installing [the skill](../../skills/reasoning/SKILL.md).

## 1. Assess a positioning claim without discarding the useful finding

**User**

> Use the reasoning skill to review this claim. We recruited twelve prospects to read a headline. Nine could explain its intended meaning. The team says this proves buyers prefer our position and recommends using it everywhere.

**Intended response**

> Nine participants understanding the headline supports a comprehension finding. It does not show that they prefer it to alternatives or would choose the product.
>
> This is the principle of **construct validity**: checking whether the study measured what the conclusion claims. It matters because explaining a headline and preferring a position are different tasks.
>
> Keep the comprehension result. To assess preference, show relevant prospects credible alternatives under comparable conditions, ask which they prefer and why, and preserve how participants were recruited. That would address stated preference; purchasing behavior would still need evidence about actual choices. Do not describe these twelve recruited participants as representing all buyers.

**User correction**

> I misread the report. Nine actually selected our headline over the comparison headline. They were asked which they preferred, not what it meant.

**Intended update**

> That changes the supported finding: nine of twelve recruited prospects preferred our headline in this comparison. Retain that preference result and withdraw the comprehension finding, which the corrected report does not establish. The study still does not establish preference across all buyers or justify using the position in every audience.

The principle need not be defined again. The evidence changed, so the answer changes; there is no reason to preserve the original criticism of a comprehension-only question.

## 2. Diagnose the buying obstacle before choosing a remedy

**User**

> Use the reasoning skill to recommend the next check. Buyers keep saying our product is hard to justify. Sales wants to lower the price. We can inspect approval records or run another general satisfaction survey next week. We do not yet know where these purchases stopped.

**Intended response**

> Inspect the approval records and walk through the buying sequence with the relevant buyers. The price proposal depends on what “hard to justify” means in these purchases.
>
> The method of **discriminating diagnosis** means seeking evidence that would differ between plausible explanations. For example:
>
> - A documented budget cap below the total quote would support an affordability obstacle.
> - A funding request that cannot proceed without an executive sponsor would support an approval obstacle.
> - An approver rejecting the business case for a specific missing benefit would support a value-justification obstacle.
>
> These are possible explanations, not completed findings, and they can coexist. Repeating the general objection in a survey would not establish which process stopped the purchase. A lower price might address one obstacle while leaving another intact.

**User follow-up**

> We have records for seven dormant accounts. Four could not submit a business case because a required executive sponsor was missing. Two had approved budgets below the total quote. The seventh has not supplied records. Does that establish the problem?

**Intended update**

> It establishes different obstacles in six reviewed accounts and leaves one unresolved. The four missing sponsors are a specific approval blocker; lowering price alone would not satisfy that requirement. The two funding caps are concrete affordability constraints and deserve separate commercial review.
>
> Do not generalize these findings to accounts that were not examined or promise that either remedy will close a sale. For the sponsor-blocked accounts, follow whether a sponsor is established, whether the business case can then be submitted and what barriers remain. For the capped accounts, check whether a commercially viable offer would fit the approved budget and whether other approvals are outstanding.

The diagnosis supplies evidence for an action discussion. It does not establish the sales effect of introducing sponsors earlier or lowering price.

## 3. Choose the commercial result, then update when an input changes

**User**

> Use the reasoning skill to choose between current outreach and a new offer for a bounded repeat pilot. We randomly assigned 120 eligible accounts to each before outreach, kept assignments stable across account members and used the same contact policy. Every account has complete sixty-day outcomes. Current outreach produced ten wins; the offer produced sixteen. Finance reconciled net contribution per win over those same sixty days: $900 for current outreach and $550 for the offer, after all variable costs and concessions. Each group also incurred $600 in setup cost, not included in the per-win amounts. Our rule is to choose the higher observed net contribution, not the higher win count.

**Intended response**

> Choose current outreach under the stated rule. It produced fewer wins but $200 more observed net contribution.
>
> | Sixty-day result | Current outreach | New offer |
> | --- | ---: | ---: |
> | Assigned accounts | 120 | 120 |
> | Wins | 10 | 16 |
> | Contribution from wins | 10 × $900 = $9,000 | 16 × $550 = $8,800 |
> | Setup cost | $600 | $600 |
> | Net contribution | **$8,400** | **$8,200** |
>
> This applies the decision method of **incremental analysis**: compare the difference in consequences between the alternatives. Here, six additional wins do not offset the offer's lower contribution per win. The comparison retains all assigned accounts and accounts for each cost once. The observed totals support this pilot choice; no precision estimate has been supplied for the difference in future comparable accounts.

**User correction**

> Finance corrected the offer's net contribution per win to $600. Nothing else changed. Keep the same decision rule.

**Intended update**

> Choose the offer. Its corrected result is 16 × $600 − $600 = **$9,000**, compared with **$8,400** for current outreach: a $600 advantage. The recommendation changes because Finance corrected one input, not because the objective or win counts changed. The original assignment and complete follow-up findings remain intact.

No new definition is needed for the same decision method. The update should recompute the affected result rather than repeat the whole study review.

## 4. Recognize when access is the prerequisite

**User**

> Check whether our interviewer used leading questions. I have supplied the study summary, but the recordings are not accessible and the questions are not quoted.

**Intended response**

> I cannot assess the wording from this summary. Please provide the question guide or a transcript of the questions and relevant follow-ups.

The missing material is necessary for that specific task. If the user instead asks whether a conclusion follows from an already visible summary, the agent should assess that inference without demanding recordings that would not change it. A routine request such as correcting a sentence also does not require a full reasoning review.
