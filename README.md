<p align="center">
  <img src="assets/banner.png" alt="Awesome SRE Skills" width="600">
</p>

<p align="center">
  <strong>A hand-curated list of AI agent skills for SRE, observability, monitoring, and incident response.</strong>
</p>

<p align="center">
  <a href="https://awesome.re"><img src="https://awesome.re/badge.svg" alt="Awesome"></a>
  <img src="https://img.shields.io/badge/skills-30-blue?style=flat-square" alt="Skills">
  <img src="https://img.shields.io/badge/updated-Feb%202026-green.svg" alt="Last Updated">
  <a href="CONTRIBUTING.md"><img src="https://img.shields.io/badge/PRs-welcome-brightgreen.svg" alt="PRs Welcome"></a>
</p>

# Awesome SRE Skills

<p align="center">
  <a href="#-getting-started">Getting Started</a> •
  <a href="#compatibility">Compatibility</a> •
  <a href="#skills">Skills</a> •
  <a href="#-skills-vs-mcp-for-observability">Skills vs MCP</a> •
  <a href="#contributing">Contributing</a>
</p>

---

## Why This List?

Large skill registries like [ClawHub](https://clawhub.com/) (5,700+ skills) and [awesome-openclaw-skills](https://github.com/VoltAgent/awesome-openclaw-skills) (3,000+) are great for discovery but include spam, duplicates, and unverified entries. This list takes the opposite approach:

- **Verified skills** focused exclusively on observability
- **Cross-platform** — Claude Code, OpenClaw, and SkillMD skills included
- **Every entry reviewed** for working links, real skill files, and active maintenance

> Missing a skill? [Open an issue](../../issues/new) or submit a PR.

---

## 🚀 Getting Started

### Claude Code CLI

```bash
# Install from GitHub
claude mcp add-skill https://github.com/OWNER/SKILL-REPO

# Or install from local directory  
claude mcp add-skill /path/to/skill-directory
```

### OpenClaw

```bash
# Add skill to your OpenClaw config
openclaw skill add https://github.com/OWNER/SKILL-REPO

# Or copy to your skills directory
cp -r skill-folder ~/.openclaw/skills/
```

## Compatibility

| Platform | Instruction File | Icon |
|----------|-----------------|------|
| Claude Code | `CLAUDE.md` or `commands/*.md` | 🤖 |
| OpenClaw | `SKILL.md` | 🦞 |
| SkillMD | Cross-platform packages | 📦 |

Most skills in this list work with Claude Code. Look for the platform icon to check compatibility.

**Other icons:**
- 🎖️ Official (maintained by vendor)
- ⭐ Popular (50+ GitHub stars at time of addition)

---

## Skills

> [!Warning]
> **Security Notice:** Skills execute code on your machine. We reviewed each skill at the time of addition, but source code can change. **Always** audit the `SKILL.md` or `CLAUDE.md` and any scripts before installing. For ClawHub skills, check the VirusTotal report on the skill's ClawHub page. We also recommend using tools like [Bitdefender AI Skills Checker](https://www.bitdefender.com/en-us/consumer/ai-skills-checker) to verify safety.

### APM & Tracing

*Debug application performance, trace requests across services, analyze AI agent behavior.*

| Skill | Creator | Description | Platform |
|-------|---------|-------------|----------|
| [Datadog Auto-Detector](https://skillsmp.com/skills/schovi-claude-schovi-schovi-skills-datadog-auto-detector-skill-md) | @schovi | Auto-detects Datadog URLs/queries, spawns analyzer subagent for context | 📦 |
| [LangSmith Fetch](https://github.com/OthmanAdi/langsmith-fetch-skill) | @OthmanAdi | Debug LangChain/LangGraph agents via LangSmith traces | 🤖 |
| [Retell AI Observability](https://skillsmp.com/skills/jeremylongshore-claude-code-plugins-plus-skills-plugins-saas-packs-retellai-pack-skills-retellai-observability-skill-md) | @jeremylongshore | Metrics, traces, alerts for Retell AI voice integrations | 📦 |

---

### Logging & Log Analysis

*Search and analyze logs, detect anomalies, correlate events across systems.*

| Skill | Creator | Description | Platform |
|-------|---------|-------------|----------|
| [Datadog CLI Skill](https://mcpmarket.com/tools/skills/datadog-cli) | MCPMarket | Search logs, tail real-time data, correlate traces, analyze error patterns | 📦 |
| [Datadog Debug Workflow](https://github.com/schovi/claude-schovi) | @schovi | Debug command with Datadog analyzer for log/metric/trace correlation | 🤖 |
| [Splunk Assistant Skills](https://github.com/grandcamel/splunk-assistant-skills) | @grandcamel | Splunk REST API automation, search queries, threat hunting | 🤖 |
| [Splunk Alert Management](https://mcpmarket.com/tools/skills/splunk-alert-management) | MCPMarket | Create, monitor, manage Splunk alerts and saved searches | 📦 |
| [DevOps Monitor Commands](https://github.com/rohitg00/awesome-claude-code-toolkit/blob/main/commands/devops/monitor.md) | @rohitg00 | Log analysis, metric queries, dashboard generation | 🤖 |

---

### Metrics & Monitoring

*Query metrics, build dashboards, set up alerting rules, track SLOs.*

| Skill | Creator | Description | Platform |
|-------|---------|-------------|----------|
| [Grafana Skill](https://github.com/julianobarbosa/claude-code-skills/tree/main/skills/grafana-skill) | @julianobarbosa | Grafana HTTP API for dashboards, alerts, data sources, annotations | 🤖 |
| [Prometheus Skill](https://github.com/julianobarbosa/claude-code-skills/tree/main/skills/prometheus-skill) | @julianobarbosa | Query Prometheus HTTP API, execute PromQL, analyze time series | 🤖 |
| [Loki Skill](https://github.com/julianobarbosa/claude-code-skills/tree/main/skills/loki-skill) | @julianobarbosa | Grafana Loki log aggregation, LogQL queries | 🤖 |
| [Mimir Skill](https://github.com/julianobarbosa/claude-code-skills/tree/main/skills/mimir-skill) | @julianobarbosa | Grafana Mimir for long-term Prometheus metrics storage | 🤖 |
| [Tempo Skill](https://github.com/julianobarbosa/claude-code-skills/tree/main/skills/tempo-skill) | @julianobarbosa | Grafana Tempo distributed tracing | 🤖 |
| [Pyroscope Skill](https://github.com/julianobarbosa/claude-code-skills/tree/main/skills/pyroscope-skill) | @julianobarbosa | Continuous profiling with Grafana Pyroscope | 🤖 |
| [Monitoring Expert](https://skillsmp.com/de/skills/jeffallan-claude-skills-skills-monitoring-expert-skill-md) | @Jeffallan | Build monitoring systems (Prometheus, Grafana, Datadog), incident detection | 📦 |
| [Datadog Observability](https://mcpmarket.com/tools/skills/datadog-observability-monitoring) | MCPMarket | Query Datadog logs, metrics, APM traces for monitoring and debugging | 📦 |
| [Monitoring Config Generator](https://openclaw.army/skills/lxgicstudios/monitoring-config-generator/) | lxgicstudios | Generate Prometheus alert rules + Grafana dashboards | 🦞 |
| [Production Monitoring](https://skillmd.ai/how-to-build/production-monitoring/) | SkillMD | Daily health checks, container status, error scanning | 📦 |
| [Uptime Kuma](https://openclaw.army/skills/msarheed/uptime-kuma/) | @msarheed | Manage uptime monitors, heartbeats, pause/resume endpoints | 🦞 |
| [DevOps Claude Skills](https://github.com/ahmedasmar/devops-claude-skills) ⭐ | @ahmedasmar | 6 scripts: metrics analysis, SLO calculation, log analysis, dashboards | 🤖 |

---

### Incident Response & Alerting

*Triage incidents, execute runbooks, classify severity, generate postmortems.*

| Skill | Creator | Description | Platform |
|-------|---------|-------------|----------|
| [PagerDuty Automation](https://github.com/ComposioHQ/awesome-claude-skills/tree/master/pagerduty-automation) | ComposioHQ | Full PagerDuty workflow: incidents, schedules, escalation policies, on-call rotations | 🤖 |
| [Incident Triage](https://skillmd.ai/how-to-build/incident-triage-1/) | SkillMD | SEV classification, first 5-15 min response framework | 📦 |
| [On-Call Playbooks](https://skillmd.ai/how-to-build/on-call-playbooks/) | SkillMD | Comprehensive runbooks for common incidents | 📦 |
| [IT Operations](https://skillsmp.com/es/skills/davila7-claude-code-templates-cli-tool-components-skills-development-it-operations-skill-md) | @davila7 | ITIL service management, observability strategies, incident response | 📦 |

---

### Infrastructure & Cloud

*Kubernetes troubleshooting, cloud platform operations, DevOps toolkits.*

| Skill | Creator | Description | Platform |
|-------|---------|-------------|----------|
| [HolmesGPT Skill](https://github.com/julianobarbosa/claude-code-skills/tree/main/skills/holmesgpt-skill) | @julianobarbosa | Investigate K8s issues, analyze alerts, troubleshoot cloud-native apps | 🤖 |
| [Microsoft Azure Skills](https://github.com/microsoft/skills) 🎖️ ⭐⭐ | Microsoft | Azure SDKs, AI Foundry integration, cloud resource management | 🤖 |
| [AWS Cost & Operations](https://clawhub.com/) | @zxkane | CloudWatch metrics, Cost Explorer, Well-Architected reviews | 🤖 |
| [Cloudflare Troubleshooting](https://github.com/daymade/claude-code-skills) ⭐⭐ | @daymade | Diagnose Cloudflare issues (SSL, DNS, redirects, caching) | 🤖 |
| [ServiceNow Agent](https://openclaw.army/skills/thesethrose/servicenow-agent/) | @thesethrose | Read-only queries to ServiceNow ITSM (tables, CMDB, incidents) | 🦞 |
| [DevOps Skills](https://github.com/lgbarn/devops-skills) | @lgbarn | Terraform/OpenTofu workflows, AWS infrastructure, safety-first IaC | 🤖 |

---

### Security & Compliance

*Threat detection, vulnerability scanning, credential leak prevention, audit trails.*

| Skill | Creator | Description | Platform |
|-------|---------|-------------|----------|
| [ClawSec](https://github.com/prompt-security/clawsec) ⭐⭐ | Prompt Security | Security skill suite: prompt injection, supply chain, credential leak detection | 🦞 |
| [Skill Guard](https://github.com/UseAI-pro/openclaw-skills-security) | UseAI-pro | Monitor skill behavior, flag permission violations, sandbox unsafe actions | 🦞 |
| [Trail of Bits Security Skills](https://github.com/trailofbits/skills) ⭐⭐ | Trail of Bits | Security research, vulnerability detection, audit workflows (fix review, variant analysis) | 🤖 |

---

## Skill Registries

| Registry | Skills | Notes |
|----------|--------|-------|
| [awesome-claude-skills](https://github.com/ComposioHQ/awesome-claude-skills) ⭐⭐ | 1000+ | ComposioHQ curated list |
| [awesome-openclaw-skills](https://github.com/VoltAgent/awesome-openclaw-skills) ⭐⭐ | 3000+ | VoltAgent curated list |
| [SkillsMP](https://skillsmp.com) | 160,000+ | Cross-platform marketplace |
| [ClawHub](https://github.com/openclaw/clawhub) ⭐⭐ | varies | OpenClaw official registry |
| [Anthropic Skills](https://github.com/anthropics/skills) 🎖️ ⭐⭐ | ~50 | Official reference implementations |
| [agent-skills.md](https://agent-skills.md/) | varies | Skill discovery site |

---

## 💡 Skills vs MCP for Observability

| Aspect | Skills | MCP Servers |
|--------|--------|-------------|
| **Purpose** | Procedural workflows, runbooks, analysis patterns | Data access, API integration |
| **Best for** | Incident triage, postmortem generation, alert analysis | Querying metrics, fetching logs, dashboard creation |
| **Examples** | "Analyze this error and suggest fixes" | "Get CPU metrics for the last hour" |
| **Execution** | Instructions + optional scripts | Running server process |
| **Portability** | Copy SKILL.md anywhere | Requires server setup |

**Use Skills when:** You need Claude to follow a specific workflow OR access live data via scripts — like triaging incidents, querying APIs, or generating reports.

**Use MCP when:** You want a standardized protocol for data access — MCP provides a consistent interface across different tools and data sources.

**Use both:** Skills can orchestrate MCP calls. For example, an "incident investigation" skill might use a Datadog MCP to fetch relevant logs, or call APIs directly via shell scripts.

> Looking for MCP servers? See [awesome-devops-mcp-servers](https://github.com/rohitg00/awesome-devops-mcp-servers)

---

## Resources

### Related Lists

- [awesome-devops-mcp-servers](https://github.com/rohitg00/awesome-devops-mcp-servers) — DevOps MCP servers with observability tools
- [awesome-mcp-servers](https://github.com/punkpeye/awesome-mcp-servers) ⭐⭐ — General MCP servers
- [awesome-observability](https://github.com/adriannovegil/awesome-observability) ⭐⭐ — General observability tools
- [awesome-sre](https://github.com/dastergon/awesome-sre) ⭐⭐ — Site Reliability Engineering resources

### Skill Development

- [Agent Skills Spec](https://github.com/agentskills/agentskills) ⭐⭐ — Open standard for portable skills
- [Claude Code Skills Guide](https://docs.anthropic.com/en/docs/claude-code/skills) — Official Anthropic docs

### Security Research

- [Bitdefender AI Skills Checker](https://www.bitdefender.com/en-us/consumer/ai-skills-checker) — Verify OpenClaw skill safety
- [1Password: OpenClaw Attack Surface](https://1password.com/blog/from-magic-to-malware-how-openclaws-agent-skills-become-an-attack-surface) — Security research on malicious skills

---

## ❓ FAQ

<details>
<summary><strong>How do observability skills differ from MCP servers?</strong></summary>

Skills teach Claude *how* to do something (workflows, analysis patterns). MCPs give Claude *access* to something (APIs, databases). For observability: use skills for incident runbooks and analysis workflows; use MCPs to query your actual monitoring data.

</details>

<details>
<summary><strong>Can I use these skills with my existing monitoring stack?</strong></summary>

Yes! Most skills are stack-agnostic — they teach patterns and workflows. Some skills are platform-specific (e.g., Datadog, Grafana) and require access to those platforms. Check each skill's documentation for prerequisites.

</details>

<details>
<summary><strong>How do I create a custom observability skill?</strong></summary>

1. Create a folder with a `SKILL.md` (OpenClaw) or `CLAUDE.md` (Claude Code)
2. Write instructions for your workflow (e.g., "How to triage a P1 incident")
3. Optionally add scripts for automation
4. Test locally, then share via GitHub

See [Creating Skills](#creating-skills) in the official docs.

</details>

<details>
<summary><strong>Do skills work with all Claude models?</strong></summary>

Skills work with Claude Pro, Max, Team, and Enterprise. Free tier users don't have access to Skills. For API usage, check the [Skills API documentation](https://docs.anthropic.com).

</details>

<details>
<summary><strong>Why are some links marked with different icons?</strong></summary>

- 🤖 = Claude Code compatible (CLAUDE.md format)
- 🦞 = OpenClaw compatible (SKILL.md format)  
- 📦 = SkillMD cross-platform package
- 🎖️ = Official/vendor-maintained

</details>

---

## Contributing

Contributions welcome! Please read the [contribution guidelines](CONTRIBUTING.md) first.

### Adding a Skill

1. Fork this repo
2. Add your skill to the appropriate **use case category**:
   - **APM & Tracing** — Performance monitoring, distributed tracing
   - **Logging & Log Analysis** — Log search, pattern detection
   - **Metrics & Monitoring** — Dashboards, alerting rules, SLOs
   - **Incident Response & Alerting** — Triage, runbooks, postmortems
   - **Infrastructure & Cloud** — K8s, cloud platforms, DevOps
   - **Security & Compliance** — Threat detection, vulnerability scanning
3. Include: Name (with link), creator, description, platform icon, star count
4. Mark official skills with 🎖️
5. Submit a PR

### Criteria

- Must be an agent skill (CLAUDE.md, SKILL.md, or SkillMD format) — **NOT** MCP servers
- Must relate to observability, monitoring, or incident response
- Should have documentation and be actively maintained

> **Note:** MCP servers belong in [awesome-devops-mcp-servers](https://github.com/rohitg00/awesome-devops-mcp-servers)

---

## License

[![CC0](https://licensebuttons.net/p/zero/1.0/88x31.png)](https://creativecommons.org/publicdomain/zero/1.0/)

---

<p align="center">
  <em>Last verified: 2026-02-13</em>
</p>
