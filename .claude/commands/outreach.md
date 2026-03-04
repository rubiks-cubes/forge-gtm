---
description: Full outreach pipeline. Researches a prospect's product, defines buyer tiers, builds lists, generates email sequences, and presents for review.
argument-hint: <client-name>
---

Run the full outreach pipeline for `$ARGUMENTS`.

## Pipeline Overview

```
Research -> Tiering -> List Building -> Sequences -> Review
```

Each step produces artifacts that feed into the next.

## Process

### Step 1: Research

Use the **prospect-research** skill.

Read the client's offer from `workspace/clients/$ARGUMENTS/offer.md` to understand what the client sells.

Analyze their product and market. Output: `product-profile.md`

### Step 2: Tiering

Use the **buyer-tiering** skill.

Take the product profile and segment prospects into 3 tiers by buying urgency. Output: `tier-definitions.md`

### Step 3: List Building

Use the **list-builder** skill.

For each tier, build a prospect list using the tier's criteria. Start with Tier 1 (highest response rate). Output: `tier-{N}/leads.csv`

### Step 4: Sequence Generation

Use the **campaign-strategy** skill in tier-based mode.

For each tier, write a 4-email, 2-thread sequence with messaging tailored to that tier's situation. Output: `tier-{N}/campaign-sequence.md`

### Step 5: Review (HARD STOP)

Present ALL sequences for human review before any sending.

**Review checklist:**
- [ ] Tier 1 messaging references a specific, observable trigger
- [ ] Tier 2 messaging educates or shares insight
- [ ] Tier 3 messaging leads with proof point
- [ ] All emails under 75 words
- [ ] No banned patterns (check BANNED.md)
- [ ] Soft CTAs only (question format)
- [ ] Subject lines are 3-4 words, lowercase
- [ ] SPINTAX included for variation

## Workspace

All outputs are saved to:
```
workspace/outreach/{date} - {client}/
├── product-profile.md
├── tier-definitions.md
├── tier-1/
│   ├── leads.csv
│   └── campaign-sequence.md
├── tier-2/
│   ├── leads.csv
│   └── campaign-sequence.md
└── tier-3/
    ├── leads.csv
    └── campaign-sequence.md
```

## Important

- This pipeline is iterative. The user can adjust at any step.
- Always read the client's full context before starting.
- Never skip the review step. Human approval is required before sending.
