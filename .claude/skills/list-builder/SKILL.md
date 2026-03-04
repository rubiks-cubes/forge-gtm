---
name: list-builder
description: Build qualified prospect lists for client outbound campaigns. Use when building lists, finding prospects, or gathering leads for a client.
---

# List Builder

Build qualified prospect lists by combining client ICP data with targeting criteria.

## When to Activate

- User asks to "build a list", "find prospects", or "gather leads"
- User mentions a specific client's outbound campaign
- User provides targeting criteria (industry, title, company size)

## Process

### Step 1: Load Client Context

Read the client's ICP file:
```
workspace/clients/{client}/icp.md
```

Extract:
- Target industries
- Decision maker titles
- Company size range
- Geographic focus
- Exclusion criteria

### Step 2: Define Search Criteria

Present the extracted criteria to the user:

> **Targeting for {client}:**
> - Industries: {list}
> - Titles: {list}
> - Company size: {range}
> - Location: {geography}
>
> Confirm or adjust?

### Step 3: Execute Search

Use the criteria to build the prospect list.
See [GATHER.md](modules/GATHER.md) for search execution details.

### Step 4: Quality Check

For each lead, verify:
- Title matches ICP seniority level
- Company size within range
- Industry alignment
- No duplicates with existing campaigns

### Step 5: Output

Save results to:
```
workspace/clients/{client}/campaigns/{campaign}/leads.csv
```

Format: first_name, last_name, title, company, industry, size, location, linkedin_url

## Output Example

| first_name | last_name | title | company | industry | size | location |
|------------|-----------|-------|---------|----------|------|----------|
| Sarah | Chen | VP Sales | Acme Corp | SaaS | 85 | San Francisco, CA |
| James | Park | Head of Revenue | DataFlow | Analytics | 120 | New York, NY |

## Related Skills

- **outbound-report** - Track campaign performance after launch
- **proposal-builder** - Build proposals when prospects respond
