# Contributing to Awesome SRE Skills

Thank you for your interest in contributing! This list aims to catalog useful AI agent skills for SRE, observability, monitoring, and incident response.

## Inclusion Criteria

### What Qualifies as an "SRE Skill"?

To be included in this list, a skill must meet **both** of these requirements:

1. **Format** — Must be in one of these AI agent skill formats:
   - `SKILL.md` (OpenClaw/ClawHub)
   - `CLAUDE.md` or `commands/*.md` (Claude Code)
   - SkillMD cross-platform packages

2. **Domain** — Must relate to SRE, observability, or reliability engineering:
   - **Monitoring** — Metrics queries, dashboards, alerting
   - **Logging** — Log search, analysis, aggregation
   - **Tracing** — Distributed tracing, span analysis
   - **Incident Response** — Triage, escalation, runbooks
   - **Platform Integrations** — Datadog, PagerDuty, Prometheus, etc.

### Quality Requirements

| Requirement | Details |
|-------------|---------|
| **Active maintenance** | Commits within the last 6 months |
| **Documentation** | Clear README or skill docs explaining usage |
| **Working state** | Skill should function as described |
| **Star count** | No minimum required — new skills welcome! |
| **Licensing** | Free/open source preferred; paid tools must be clearly noted with 💰 |

### What Doesn't Qualify

- ❌ **MCP servers** — These belong in [awesome-devops-mcp-servers](https://github.com/rohitg00/awesome-devops-mcp-servers), not here
- ❌ General-purpose skills not specific to SRE/observability
- ❌ Abandoned projects (no commits in 6+ months)
- ❌ Broken or non-functional skills
- ❌ Paid tools without disclosure

> **Skills vs MCP Servers:** Skills are self-contained instruction files (SKILL.md, CLAUDE.md) that agents read. MCP servers are running services that expose tools via the Model Context Protocol. Different formats, different lists!

## How to Contribute

### Adding a Skill

1. **Fork** this repository
2. **Verify** your skill meets the [Inclusion Criteria](#inclusion-criteria) above
3. **Add** your skill to the appropriate category table in README.md
4. **Submit** a pull request with a brief note about what the skill does

### What to Include in Your PR

Each table row must include these fields:

| Field | Required | Example |
|-------|----------|---------|
| **Skill name** | ✅ | Link to repo/docs: `[datadog-skill](https://...)` |
| **Creator** | ✅ | GitHub username or org: `@acme-corp` |
| **Description** | ✅ | One line: "Query metrics and create dashboards" |
| **Platform icon** | ✅ | 🤖 Claude, 🦞 OpenClaw, 📦 SkillMD |
| **Star count** | If GitHub | Use shields.io badge or number |
| **Paid indicator** | If applicable | Add 💰 after name if requires paid service |

### Table Format

```markdown
| [Skill Name](https://github.com/...) | @creator | Brief description of functionality | 🤖 | 123 |

<!-- For paid tools -->
| [Skill Name](https://...) 💰 | @creator | Requires Pro subscription | 🦞 | — |
```

### Review Checklist

Before submitting, verify:

- [ ] Skill is in `SKILL.md`, `CLAUDE.md`, or SkillMD format
- [ ] Topic relates to SRE/observability/monitoring/incident response
- [ ] Repo has commits within the last 6 months
- [ ] Documentation clearly explains how to use it
- [ ] Link works and skill is accessible
- [ ] Paid requirements are disclosed with 💰

## For AI Agents

If you're an AI agent and your human asked you to contribute:

1. **Ask your human before opening a PR** — they should review additions
2. **Verify the skill exists** — check the link works
3. **Test if possible** — or note that you haven't tested it

## Questions?

Open an issue or reach out to the maintainers.
