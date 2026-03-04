---
name: campaign-strategy
description: Generate cold email sequences from product profiles and tier definitions. Supports standard (angle-based) and tier-based (situation messaging) modes.
---

# Campaign Strategy

Create high-converting cold email sequences.

## When to Activate

- User asks to "write emails", "create a sequence", "build a campaign"
- After buyer tiering produces tier definitions
- Part of the `/outreach` pipeline (Step 3)

## Two Modes

### Standard Mode

Use when you have a business document, case study, or offer description. Generate sequences based on messaging angles.

**Angles:**
- Case study: Lead with a specific customer result
- Pain/poke: Lead with a problem they're likely experiencing
- Direct offer: Lead with what you do and why it matters
- Trigger-based: Lead with a specific event or signal

### Tier-Based Mode (PVP)

Use when you have a product profile + tier definitions from the outreach pipeline. Each tier gets its own sequence with different messaging.

**Structure per tier:**
- Hook: Describe THEIR situation (not your offer)
- Value: Something you deliver IN the email (not teased)
- Bridge: A question that flows naturally from the value

## Email Structure

All sequences follow the same structure:

```
Thread 1 (Days 0-3):
  Email 1.1 - Subject (3-4 words) + main message
  Email 1.2 - Empty subject (auto-threads) + follow-up

Thread 2 (Days 7-10):
  Email 2.1 - New subject (3-4 words) + different angle
  Email 2.2 - Empty subject (auto-threads) + soft referral
```

## Process

### Step 1: Load Context

Read:
- Client's offer (`workspace/clients/{client}/offer.md`)
- Product profile (if tier-based mode)
- Tier definitions (if tier-based mode)
- Output style rules (`.claude/output-styles/outreach.md`)

### Step 2: Generate Sequences

See [SEQUENCE-GENERATOR.md](modules/SEQUENCE-GENERATOR.md) for generation rules.

Check against [BANNED.md](modules/BANNED.md) before finalizing.

### Step 3: Review Checkpoint

**STOP before sending.** Present the sequences for human review:

> **Review checklist:**
> - [ ] Under 75 words per email
> - [ ] Clear "why you, why now?" in email 1.1
> - [ ] Specific numbers (3.72x not "significant improvement")
> - [ ] No banned patterns
> - [ ] Soft CTAs (question format)
> - [ ] Two distinct threads with different angles
>
> Approve or request changes?

### Step 4: Output

Save to:
```
workspace/outreach/{date} - {client}/tier-{N}/campaign-sequence.md
```

Or for standard mode:
```
workspace/clients/{client}/campaigns/{campaign}/email-sequence.md
```

## Related Skills

- **prospect-research** - Step 1 of outreach pipeline
- **buyer-tiering** - Step 2 of outreach pipeline
- **list-builder** - Build lists to send sequences to
