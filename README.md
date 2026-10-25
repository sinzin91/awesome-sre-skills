# Awesome SRE Skills [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

<p align="center">
  <img src="assets/banner.png" alt="Awesome SRE Skills" width="600">
</p>

<p align="center">
  <strong>A hand-curated list of AI agent skills for SRE, observability, monitoring, and incident response.</strong>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/skills-86-blue?style=flat-square" alt="Skills">
  <img src="https://img.shields.io/badge/updated-Oct%202026-green.svg" alt="Last Updated">
  <a href="CONTRIBUTING.md"><img src="https://img.shields.io/badge/PRs-welcome-brightgreen.svg" alt="PRs Welcome"></a>
</p>

<p align="center">
  <a href="#-getting-started">Getting Started</a> •
  <a href="#compatibility">Compatibility</a> •
  <a href="#skills">Skills</a> •
  <a href="#-skills-vs-mcp-for-sre">Skills vs MCP</a> •
  <a href="#contributing">Contributing</a>
</p>

---

## Why This List

Large skill registries like ClawHub (80,000+ skills) and awesome-openclaw-skills (5,300+) are great for discovery but can be noisy. This list focuses on SRE, observability, and incident response skills across platforms (Claude Code, OpenClaw, and SkillMD).

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

| Platform    | Instruction File                                                        | Icon |
| ----------- | ----------------------------------------------------------------------- | ---- |
| Claude Code | Plugin, `SKILL.md`, `CLAUDE.md` or `commands/*.md`                      | 🤖   |
| OpenClaw    | Skills built for OpenClaw (ClawHub-hosted, or targeting OpenClaw first) | 🦞   |
| SkillMD     | Packages hosted on [skillmd.ai](https://skillmd.ai/)                    | 📦   |

Each entry's icon shows its **primary** platform, meaning the agent it's packaged or built for. Compatibility is wider than that: a standard `SKILL.md` follows the open Agent Skills format, so most 🤖 and 🦞 skills work in both Claude Code and OpenClaw. Check the skill's README for the agents it supports.

**Other icons:**
- 🎖️ Official (maintained by vendor)
- ⭐ Popular (50+ GitHub stars at time of addition)
- ⭐⭐ Very popular (1000+ GitHub stars at time of addition)
- 💰 = Requires a paid service (no usable free tier)

---

## Skills

> [!Warning]
> **Security Notice:** Skills execute code on your machine. Source code can change at any time. **Always** audit the `SKILL.md` or `CLAUDE.md` and any scripts before installing. For ClawHub skills, check the VirusTotal report on the skill's ClawHub page. We also recommend using tools like Bitdefender AI Skills Checker (see Security Research below) to verify safety.

### APM & Tracing

*Debug application performance, trace requests across services, analyze AI agent behavior.*

| Skill                                                                                                                                                                | Creator          | Description                                                                                 | Platform |
| -------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------- | ------------------------------------------------------------------------------------------- | -------- |
| [Datadog Auto-Detector](https://github.com/schovi/claude-schovi/tree/main/plugins/schovi/skills/datadog-auto-detector)                                               | @schovi          | Auto-detects Datadog URLs/queries, spawns analyzer subagent for context                     | 🤖       |
| [Retell AI Observability](https://github.com/jeremylongshore/tons-of-skills-marketplace/tree/main/plugins/saas-packs/retellai-pack/skills/retellai-observability) 💰 | @jeremylongshore | Metrics, traces, alerts for Retell AI voice integrations                                    | 🤖       |
| [Honeycomb Agent Skills](https://github.com/honeycombio/agent-skill) 🎖️                                                                                             | @honeycombio     | Official Honeycomb skills: querying, SLOs/triggers, OTel instrumentation, prod-debug agents | 🤖       |
| [Langfuse Skills](https://github.com/langfuse/skills) 🎖️ ⭐                                                                                                          | @langfuse        | Query/manage Langfuse traces, prompts, datasets & scores for LLM-app observability          | 🤖       |
| [LangSmith Skills](https://github.com/langchain-ai/langsmith-skills) 🎖️ ⭐                                                                                           | @langchain-ai    | Query LLM traces, build eval datasets & custom evaluators in LangSmith                      | 🤖       |
| [Datadog Agent Skills](https://github.com/datadog-labs/agent-skills) 🎖️ ⭐                                                                                           | Datadog          | APM/trace analysis and LLM-app observability (RCA, eval, session tracing)                   | 🤖       |
| [Elastic Agent Skills](https://github.com/elastic/agent-skills) 🎖️ ⭐                                                                                                | Elastic          | Observability skills: EDOT/OTel, APM, SLOs, Kubernetes investigation, ES&#124;QL log search | 🤖       |
| [Sentry for AI](https://github.com/getsentry/sentry-for-ai/tree/main/src/skills) 🎖️ ⭐                                                                               | Sentry           | Fix issues from stack traces, set up SDKs, alerts and the OTel exporter                     | 🤖       |
| [Dynatrace for AI](https://github.com/Dynatrace/dynatrace-for-ai/tree/main/skills) 💰 🎖️ ⭐                                                                          | Dynatrace        | DQL, problem/RCA, logs, traces, Kubernetes & cloud observability skills                     | 🤖       |
| [Dash0 Agent Skills](https://github.com/dash0hq/agent-skills/tree/main/skills) 🎖️ ⭐                                                                                 | Dash0            | Vendor-neutral OTel instrumentation, Collector config, OTTL & semantic conventions          | 🤖       |
| [SigNoz Agent Skills](https://github.com/SigNoz/agent-skills/tree/main/plugins/signoz/skills) 🎖️                                                                    | SigNoz           | Query SigNoz telemetry, investigate alerts, build dashboards, cut telemetry cost            | 🤖       |
| [New Relic Skills Hub](https://github.com/newrelic/nr-skills-hub/tree/main/skills) 🎖️                                                                               | New Relic        | Read-only NRQL generation, trace discovery & APM error root-cause analysis                  | 🤖       |
| [Last9 AI Toolkit](https://github.com/last9/ai-toolkit/tree/master/skills) 🎖️                                                                                       | Last9            | Guided trace and log investigation plus CloudWatch queries via Last9                        | 🤖       |
| [Logfire Skills](https://github.com/pydantic/skills/tree/main/plugins/logfire) 🎖️ ⭐                                                                                 | Pydantic         | Instrument apps with Logfire and query traces, logs & metrics                               | 🤖       |
| [OpenTelemetry Agent Skills](https://github.com/ollygarden/opentelemetry-agent-skills/tree/main/skills) ⭐                                                            | @ollygarden      | 20 OTel skills: SDKs in 7 languages, Collector, OTTL, Weaver & semconv                      | 🤖       |
| [OpenTelemetry Skill](https://github.com/o11y-dev/opentelemetry-skill/blob/main/SKILL.md) ⭐                                                                          | @o11y-dev        | Collector configs, OTTL, sampling, cardinality & debugging missing signals                  | 🤖       |
| [Oddyssey](https://github.com/using-system/oddyssey/tree/main/marketplace/oddyssey)                                                                                  | @using-system    | Observability-driven development: OTel instrumentation, local stack, k6 load tests          | 🤖       |
| [LLM Observability Skills](https://github.com/ContextJet-ai/awesome-llm-observability/tree/main/skills)                                                              | @ContextJet-ai   | Debug agents from traces, drift alerts & GenAI span validation                              | 🤖       |
| [Go Observability](https://github.com/samber/cc-skills-golang/tree/main/skills/golang-observability) ⭐⭐                                                              | @samber          | Go logging, metrics & tracing best practices (slog, Prometheus, OTel)                       | 🤖       |

---

### Logging & Log Analysis

*Search and analyze logs, detect anomalies, correlate events across systems.*

| Skill                                                                                                                    | Creator             | Description                                                                              | Platform |
| ------------------------------------------------------------------------------------------------------------------------ | ------------------- | ---------------------------------------------------------------------------------------- | -------- |
| [Datadog CLI Skill](https://github.com/DataDog/pup) 🎖️ ⭐                                                                | Datadog             | Official Datadog `pup` CLI + skills: `/sre-investigate` for log/trace/metric correlation | 🤖       |
| [Datadog Debug Workflow](https://github.com/schovi/claude-schovi)                                                        | @schovi             | Debug command with Datadog analyzer for log/metric/trace correlation                     | 🤖       |
| [DevOps Monitor Commands](https://github.com/rohitg00/awesome-claude-code-toolkit/blob/main/commands/devops/monitor.md)  | @rohitg00           | Monitoring-setup playbook: Prometheus/Grafana/Datadog config, alert rules, OTel tracing  | 🤖       |
| [Coralogix cx-cli Skills](https://github.com/coralogix/cx-cli/tree/master/skills) 💰 🎖️ ⭐                               | Coralogix           | Official skills to query logs, spans, metrics, RUM, alerts & SLOs via the cx CLI         | 🤖       |
| [OpenSearch Agent Skills](https://github.com/opensearch-project/opensearch-agent-skills) 🎖️                             | @opensearch-project | Log & trace analytics with PPL queries, error and trace investigation                    | 🤖       |
| [kstack](https://github.com/kubetail-org/kstack) ⭐                                                                       | @kubetail-org       | Kubernetes log/metrics investigation + security/cost/network audits via slash commands   | 🤖       |
| [Splunk Agent Skills](https://github.com/splunk/splunk-agent-skills/tree/main/skills) 🎖️ ⭐                              | Splunk              | 32 skills: SPL search, alerting, ingest doctor, cluster health, incident diagnosis       | 🤖       |
| [ClickStack OTel Collector](https://github.com/ClickHouse/agent-skills/tree/main/skills/clickstack-otel-collector) 🎖️ ⭐ | ClickHouse          | Wire an OTel Collector into ClickStack (HyperDX) for logs, traces & metrics              | 🤖       |

---

### Metrics & Monitoring

*Query metrics, build dashboards, set up alerting rules, track SLOs.*

| Skill                                                                                                                   | Creator         | Description                                                                               | Platform |
| ----------------------------------------------------------------------------------------------------------------------- | --------------- | ----------------------------------------------------------------------------------------- | -------- |
| [Grafana Skill](https://github.com/julianobarbosa/claude-code-skills/tree/main/skills/grafana)                          | @julianobarbosa | Grafana HTTP API for dashboards, alerts, data sources, annotations                        | 🤖       |
| [Prometheus Skill](https://github.com/julianobarbosa/claude-code-skills/tree/main/skills/prometheus)                    | @julianobarbosa | Query Prometheus HTTP API, execute PromQL, analyze time series                            | 🤖       |
| [Loki Skill](https://github.com/julianobarbosa/claude-code-skills/tree/main/skills/loki)                                | @julianobarbosa | Grafana Loki log aggregation, LogQL queries                                               | 🤖       |
| [Mimir Skill](https://github.com/julianobarbosa/claude-code-skills/tree/main/skills/mimir)                              | @julianobarbosa | Grafana Mimir for long-term Prometheus metrics storage                                    | 🤖       |
| [Tempo Skill](https://github.com/julianobarbosa/claude-code-skills/tree/main/skills/tempo)                              | @julianobarbosa | Grafana Tempo distributed tracing                                                         | 🤖       |
| [Pyroscope Skill](https://github.com/julianobarbosa/claude-code-skills/tree/main/skills/pyroscope)                      | @julianobarbosa | Continuous profiling with Grafana Pyroscope                                               | 🤖       |
| [Monitoring Expert](https://github.com/Jeffallan/claude-skills/tree/main/skills/monitoring-expert) ⭐⭐                   | @Jeffallan      | Build monitoring systems (Prometheus, Grafana, Datadog), incident detection               | 🤖       |
| [Production Monitoring](https://skillmd.ai/how-to-build/production-monitoring/)                                         | SkillMD         | Daily health checks, container status, error scanning                                     | 📦       |
| [Uptime Kuma](https://clawhub.ai/msarheed/skills/uptime-kuma)                                                           | @msarheed       | Manage uptime monitors, heartbeats, pause/resume endpoints                                | 🦞       |
| [Grafana Skills](https://github.com/grafana/skills) 🎖️ ⭐                                                               | @grafana        | 44 official skills for Grafana, PromQL, Loki, Tempo, Mimir, Pyroscope, k6 & on-call/IRM   | 🤖       |
| [Checkly Skill](https://github.com/checkly/checkly-cli/tree/main/skills/checkly) 🎖️ ⭐                                  | Checkly         | Synthetic & uptime monitoring-as-code: API/browser/multistep checks, alerts, status pages | 🤖       |
| [Observability & Monitoring Plugin](https://github.com/wshobson/agents/tree/main/plugins/observability-monitoring) ⭐⭐   | @wshobson       | Prometheus config, Grafana dashboards (RED/USE), SLO implementation & distributed tracing | 🤖       |
| [gcx Claude Plugin](https://github.com/grafana/gcx/tree/main/claude-plugin/skills) 🎖️ ⭐                                | @grafana        | Grafana CLI skills: alert investigation, on-call triage, SLOs, synthetics, dashboards     | 🤖       |
| [VictoriaMetrics Skills](https://github.com/VictoriaMetrics/skills/tree/main/plugins) 🎖️ ⭐                             | VictoriaMetrics | MetricsQL/LogsQL/trace queries, cardinality analysis, diagnostics & vmanomaly             | 🤖       |
| [Netdata Skills](https://github.com/netdata/skills/tree/master/skills) 🎖️                                              | Netdata         | Collector config, alert migration & troubleshooting playbooks for 50+ services            | 🤖       |
| [Google Cloud Skills](https://github.com/google/skills/tree/main/skills/cloud) 🎖️ ⭐⭐                                   | Google          | Cloud Logging/Monitoring/Trace queries, SLO alerts & GKE troubleshooting                  | 🤖       |
| [AWS Observability](https://github.com/aws/agent-toolkit-for-aws/tree/main/skills/core-skills/aws-observability) 🎖️ ⭐⭐ | AWS             | CloudWatch Logs Insights, alarms, X-Ray/ADOT & Application Signals                        | 🤖       |
| [promql-cli](https://github.com/samber/cc-skills/tree/main/skills/promql-cli) ⭐                                         | @samber         | Run PromQL against Prometheus, Thanos, Mimir & VictoriaMetrics                            | 🤖       |

---

### Incident Response & Alerting

*Triage incidents, execute runbooks, classify severity, generate postmortems.*

| Skill                                                                                                                                       | Creator       | Description                                                                          | Platform |
| ------------------------------------------------------------------------------------------------------------------------------------------- | ------------- | ------------------------------------------------------------------------------------ | -------- |
| [Incident Triage](https://skillmd.ai/how-to-build/incident-triage-1/)                                                                       | SkillMD       | SEV classification, first 5-15 min response framework                                | 📦       |
| [On-Call Playbooks](https://skillmd.ai/how-to-build/on-call-playbooks/)                                                                     | SkillMD       | Comprehensive runbooks for common incidents                                          | 📦       |
| [Incident Response (Anthropic)](https://github.com/anthropics/knowledge-work-plugins/tree/main/engineering/skills/incident-response) 🎖️ ⭐⭐ | Anthropic     | Incident triage (SEV1-4), status comms & blameless postmortems with 5-whys RCA       | 🤖       |
| [PagerDuty Claude Code Plugins](https://github.com/PagerDuty/claude-code-plugins) 🎖️                                                       | PagerDuty     | Official PagerDuty plugins: commit-risk scoring from incident history, skill-builder | 🤖       |
| [Axiom SRE](https://github.com/axiomhq/skills/tree/main/skills/sre) 🎖️                                                                     | @axiomhq      | Official Axiom skill: query logs/metrics & investigate incidents via APL             | 🤖       |
| [Incident Commander](https://github.com/borghei/Claude-Skills/blob/main/engineering/incident-commander/SKILL.md) ⭐                          | @borghei      | SEV scoring, timeline reconstruction & postmortem/RCA generation                     | 🤖       |
| [Incident Response Plugin](https://github.com/wshobson/agents/tree/main/plugins/incident-response) ⭐⭐                                       | @wshobson     | Postmortem writing and on-call handoff patterns                                      | 🤖       |
| [Claude Tabletop](https://github.com/cjcsecurity/claude-tabletop)                                                                           | @cjcsecurity  | Generate project-aware IR tabletop exercises, facilitator runbook & AAR              | 🤖       |
| [incident.io Skills](https://github.com/incident-io/skills/tree/main/plugins/incident-io/skills) 💰 🎖️                                     | incident.io   | Declare and update incidents, manage roles, on-call & postmortems                    | 🤖       |
| [Better Stack Plugin](https://github.com/BetterStackHQ/claude-plugin/tree/main/skills) 🎖️                                                  | Better Stack  | Incident investigation across on-call, uptime monitors, logs, metrics & traces       | 🤖       |
| [Oncall Kit](https://github.com/anthropics/oncall-kit) 🎖️ ⭐                                                                                | Anthropic     | Mine incident history into triage playbooks; read-only on-call help in Slack         | 🤖       |
| [AWS DevOps Agent Plugin](https://github.com/aws/agent-toolkit-for-aws/tree/main/plugins/aws-agents-for-devsecops) 💰 🎖️ ⭐⭐                | AWS           | Investigate incidents & analyze release readiness via AWS DevOps Agent               | 🤖       |
| [Rootly Plugin](https://github.com/Rootly-AI-Labs/rootly-claude-plugin/tree/main/skills) 💰 🎖️                                             | Rootly        | Incident response, handoff, on-call swap & retro workflows (experimental)            | 🤖       |
| [SRE-Skills](https://github.com/kryptophonik/SRE-Skills/tree/main/.claude/skills)                                                           | @kryptophonik | 41 SRE skills with approval gates: triage, incident command, burn-rate alerts        | 🤖       |
| [Writing Postmortems](https://github.com/riekelt/technical-writer/tree/main/plugins/technical-writer/skills/writing-postmortems)            | @riekelt      | Blameless postmortem and RCA write-ups                                               | 🤖       |

---

### Reliability & Chaos Engineering

*Define SLOs and error budgets, run chaos experiments, and validate resilience before failures hit prod.*

| Skill                                                                                                                              | Creator         | Description                                                                                | Platform |
| ---------------------------------------------------------------------------------------------------------------------------------- | --------------- | ------------------------------------------------------------------------------------------ | -------- |
| [AWS Resilience Skills](https://github.com/aws-samples/sample-aws-resilience-skill) 🎖️                                            | AWS             | Resilience maturity/modeling, chaos engineering (FIS), EKS checks, Well-Architected review | 🤖       |
| [Chaos Engineering](https://github.com/borghei/Claude-Skills/blob/main/engineering/chaos-engineering/SKILL.md) ⭐                   | @borghei        | Design & run fault-injection experiments with hypotheses and blast-radius control          | 🤖       |
| [SLO Architect](https://github.com/alirezarezvani/claude-skills/tree/main/engineering/skills/slo-architect) ⭐⭐                     | @alirezarezvani | Define SLIs/SLOs, error budgets & multi-window burn-rate alerts                            | 🤖       |
| [SRE Practice Skills](https://github.com/paulip114/sre-practice-skills) ⭐                                                          | @paulip114      | 8 skills from the Google SRE books: SLOs, error budgets, postmortems, toil                 | 🤖       |
| [Site Reliability Engineering](https://github.com/magnus919/agent-skills/tree/main/site-reliability-engineering) ⭐                 | @magnus919      | SLO, error-budget and incident-command practices                                           | 🤖       |
| [Harness Observability & Governance](https://github.com/harness/harness-skills/tree/main/skills/observability-governance) 💰 🎖️ ⭐ | Harness         | Chaos experiments, DR tests, SLOs, incident response & DORA metrics                        | 🤖       |
| [Well-Architected Skills](https://github.com/aws-samples/sample-well-architected-skills-and-steering) 🎖️ ⭐                        | AWS             | Well-Architected reviews, including reliability-pillar improvement plans                   | 🤖       |
| [EKS Operation Review](https://github.com/aws-samples/sample-eks-operation-review-skill) 🎖️                                       | AWS             | Read-only operational-readiness assessment of a live EKS cluster                           | 🤖       |

---

### Infrastructure & Cloud

*Kubernetes troubleshooting, cloud platform operations, DevOps toolkits.*

| Skill                                                                                                                                 | Creator         | Description                                                                              | Platform |
| ------------------------------------------------------------------------------------------------------------------------------------- | --------------- | ---------------------------------------------------------------------------------------- | -------- |
| [HolmesGPT Skill](https://github.com/julianobarbosa/claude-code-skills/tree/main/skills/holmesgpt)                                    | @julianobarbosa | Investigate Kubernetes issues, analyze alerts, troubleshoot cloud-native apps            | 🤖       |
| [Microsoft Azure Skills](https://github.com/microsoft/skills) 🎖️ ⭐⭐                                                                  | Microsoft       | Azure SDKs, AI Foundry integration, cloud resource management                            | 🤖       |
| [AWS Cost & Operations](https://github.com/zxkane/aws-skills/tree/main/plugins/aws-cost-ops) ⭐                                        | @zxkane         | CloudWatch metrics, Cost Explorer, Well-Architected reviews                              | 🤖       |
| [Cloudflare Troubleshooting](https://github.com/daymade/claude-code-skills) ⭐⭐                                                        | @daymade        | Diagnose Cloudflare issues (SSL, DNS, redirects, caching)                                | 🤖       |
| [ServiceNow Agent](https://clawhub.ai/thesethrose/skills/servicenow-agent)                                                            | @thesethrose    | Read-only queries to ServiceNow ITSM (tables, CMDB, incidents)                           | 🦞       |
| [Kubernetes Skill](https://github.com/LukasNiessen/kubernetes-skill) ⭐                                                                | @LukasNiessen   | Grounds agents in official Kubernetes/Helm/Kustomize best practices & security hardening | 🤖       |
| [Flux CD Agent Skills](https://github.com/fluxcd/agent-skills) 🎖️ ⭐                                                                  | @fluxcd         | Debug live Flux/Kubernetes GitOps clusters, audit repo readiness, generate manifests     | 🤖       |
| [Terraform Skill](https://github.com/antonbabenko/terraform-skill) ⭐⭐                                                                 | @antonbabenko   | Terraform/OpenTofu best practices: testing, modules, state, CI/CD, security scanning     | 🤖       |
| [Neon PostgreSQL Skills](https://github.com/neondatabase/postgres-skills) 🎖️                                                         | @neondatabase   | PostgreSQL reliability best practices: performance, HA and operational tuning            | 🤖       |
| [Platform Skills](https://github.com/nitinjain999/platform-skills/tree/main/plugins/platform-skills/skills) ⭐                         | @nitinjain999   | Platform/SRE handbook: Kubernetes, Flux, chaos, DORA, cluster upgrades & DR              | 🤖       |
| [APEX EKS/ECS Skills](https://github.com/aws-samples/sample-apex-skills/tree/main/skills) 🎖️ ⭐                                       | AWS             | EKS/ECS operations reviews, upgrade checks, observability & cost                         | 🤖       |
| [Azure Diagnostics](https://github.com/microsoft/azure-skills/tree/main/.github/plugins/azure-skills/skills/azure-diagnostics) 🎖️ ⭐⭐ | Microsoft       | Debug Azure production issues with AppLens & Azure Monitor                               | 🤖       |
| [Azure SRE Agent Skills](https://github.com/ricmmartins/azure-sre-agent-skills/tree/main/skills) 💰 ⭐                                 | @ricmmartins    | WAF review, FinOps, capacity planning & postmortems for Azure SRE Agent                  | 🤖       |
| [VMware AIops](https://github.com/vmware-skills/VMware-AIops/tree/main/skills/vmware-aiops) 💰 ⭐                                      | @vmware-skills  | vCenter/ESXi VM operations and alarm triage                                              | 🤖       |
| [Anyshift SRE Skills](https://github.com/anyshift-io/sre-skills/tree/main/skills)                                                     | @anyshift-io    | kubectl investigation plus IAM, security-group, S3 & SQS auditors                        | 🤖       |

---

### Security & Compliance

*Threat detection, vulnerability scanning, credential leak prevention, audit trails.*

| Skill                                                                     | Creator         | Description                                                                                | Platform |
| ------------------------------------------------------------------------- | --------------- | ------------------------------------------------------------------------------------------ | -------- |
| [ClawSec](https://github.com/prompt-security/clawsec) ⭐⭐                  | Prompt Security | Security skill suite: prompt injection, supply chain, credential leak detection            | 🦞       |
| [Trail of Bits Security Skills](https://github.com/trailofbits/skills) ⭐⭐ | Trail of Bits   | Security research, vulnerability detection, audit workflows (fix review, variant analysis) | 🤖       |
| [CrowdSec Skill](https://github.com/crowdsecurity/crowdsec-skill) 🎖️     | CrowdSec        | Install, configure, operate & debug CrowdSec intrusion prevention                          | 🤖       |

---

## Skill Registries

| Registry                                                                           | Skills              | Notes                              |
| ---------------------------------------------------------------------------------- | ------------------- | ---------------------------------- |
| [awesome-claude-skills](https://github.com/ComposioHQ/awesome-claude-skills) ⭐⭐    | 170+                | ComposioHQ curated list            |
| [awesome-openclaw-skills](https://github.com/VoltAgent/awesome-openclaw-skills) ⭐⭐ | 5,300+              | VoltAgent curated list             |
| [SkillsMP](https://skillsmp.com)                                                   | 3M+ (self-reported) | Cross-platform marketplace         |
| [ClawHub](https://clawhub.ai/)                                                     | 80,000+             | OpenClaw official registry         |
| [Anthropic Skills](https://github.com/anthropics/skills) 🎖️ ⭐⭐                    | ~19                 | Official reference implementations |
| [agent-skills.md](https://agent-skills.md/)                                        | varies              | Skill discovery site               |

---

## 💡 Skills vs MCP for SRE

| Aspect          | Skills                                                 | MCP Servers                                         |
| --------------- | ------------------------------------------------------ | --------------------------------------------------- |
| **Purpose**     | Procedural workflows, runbooks, analysis patterns      | Data access, API integration                        |
| **Best for**    | Incident triage, postmortem generation, alert analysis | Querying metrics, fetching logs, dashboard creation |
| **Examples**    | "Analyze this error and suggest fixes"                 | "Get CPU metrics for the last hour"                 |
| **Execution**   | Instructions + optional scripts                        | Running server process                              |
| **Portability** | Copy SKILL.md anywhere                                 | Requires server setup                               |

**Use Skills when:** You need Claude to follow a specific workflow OR access live data via scripts - like triaging incidents, querying APIs, or generating reports.

**Use MCP when:** You want a standardized protocol for data access - MCP provides a consistent interface across different tools and data sources.

**Use both:** Skills can orchestrate MCP calls. For example, an "incident investigation" skill might use a Datadog MCP to fetch relevant logs, or call APIs directly via shell scripts.

> Looking for MCP servers? See awesome-devops-mcp-servers in Related Lists below

---

## Resources

### Related Lists

- [awesome-devops-mcp-servers](https://github.com/rohitg00/awesome-devops-mcp-servers) - DevOps MCP servers with observability tools.
- [awesome-mcp-servers](https://github.com/punkpeye/awesome-mcp-servers) ⭐⭐ - General MCP servers
- [awesome-observability](https://github.com/adriannovegil/awesome-observability) ⭐⭐ - General observability tools
- [awesome-sre](https://github.com/dastergon/awesome-sre) ⭐⭐ - Site Reliability Engineering resources

### Skill Development

- [Agent Skills Spec](https://github.com/agentskills/agentskills) ⭐⭐ - Open standard for portable skills
- [Claude Code Skills Guide](https://code.claude.com/docs/en/skills) - Official Anthropic docs.

### Security Research

- [Bitdefender AI Skills Checker](https://www.bitdefender.com/en-us/consumer/ai-skills-checker) - Verify OpenClaw skill safety.
- [1Password: OpenClaw Attack Surface](https://1password.com/blog/from-magic-to-malware-how-openclaws-agent-skills-become-an-attack-surface) - Security research on malicious skills.

---

## ❓ FAQ

<details>
<summary><strong>How do SRE skills differ from MCP servers?</strong></summary>

Skills teach Claude *how* to do something (workflows, analysis patterns). MCPs give Claude *access* to something (APIs, databases). For SRE: use skills for incident runbooks and analysis workflows; use MCPs to query your actual monitoring data.

</details>

<details>
<summary><strong>Can I use these skills with my existing monitoring stack?</strong></summary>

Yes! Most skills are stack-agnostic - they teach patterns and workflows. Some skills are platform-specific (e.g., Datadog, Grafana) and require access to those platforms. Check each skill's documentation for prerequisites.

</details>

<details>
<summary><strong>How do I create a custom SRE skill?</strong></summary>

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

- 🤖 = Primarily Claude Code (plugin, SKILL.md, CLAUDE.md or commands)
- 🦞 = Primarily OpenClaw (ClawHub-hosted or built for OpenClaw)  
- 📦 = SkillMD package (hosted on skillmd.ai)
- 🎖️ = Official/vendor-maintained
- 💰 = Requires a paid service (no usable free tier)

</details>

---

## Contributing

Contributions welcome! Please read the [contribution guidelines](CONTRIBUTING.md) first.

### Adding a Skill

1. Fork this repo
2. Add your skill to the appropriate **use case category** (APM & Tracing, Logging & Log Analysis, Metrics & Monitoring, Incident Response & Alerting, Infrastructure & Cloud, Reliability & Chaos Engineering, or Security & Compliance).
3. Include: Name (with link), creator, description, platform icon, star count
4. Mark official skills with 🎖️
5. Submit a PR

### Criteria

- Must be an agent skill (CLAUDE.md, SKILL.md, or SkillMD format) - **NOT** MCP servers
- Must relate to SRE, observability, monitoring, or incident response
- Should have documentation and be actively maintained

> **Note:** MCP servers belong in the awesome-devops-mcp-servers list (see Related Lists)

---

---

<p align="center">
  <em>Last updated: 2026-10-25</em>
</p>
