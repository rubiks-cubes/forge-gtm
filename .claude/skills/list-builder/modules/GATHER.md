# Gather Module

Execute prospect searches using available data sources.

## Data Sources

| Source | Best For | How |
|--------|----------|-----|
| **Apollo** | B2B contacts with verified emails | API search with filters |
| **LinkedIn Sales Nav** | Account-based targeting | Export + enrichment |
| **Clay** | Enrichment at scale | Table builder integration |
| **Manual research** | Niche or hard-to-reach segments | Web research + LinkedIn |

## Search Process

### Using Apollo (Default)

Build the search query from ICP criteria:

1. Set industry filter from client ICP
2. Set title/seniority filter
3. Set company size range
4. Set geography
5. Apply exclusion filters (competitors, existing clients)
6. Execute search, cap at requested volume

### Using Clay (When Available)

1. Start with Apollo or LinkedIn as the source
2. Use Clay tables for enrichment columns
3. Apply scoring/filtering within Clay
4. Export final list

### Quality Filters

After gathering raw results, apply:

- **Recency filter**: Person has been in role 3+ months (avoid job hoppers)
- **Company health**: Active website, real social presence
- **Email quality**: Prefer verified business emails over catch-all domains
- **Deduplication**: Check against all active campaigns for this client

## Output

Return structured CSV with standardized column names.
Always include `linkedin_url` for manual verification if needed.
