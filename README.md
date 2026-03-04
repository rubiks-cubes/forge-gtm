# Forge GTM - Claude Code AI Workspace

A ready-to-use Claude Code workspace for B2B outbound sales agencies. Clone it, customize the context files for your business, and start running outbound campaigns with AI.

This is a reference implementation showing how to structure a Claude Code workspace for a real business use case: managing multiple B2B clients, running outbound email campaigns, and generating proposals and reports.

## What's Inside

### Context (your business knowledge)

| File | Purpose |
|------|---------|
| `context/icp.md` | Agency's ideal client profile |
| `context/messaging.md` | Core messaging and objection handling |
| `context/offers.md` | Service packages and pricing |
| `context/tone-of-voice.md` | Writing rules for all copy |

### Skills (repeatable processes)

| Skill | What it does |
|-------|-------------|
| **campaign-strategy** | Generate cold email sequences (standard or tier-based) |
| **prospect-research** | Analyze a prospect's product, find buying triggers |
| **buyer-tiering** | Segment prospects into 3 tiers by buying urgency |
| **list-builder** | Build qualified prospect lists from ICP criteria |
| **outbound-report** | Generate weekly performance reports |
| **proposal-builder** | Create client proposals from discovery notes |
| **email-infra-check** | Audit email deliverability and domain health |

### Commands (quick actions)

| Command | What it does |
|---------|-------------|
| `/morning` | Daily briefing across all clients |
| `/load-client {name}` | Load a client's full context |
| `/new-campaign {client}` | Set up a new outbound campaign |
| `/outreach {client}` | Run the full outreach pipeline |

### Workspace (where work happens)

- `workspace/clients/` - Client folders with context, campaigns, and reports
- `workspace/outreach/` - Outreach pipeline outputs (research, tiering, sequences)
- `workspace/content/` - Agency content (LinkedIn posts, newsletters)

## The Outreach Pipeline

The `/outreach` command runs a 5-step pipeline:

```
Research -> Tiering -> List Building -> Sequences -> Human Review
```

Each step uses a dedicated skill and produces artifacts that feed into the next. All sequences require human approval before sending.

## Demo Data

Two fictional clients are included to show how the workspace operates:

- **NovaCRM** - Series A CRM company, multi-campaign engagement ($8K/mo)
- **PeakHire** - Seed-stage HR tech, single campaign ($3.5K/mo)

Both include complete examples: client context, ICP definitions, campaign briefs, email sequences, lead lists, weekly reports, and outreach pipeline outputs.

## Getting Started

1. Install [Claude Code](https://docs.anthropic.com/en/docs/claude-code)
2. Clone this repo: `git clone https://github.com/riccardovandra/forge-gtm.git`
3. Open in VS Code, then start Claude Code from the extension
4. Try `/morning` to see the daily briefing
5. Try `/load-client novaCRM` to load a client
6. Try `/outreach peakhire` to run the outreach pipeline

## How to Customize

1. **Replace the context files** in `context/` with your agency's ICP, messaging, offers, and tone
2. **Create your first real client** by copying the `workspace/clients/novaCRM/` structure
3. **Adjust the skills** if your workflow differs (e.g., different email sequence structure)

## Related

- [Productivity Suite Plugin](https://github.com/riccardovandra/cc-plugin-productivity-suite) - 14 integration skills for Claude Code (Gmail, Google Sheets, Docs, Drive, Slack, ClickUp, and more)

## License

MIT
