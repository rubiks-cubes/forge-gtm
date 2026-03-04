---
name: buyer-tiering
description: Segment prospects into 3 tiers based on proximity to buying moment. Takes a product profile as input and outputs tier definitions with criteria and expected response rates.
---

# Buyer Tiering

Segment prospects into 3 tiers by how close they are to buying.

## When to Activate

- After `prospect-research` produces a product profile
- User wants to prioritize prospects by urgency
- Part of the `/outreach` pipeline (Step 2)

## Input

Read the product profile from:
```
workspace/outreach/{date} - {client}/product-profile.md
```

## The Three Tiers

### Tier 1: In-Market NOW (Expected response: 15-25%)

These prospects have an ACTIVE buying signal. Something observable proves they need the product right now.

**Signal types:**
- EDP is present (the existential data point from research)
- Job posting for a role the product replaces or supports
- Recent funding round (budget unlocked)
- Leadership change (new CRO/VP reviewing stack)
- Regulatory deadline approaching
- Public announcement of relevant initiative

### Tier 2: Approaching (Expected response: 5-10%)

Leading indicators suggest they'll need the product soon, but no active buying signal yet.

**Signal types:**
- Hiring growth in relevant department
- Tech stack changes (adopting complementary tools)
- Competitor movement (their competitor just adopted this type of tool)
- Market pressure (industry shift creating new requirements)
- Team scaling signals

### Tier 3: ICP Fit (Expected response: 1-3%)

Right profile, no urgency signal. Standard targeting based on firmographics.

**Signal types:**
- Matches industry, size, and role criteria
- No specific buying trigger detected
- General ICP alignment

## Process

### Step 1: Define Tier Criteria

For each tier, specify:
- Observable signals (what you can find in data)
- Where to find these signals (job boards, LinkedIn, news, tech databases)
- Volume estimate (how many prospects fit this tier)

### Step 2: Messaging Approach

Each tier gets different messaging:

| Tier | Approach | Example |
|------|----------|---------|
| 1 | Direct value delivery - they feel the pain NOW | "Your [specific signal] suggests [specific insight]" |
| 2 | Education and insight - help them see what's coming | "Companies scaling their [department] often find..." |
| 3 | General value proposition - plant the seed | "[Proof point] for companies like [theirs]" |

### Step 3: Output

See [TIER-TEMPLATE.md](modules/TIER-TEMPLATE.md) for the output format.

Save to: `workspace/outreach/{date} - {client}/tier-definitions.md`

## Key Principle

The tier IS the message. You don't write one email and send it to everyone. The list structure determines the messaging strategy.

## Related Skills

- **prospect-research** - Previous step: product analysis
- **campaign-strategy** - Next step: write sequences per tier
- **list-builder** - Build lists using tier criteria
