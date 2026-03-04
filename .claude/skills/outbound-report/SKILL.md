---
name: outbound-report
description: Generate weekly outbound performance reports for clients. Use when creating reports, sending campaign updates, or reviewing performance.
---

# Outbound Report

Generate weekly performance reports for client outbound campaigns.

## When to Activate

- User asks to "generate report", "weekly report", "campaign update"
- End of week (Friday workflow)
- Client asks for a status update

## Process

### Step 1: Gather Data

For the specified client and time period:
1. Read campaign data from `workspace/clients/{client}/campaigns/`
2. Collect metrics: emails sent, opens, replies, meetings booked
3. Check email infrastructure health

### Step 2: Calculate Metrics

See [GENERATE.md](modules/GENERATE.md) for metric calculations.

Key metrics:
- Open rate (target: 50%+)
- Reply rate (target: 3-5%)
- Positive reply rate
- Meetings booked
- Pipeline generated

### Step 3: Generate Report

Output to:
```
workspace/clients/{client}/campaigns/reports/weekly-report-{date}.md
```

## Report Structure

```
# Weekly Outbound Report - {Client} - Week of {date}

## Summary
{3-line executive summary}

## Campaign Performance
{Table with metrics per campaign}

## What Worked
{Top performing sequences, subject lines, segments}

## What We're Changing
{Adjustments for next week}

## Next Week Plan
{Volume, new campaigns, tests}
```
