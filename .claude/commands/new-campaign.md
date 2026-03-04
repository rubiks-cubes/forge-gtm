---
description: Set up a new outbound campaign for a client. Creates folder structure, campaign brief, and walks through targeting.
argument-hint: <client-name>
---

Set up a new outbound campaign for the specified client.

## Process

### 1. Load Client Context

Read the client's files:
- `workspace/clients/$ARGUMENTS/context.md`
- `workspace/clients/$ARGUMENTS/icp.md`
- `workspace/clients/$ARGUMENTS/offer.md`

### 2. Gather Campaign Details

Ask the user:

1. **Campaign name** - What should we call this campaign?
2. **Target segment** - Which ICP segment are we targeting?
3. **Volume** - How many prospects do we need?
4. **Timeline** - When does this need to launch?
5. **Angle** - What messaging approach? (case study, pain-based, direct offer, trigger-based)

### 3. Create Campaign Folder

Create the following structure:
```
workspace/clients/{client}/campaigns/{campaign-name}/
├── campaign-brief.md
├── email-sequence.md  (placeholder - to be filled by campaign-strategy)
└── leads.csv          (placeholder - to be filled by list-builder)
```

### 4. Generate Campaign Brief

Create `campaign-brief.md` with:
- Target segment definition (from ICP)
- Messaging angle
- Volume and timeline
- Success metrics (target reply rate, meetings)
- Status: SETUP

### 5. Next Steps

Present to the user:

> Campaign "{name}" is set up for {client}.
>
> Next steps:
> 1. Build the prospect list: "build a list for {campaign-name}"
> 2. Write the email sequence: "write emails for {campaign-name}"
> 3. Check infrastructure: "check email health for {client}"
