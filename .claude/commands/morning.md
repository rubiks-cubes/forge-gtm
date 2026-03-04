---
description: Daily briefing. Shows campaign status across all clients, flags issues, and surfaces priorities for the day.
---

Start the day with a full view across all active clients and campaigns.

## Process

### 1. Scan Active Clients

Read all client folders in `workspace/clients/` and identify:
- Active campaigns (folders with recent activity)
- Upcoming deadlines
- Flagged issues from previous reports

### 2. Campaign Health Check

For each active campaign, check:
- Current reply rate (flag if below 1%)
- Leads remaining in sequence
- Any bounces or complaints from recent reports

### 3. Today's Priorities

Based on the scan, list:

1. **Urgent** - Campaigns with deliverability issues or expiring lead lists
2. **Important** - Reports due, proposals to send, campaigns to launch
3. **Routine** - Regular check-ins, content to post

### 4. Display

Present as:

```
## Morning Briefing - {date}

### Active Clients
| Client | Active Campaigns | Status |
|--------|-----------------|--------|

### Priorities Today
1. {urgent item}
2. {important item}
3. {routine item}

### Alerts
- {any issues flagged}

---
What do you want to work on first?
```
