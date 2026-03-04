---
description: Load a client's full context to start working on their account.
argument-hint: <client-name>
---

Load all context for the specified client so you can work on their account.

## Process

### 1. Read Client Files

Load these files for `$ARGUMENTS`:

- `workspace/clients/$ARGUMENTS/context.md` - Client background
- `workspace/clients/$ARGUMENTS/icp.md` - Their target audience
- `workspace/clients/$ARGUMENTS/offer.md` - Their value proposition

### 2. Scan Active Campaigns

List all folders in `workspace/clients/$ARGUMENTS/campaigns/` and identify which are active (check for campaign-brief.md with status).

### 3. Display Context Summary

Present as:

```
## Client Loaded: {client name}

**Industry:** {industry}
**Stage:** {funding stage}
**ICP:** {one-line summary of target audience}
**Offer:** {one-line summary of value proposition}
**Active Campaigns:** {list with status}
**Last Report:** {date of most recent report}

---
Ready to work on {client name}. What do you need?
```

### 4. Maintain Context

For the rest of this conversation, always reference this client's ICP, offer, and messaging when generating any work product.
