# Audit Module

Detailed checks for email infrastructure health.

## Authentication Checks

| Check | Pass Criteria | How to Verify |
|-------|--------------|---------------|
| SPF | Record exists, includes sending IPs | DNS lookup |
| DKIM | Valid DKIM record for sending domain | DNS lookup |
| DMARC | Policy set to quarantine or reject | DNS lookup |
| Custom tracking domain | Configured and resolving | HTTP check |

## Volume and Warming

| Warming Stage | Daily Limit | Duration |
|--------------|------------|----------|
| Week 1-2 | 5-10/day | Ramp slowly |
| Week 3-4 | 15-25/day | Monitor bounces |
| Week 5-8 | 30-50/day | Full capacity |
| Mature | 50-75/day | Maintain |

**Red Flags:**
- Bounce rate above 3% on any account
- Spam complaints above 0.1%
- Sudden volume spike (more than 2x day-over-day)
- Authentication failures
- Blacklist appearances

## Health Classification

| Status | Criteria |
|--------|----------|
| Healthy | All auth passes, bounce < 2%, complaints < 0.05% |
| Warning | Minor auth issue OR bounce 2-3% OR complaints 0.05-0.1% |
| Critical | Auth failures OR bounce > 3% OR complaints > 0.1% OR blacklisted |

## Output Format

For each account, produce a status summary with auth results, volume data, health metrics, and overall status.
