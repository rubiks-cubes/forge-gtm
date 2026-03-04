---
name: proposal-builder
description: Build client proposals for outbound campaign engagements. Use when creating proposals, scoping projects, or preparing for pitch meetings.
---

# Proposal Builder

Create professional proposals for prospective outbound clients.

## When to Activate

- User mentions "build proposal", "create proposal", "scope project"
- User has call notes or discovery information to work with
- User is preparing for a pitch meeting

## Process

### Step 1: Discovery

See [DISCOVERY.md](modules/DISCOVERY.md)

Extract from provided information:
- Client's current situation (team size, current pipeline, tools)
- Pain points (what's broken or underperforming)
- Goals (revenue target, pipeline target, timeline)
- Budget indicators

### Step 2: Solution Design

Based on discovery, recommend:
- Campaign scope (number of campaigns, volume)
- Services included (list building, copy, infrastructure, reporting)
- Timeline
- Expected results (pipeline generated, meetings booked)

### Step 3: Generate Proposal

See [OUTPUT.md](modules/OUTPUT.md)

Output two documents:
- `proposal.md` - Internal version with full analysis
- `proposal-client.md` - Client-facing version, clean and professional

## Output Location

```
workspace/clients/{client}/proposals/{date}-proposal.md
workspace/clients/{client}/proposals/{date}-proposal-client.md
```

## Default Pricing

| Service | Monthly | Setup |
|---------|---------|-------|
| Managed Outbound (1 campaign) | $3,500/mo | $1,000 |
| Managed Outbound (3 campaigns) | $8,000/mo | $2,000 |
| List Building Only | $1,500/mo | $500 |
| Full GTM Package | $12,000/mo | $3,000 |
