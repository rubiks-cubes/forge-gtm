# Sequence Generator

Rules for generating email sequences.

## Pre-Generation

Before writing any email:
1. Read the client's offer and identify: value prop, case studies, pain points, guarantee, differentiation
2. Read BANNED.md for patterns to avoid
3. Read `.claude/output-styles/outreach.md` for copy rules

## Structure Rules

### Threading
- 2 threads, 2 emails each = 4 emails total
- Thread 1: Primary angle
- Thread 2: Secondary angle (completely different approach)
- Follow-up emails (1.2 and 2.2) have EMPTY subject lines (auto-threads in email client)

### Subject Lines
- 3-4 words maximum
- Lowercase (except proper nouns)
- No punctuation
- No clickbait or urgency words

Good: "your pipeline forecast", "sales team scaling"
Bad: "Quick question for you!", "DON'T MISS THIS"

### Body Rules
- Under 75 words per email
- One idea per email
- First line: about THEM, not you
- No introductions ("Hi, I'm John from...")
- Soft CTA: question format, never "book a call"

### SPINTAX

Use SPINTAX for natural variation:

```
{Hey|Hi} {{first_name}} - {noticed|saw} {{company_name}} is {growing|scaling} the sales team.
```

Common SPINTAX:
- Greetings: {Hey|Hi}
- Transitions: {Noticed|Saw|Came across}
- CTAs: {Would|Could} a {quick|short} {look|walkthrough} be {useful|helpful}?

### Variables

Standard variables:
- {{first_name}} - Prospect's first name
- {{company_name}} - Company name
- {{title}} - Job title

Custom variables (from enrichment):
- {{custom_variable}} - Dynamic per-lead data

## Tier-Based Messaging

### Tier 1 (In-Market NOW)
- Lead with their SPECIFIC situation
- Reference the observable trigger directly
- Deliver concrete value (data point, insight, introduction)
- Bridge with a natural question

### Tier 2 (Approaching)
- Lead with an industry trend or pattern
- Educate them on something they'll face soon
- Share a relevant proof point
- Bridge with curiosity

### Tier 3 (ICP Fit)
- Lead with a strong proof point (case study, stat)
- Keep it short and direct
- Make it easy to forward to the right person
- Bridge with a low-commitment question
