---
name: prospect-research
description: Analyze a prospect's website and product to understand what they sell, who they sell to, and what buying triggers exist. First step of the outreach pipeline.
---

# Prospect Research

Analyze a prospect's product and market position to inform outreach strategy.

## When to Activate

- User provides a company website URL for research
- Starting a new outreach campaign for a client
- Part of the `/outreach` pipeline (Step 1)

## Process

### Step 1: Website Analysis

Visit the prospect's website and extract:
- What problem do they solve?
- What is their solution?
- Who is their ideal customer?
- What are their key value propositions?

### Step 2: Buyer Profile

Identify:
- Decision maker titles (who buys this?)
- Company types that need this
- Buying situations (when do they buy?)

### Step 3: Buying Triggers

Find 3-5 observable signals that indicate a company needs this product NOW:
- Job postings (hiring for roles the product replaces/supports)
- Funding rounds (budget available for new tools)
- Leadership changes (new leader reviewing tech stack)
- Regulatory changes (compliance deadlines)
- Growth signals (team expansion, new markets)

### Step 4: Existential Data Point (EDP)

Identify the ONE data point that proves a prospect needs this product right now. This is the strongest buying signal.

Examples:
- For a CRM: "Job posting for Salesforce admin" (means CRM is complex enough to need dedicated admin)
- For recruiting tool: "10+ open roles on careers page" (actively struggling with hiring volume)
- For security tool: "SOC 2 certification mentioned on website" (compliance-driven buying)

### Step 5: Output

See [PRODUCT-PROFILE.md](modules/PRODUCT-PROFILE.md) for the output template.

Save to: `workspace/outreach/{date} - {client}/product-profile.md`

## Related Skills

- **buyer-tiering** - Next step: segment prospects by urgency
- **campaign-strategy** - Final step: write email sequences
