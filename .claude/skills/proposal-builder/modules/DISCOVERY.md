# Discovery Module

Extract engagement opportunities from provided context.

## Input Sources

Accept any of:
- Discovery call transcripts
- Email threads
- Brief descriptions from the user
- Website analysis

## Extraction Process

### Step 1: Read and Extract

From the provided input, identify:

1. **Current State** - What tools are they using? What's their team size? How much pipeline are they generating today?
2. **Pain Points** - Where are they losing time, money, or opportunities?
3. **Goals** - What does success look like for them?
4. **Timeline** - When do they need results?

### Step 2: Present Understanding

Show your analysis:

> **Here's what I'm seeing:**
>
> **Current state:** {summary}
> **Main pain points:** {list}
> **Goals:** {list}
>
> Does this capture it? What am I missing?

Wait for confirmation before proceeding.

### Step 3: Fill Gaps

For missing information, use reasonable assumptions and flag them:

| Assumption | Default | Flag |
|------------|---------|------|
| Average deal size | $50K ARR | Validate on call |
| Sales cycle | 3-6 months | Validate on call |
| Current conversion rate | 2% reply, 0.5% meeting | Industry average |
