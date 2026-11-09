# Night Lords Squad: AI SRE and DevOps Team for Azure

An AI-powered SRE and DevOps team built with [GitHub Copilot CLI](https://github.com/features/copilot) and [Squad](https://github.com/bradygaster/squad). Squad turns Copilot into a team of specialized AI agents, each with a defined role, routing rules, and shared guardrails, modeled on how real SRE teams run incident response across Microsoft Azure, Azure DevOps, and GitHub.

## The team

| Agent | Role | Focus |
|---|---|---|
| Konrad | Lead Orchestrator | Triage, delegation, incident timeline |
| Talos | Azure SRE and Delivery Lead | Root cause, AKS, App Service, pipelines, deployments |
| Octavia | Azure Network Engineer | VNets, DNS, firewalls, Private Link, connectivity |
| Variel | Azure Data Engineer | Databases, backups, replication, data safety |
| Cyrion | Azure Observability Engineer | Azure Monitor, KQL, alerts, SLOs |
| Septimus | Incident Documentation Lead | Timelines, postmortems, work items |
| Sevatar | Independent QA and Reviewer | Verifies diagnoses and changes before sign-off |

## Guardrails

Every agent follows shared rules defined in `.squad/decisions.md`:

- A human is the final authority on every decision
- Agents default to read-only investigation
- Explicit human approval is required before any production change
- No merging pull requests, bypassing checks, or exposing secrets
- The reviewer cannot review its own work, and the lead agent cannot override a rejection
- Every claim is labeled Confirmed, Likely, or Unknown, and agents never invent details they cannot verify

## Repository structure

| Path | Purpose |
|---|---|
| `.squad/team.md` | Team roster |
| `.squad/routing.md` | Which agent handles which kind of work |
| `.squad/decisions.md` | Shared rules and guardrails |
| `.squad/agents/` | Each agent's charter (role) and history (memory) |
| `.github/agents/squad.agent.md` | Lets Copilot load the team |
| `.github/workflows/` | Squad automations that run on GitHub |

## Setup

Works on Windows and macOS.

1. Install the prerequisites: Git, Node.js 22+, GitHub CLI, PowerShell 7
   - Windows: `winget`
   - macOS: `brew`
2. Install the tools: `npm install -g @github/copilot @bradygaster/squad-cli`
3. Sign in: `gh auth login`
4. Start the team: `copilot --agent squad`

## Status

Demo environment. No live Azure environment is connected, so environment details are marked Unknown by design.
