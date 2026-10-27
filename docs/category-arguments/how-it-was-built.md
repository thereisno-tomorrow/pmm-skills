# How Category Arguments was built

This skill comes from category and founder research I did on one company's public conversation. The question was what the people in that category were arguing about, and where each founder stood.

## The research behind it

Collection centred on X. 33 searches across five lanes surfaced 1,024 unique posts, and 685 looked relevant at first. After each was read with its parent and quoted posts, 458 stayed, each with the reason recorded.

The work then ran in a fixed order: collect, recover each post's context, map the category's arguments, write a perspective for each founder, and finally correct the category map using what the founders' own statements showed. That last step mattered. One founder's posts made clear that openness and product quality were two separate questions, not one, and the map was corrected to show both axes.

## Calls that shaped it

**Context before judgment.** Every post's parent and quoted post was recovered before deciding to keep or drop it. Judgments were recorded with their reasons, separately from the mechanics of fetching, so a reader can see why each source is in the collection.

**The map revises itself.** Founder evidence is allowed to correct the category map. The skill builds that in as a separate check, because a derived map is easy to trust once it exists.

**Per-person attribution.** Each founder got their own brief. A technical comment from one person was not stretched into a broad thesis for the whole company, and a public position was kept apart from proof that the product delivers it.

**No quota of arguments.** That project ended with seven arguments. The skill treats seven as one case's outcome, not a target, and lets the map grow from whatever the evidence supports.

## From research to skill

The skill keeps that method and makes it portable: multi-lane collection, de-duplication by post ID, context recovery before attribution, filtering you can audit, source-linked claims, separate founder briefs, and maps that can be revised when new statements arrive. The X helper turns the collection step into commands. It uses Grok's X search to find candidate posts and a public mirror to fetch the exact text, and it records the query that found every post.

The examples in [`references/ledger.md`](../../skills/category-arguments/references/ledger.md) are fictional.

I directed the research and decided what the skill keeps. AI agents ran the searches, wrote the Python helper and drafted the files.

[Back to the guide](README.md)
