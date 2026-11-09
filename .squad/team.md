# Squad Team

> SRE and DevOps team focused on Microsoft Azure, Azure DevOps, and GitHub.

## Coordinator

| Name | Role | Notes |
|------|------|-------|
| Squad | Coordinator | Routes work, enforces handoffs and reviewer gates. Does not perform specialist work. |

## Members

| Name | Role | Charter | Status |
|------|------|---------|--------|
| Konrad | Lead Orchestrator | `.squad/agents/konrad/charter.md` | ✅ Active |
| Talos | Azure SRE and Delivery Lead | `.squad/agents/talos/charter.md` | ✅ Active |
| Octavia | Azure Network Engineer | `.squad/agents/octavia/charter.md` | ✅ Active |
| Variel | Azure Data Engineer | `.squad/agents/variel/charter.md` | ✅ Active |
| Cyrion | Azure Observability Engineer | `.squad/agents/cyrion/charter.md` | ✅ Active |
| Septimus | Incident Documentation Lead | `.squad/agents/septimus/charter.md` | ✅ Active |
| Sevatar | Independent QA and Reviewer | `.squad/agents/sevatar/charter.md` | ✅ Active |

## Built-in Support Agents

| Name | Role | Charter | Status |
|------|------|---------|--------|
| Scribe | Decision Merger | `.squad/agents/scribe/charter.md` | 📋 Silent |
| Ralph | Work Monitor | `.squad/agents/ralph/charter.md` | 🔄 Monitor |
| Rai | RAI Reviewer | `.squad/agents/Rai/charter.md` | 🛡️ RAI |
| Fact Checker | Devil's Advocate & Verification Agent | `.squad/agents/fact-checker/charter.md` | 🔍 Verifier |

## Project Context

- **Owner:** Jaden Lassiter
- **Project:** `jaden-squad`
- **Description:** Squad coordinator configuration and GitHub Actions automation for Squad issue routing and team operations.
- **Stack:** Squad CLI 1.1.0; Markdown and GitHub Actions workflows. Application and production workload stack: Unknown.
- **Created:** 2026-11-09

## Environment and Platform Sources of Truth

- **Azure environment and services:** Unknown; no tenant, subscription, landing-zone, region, compute, network, data, or observability configuration is declared in the repository.
- **Code source of truth:** Unknown.
- **CI/CD source of truth:** Unknown. The repository contains GitHub Actions for Squad issue assignment, triage, heartbeat, and label synchronization; this does not establish the workload CI/CD source of truth.
- **Work-tracking source of truth:** Unknown.
- **GitHub organization and workload repositories:** Unknown. Squad automation workflows use GitHub-hosted `ubuntu-latest`; workload runner model, environments, rulesets, and CODEOWNERS: Unknown.
- **Azure DevOps organization, projects, Boards process, pipelines, agent pools, service connections, and environments:** Unknown.
- **Platform integrations, infrastructure as code, and incident tooling:** Unknown.
- **Evidence note:** No configured Git remote or repository-level Azure/workload deployment configuration was found during setup. No platform-source conflict was found.
