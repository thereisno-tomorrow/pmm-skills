# Worked calibration: investigative operations

These are fictional companies, records and numbers, created to teach operations recovered from the author's earlier company case studies. They are not actual findings from those cases. Use the method and infer afresh from the researched company's evidence. The examples intentionally include stopping and unresolved verdicts: depth does not require a confident commercial recommendation.

## Product mechanisms and specification arithmetic

**Question:** Can fictional ForgeMap meet a buyer's 0.20 mm complete-system tolerance on a large workpiece, and what does its “adaptive” claim mean?

**Evidence packet:** P1 vendor v7 manual: offline workstation plans a path; an on-cell service scans a reference-compatible workpiece, computes a pose transform and offsets the path before export; customer controller executes it. P2 sensor datasheet: linearity ±0.02% of a 1200 mm measurement range, resolution 0.08 mm. P3 educational white paper: this technology class can resolve 0.005 mm in a different short-range configuration. P4 v7 notes: mesh limit increased from 600 MB to 900 MB; scan-timeout handling repaired. P5 no matching whole-cell acceptance results supplied.

**Investigation:** First draw planning → scan/registration → path offset → native program → customer execution. Locate the human, runtime and responsibility boundary at each step. “No vendor runtime on the robot controller” does not mean no vendor service on the cell. The documented adaptation handles pose before execution; it does not establish geometry regeneration, force compensation or within-pass feedback. Ask separately if those are claimed.

Next normalize the spec: `0.02 / 100 × 1200 mm = 0.24 mm`. Label this a derived component-linearity bound. It is not resolution, complete-system accuracy or a measured finished-part tolerance. Do not add error terms without an error model or infer total accuracy from this one number. P3's class-level resolution does not establish the shipped configuration's resolution, and comparison with P2 linearity would mix metrics. The shipped sensor's stated resolution is 0.08 mm; compare that with P3 only with configuration differences explicit.

The buyer's 0.20 mm requirement cannot be accepted from this packet. One component already has a stated bound larger than that requirement, and other error terms are unquantified; this is a reason to seek a matching acceptance/error-budget result, not proof every deployment fails. P4 supports a current 900 MB limit for v7 and a repaired timeout condition, not a current 600 MB ceiling or universal reliability.

**Usable verdict:** documented pre-run pose correction, configuration-dependent sensor limits and an unresolved full-system acceptance claim. **Gap route:** matching-version/configuration acceptance test, calibration method and robot contribution; product fit depends on the result. **Gate:** mechanism/specification investigation complete within supplied scope; achieved-performance verification open. A homepage and feature list would leave the operational-depth gate open.

## Buyer populations and purchase gates

**Question:** Who could use ForgeMap and what must be proved to buy it?

**Evidence packet:** B1 same-year census: 12,000 small plants, 4% have compatible equipment; 600 large plants, 35% have it. B2 an earlier survey reported 18% ownership among a large-plant sample. B3 buyer job descriptions assign engineers equipment justification and finance budget approval. B4 partner program assigns proof and commissioning to integrators. B5 a vendor-selected story claims ten labor-hours saved weekly but gives no utilization or complete-cell cost. Variable-part need among equipment owners is unmeasured.

**Investigation:** Compute compatible small plants `12,000 × 0.04 = 480`; large plants `600 × 0.35 = 210`; total `690`. Large plants have a much higher within-group ownership rate, while small plants form `480 / 690 ≈ 69.6%` of this compatible installed base. Neither quantity establishes purchase intent, and compatibility alone does not establish variable-part need or deployment feasibility. B2 cannot form a time trend with B1 without equivalent universes and methods.

Map plant engineer=user/evaluator or possible champion; finance=budget approver; integrator=proof/delivery role under published program design. Do not label the integrator economic buyer without contracting evidence. Reconstruct a **candidate** sequence: trigger → configuration screening → proof on representative parts → full-cost justification → references/approval → commissioning. For each stage name actor, decision, evidence required and possible stop. B3/B4 support this model's parts, not observed deal frequency.

For economics distinguish labor expense actually removed/redeployed from hypothetical avoided downtime. B5 alone gives neither achieved savings nor payback: workload, utilization, labor value, installation, tooling, hardware and support are missing. The plausible need is a champion's finance-ready justification; the actual dominant lost-deal cause is unknown.

**Usable verdict:** condition-led candidate population and a sourced/transferred buying model. **Gap route:** buyer/operator accounts, procurement documents and authorized deployment/deal evidence, including losses and no-decisions. **Gate:** population arithmetic and model can be handed off with limits; observed customer fit and economics remain open.

## Alternatives and wrong-surface discovery

**Question:** What alternatives could satisfy this buyer's finishing job?

**Evidence packet:** C1 ForgeMap sells planning/perception software and requires a customer cell. C2 FinishServe sells a staffed complete cell on a usage contract, details subject to proposal. C3 an incumbent license is already installed and supports CAD-based planning plus documented measurement correction. C4 the priority application includes public repair depots. Initial research examined funding articles only; C5 an original award record names DepotWorks for a relevant coating project but does not identify all subcontractors or prove open commercial sales.

**Investigation:** Divide by buyer decision: extend existing equipment/tooling, procure a complete supported outcome, substitute manual work, or use an established supplier. Compare full scope, compatible configuration, technical limits, human/integrator work and payment/risk conditions. Do not compare a software-seat price with complete-cell cost as equivalent. Do not assume subscription procurement is automatically simpler. C3 defeats a simplistic “all incumbents trust CAD, only we measure” distinction; revise the comparison before evaluating differences.

