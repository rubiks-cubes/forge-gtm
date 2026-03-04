---
name: email-infra-check
description: Audit email sending infrastructure health across client accounts. Use when checking deliverability, before launching campaigns, or during weekly reviews.
---

# Email Infrastructure Check

Monitor and audit email sending health for client campaigns.

## When to Activate

- User asks to "check email health", "audit deliverability"
- Before launching a new campaign
- Weekly infrastructure review

## Process

### Step 1: Identify Client Accounts

Read the client's campaign folder for active sending domains and accounts.

### Step 2: Run Audit

See [AUDIT.md](modules/AUDIT.md) for detailed checks.

Check each sending account for:
- Domain authentication (SPF, DKIM, DMARC)
- Sending volume vs. warming stage
- Bounce rate (flag if > 3%)
- Spam complaint rate (flag if > 0.1%)
- Inbox placement estimate

### Step 3: Report

Generate a health scorecard:

| Account | Domain Auth | Volume | Bounce Rate | Status |
|---------|-------------|--------|-------------|--------|
| account-1@send.client.com | Pass | 45/day | 1.2% | Healthy |
| account-2@send.client.com | Fail DMARC | 30/day | 4.1% | Warning |

### Step 4: Recommendations

For any flagged issues, provide:
- What's wrong
- How to fix it
- Priority (critical / warning / info)

## Related Skills

- **outbound-report** - Include infrastructure health in weekly reports