Funding coverage is the wrong sole surface for public-depot suppliers. C5 provides a bounded additional alternative lead and documented public footprint. Verify supplier role, scope and relevance before promoting it into a head-to-head competitor claim. Awards do not measure all demand or prove ForgeMap loses to DepotWorks.

**Usable verdict:** alternatives differ in installed prerequisites, delivery responsibility and commercial exposure; relative preference remains untested. **Gate:** commercial comparison and procurement discovery are bounded; actual deal incidence and complete proposal economics remain open. The original company's four competitive layers are not a fixed taxonomy for every market.

## Advantage and deployability

**Question:** Does an open framework eliminate ForgeMap's advantage?

**Evidence packet:** A1 OpenFinish's maintained framework exposes a similar high-level pipeline. Its older finishing demo depends on an unsupported runtime; a current application supports one laboratory cell. A2 a consortium reports a production deployment with a public sponsor, lab and OEM; no full cost or duration. A3 developer discussion records several repositories, calibration and a library conflict. A4 ForgeMap documents five controller integrations and contracted support, with support outcomes unverified. A5 one pending old-interface patent application, unpublished filings unknown; air-gap deployment is optional and connected-data rights unknown.

**Investigation:** Separate framework availability, application maturity and demonstrated system deployment. A2 establishes reported production feasibility and an involved delivery arrangement. A3 documents integration work for that case; it does not prove universal difficulty, duration or unaffordability. The fair conclusion is neither “open source cannot do it” nor “download equals replacement.”

Test candidate barriers separately: integration coverage, calibration/commissioning knowledge, support, customer dependencies, ownership and rights. A funded rival would need to match the required configuration and service, not merely recreate the diagram. Five documented integrations support accumulated work, not a quantified catch-up time or durable exclusivity. Pending old-interface IP does not protect the current pipeline by implication, but absence of matching published claims does not prove no proprietary rights. Optional air gaps block automatic telemetry for those deployments, not every connected deployment or all forms of learning.

**Usable verdict:** architecture alone is not an established moat; documented configuration/productization work may be a relative strength, durability unresolved. **Gap route:** deployment/maintenance evidence for the relevant substitutes, integration acceptance, ownership, data rights and actual support burden. **Gate:** barrier hypotheses tested and bounded; no forced moat or forced absence of all advantage.

## Marketing admission and negative-claim repair

**Question:** Does marketing support the purchase, and what is the constraint?

**Evidence packet:** M1 an initial server-HTML check found no analytics tags. M2 rendered/consent-aware inspection observes tag loading, but conversion/CRM mapping is untested. M3 six cases exist in sitemap/navigation while 14 of 20 tested old paths fail; current cases contain application descriptions without measured economics. M4 technical demos and partner pages exist; qualified reach, win/loss and private sales material are unread. A generic audit also reports page-title lengths and color variations with no identified purchase consequence.

**Investigation:** Collect, verify/admit, then analyze. M2 overturns “no analytics”; revise that evidence and every dependent conclusion. The safe statement is instrumentation observed, attribution effectiveness unknown. M3 overturns “case studies do not exist”; the remaining observations are broken legacy routes and limited public outcome proof, not proven absence of customer/private evidence. Neither sitemap inclusion nor a few search results establish complete indexation.

Admit these findings because they affect discovery, reference diligence and financial justification. Keep generic audit trivia outside the diagnosis unless a concrete purchase or competitive connection is demonstrated. A missing public financial proof asset can motivate a hypothesis about champion support; it does not establish that finance blocks most deals or awareness is adequate. Activity, usage, qualified reach, stage conversion and revenue effect require different evidence.

**Gate:** supported surface observations and hypothesis can be delivered; attribution, private proof, bottleneck incidence and indexation remain explicitly open. Choosing a better observation method repairs the negative; simply adding a caveat does not.

## Confidence audit and handoff repair

Draft synthesis: “ForgeMap's variable-part installed-base niche is the best beachhead, and finance proof is its main bottleneck.” The prior examples support technical compatibility conditions and a visible public proof gap. They do not establish best segment, adequate qualified awareness, actual deal failures or causal priority.

Audit exact propositions. **Existence:** documented mechanism/assets, with source limits. **Performance:** matching system outcomes unverified. **Prevalence:** fit among actual customers/deals unknown. **Causality:** why deals win/stall unknown. Candidate rivals include poor qualified reach, technical mismatch, delivery capacity and commercial terms. Predict what each would produce: low qualified entries versus failed tests versus commissioning delays versus proposal losses. Design discriminating checks against defined opportunity/deployment records and wins/losses/no-decisions; first verify those records' coverage and definitions.

Rewrite to: “Variable-part work with compatible equipment is a candidate fit condition. Public materials support technical exploration but lack quantified economics in the inspected set. Relative segment value and the dominant commercial constraint are not established.” Update buyer/marketing verdicts and handoff, preserving supported technical facts. Hand off differences only where the compatible comparison supports them; if all examined alternatives are at parity, say so. Name unsupported wording and the minimum checks before using it.

**Final gate:** usable research inputs, traced reasoning, exact uncertainty and explicit unfinished validation. Research completion does not require inventing a winning position. It does require that a downstream stage can use the conclusions without repairing hidden overstatements.
