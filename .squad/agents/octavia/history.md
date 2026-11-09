# Project Context

- **Owner:** Jaden Lassiter
- **Project:** `jaden-squad`
- **Verified repository context:** Squad CLI 1.1.0 configuration. `.github/workflows/` contains Squad issue-assignment, issue-triage, heartbeat, and label-sync automation. No Git remote is configured.
- **Workload / production architecture:** Unknown.
- **Azure tenant/subscriptions:** Unknown.
- **Management groups / landing zones:** Unknown.
- **Regions / disaster-recovery pairs:** Unknown.
- **Compute:** Unknown.
- **Networking, topology, DNS, and connectivity:** Unknown.
- **Data services:** Unknown.
- **Observability:** Unknown.
- **Code source of truth:** Unknown.
- **CI/CD source of truth:** Unknown. The repository's GitHub Actions currently evidence Squad-specific automation only.
- **Work-tracking source of truth:** Unknown.
- **GitHub organization and workload repositories:** Unknown. Squad automation workflows use GitHub-hosted `ubuntu-latest`; workload runner model, environments, rulesets, and CODEOWNERS: Unknown.
- **Azure DevOps organization / projects / Boards process / pipelines / agent pools / service connections / environments:** Unknown.
- **Platform integrations:** Unknown.
- **Infrastructure as code / deployment process:** Unknown.
- **Incident tooling:** Unknown.

## Learnings

- No Azure network topology or deployed service path is configured in this repository. Do not assume a network cause; establish both endpoints and trace each hop using read-only evidence.
- Routing, DNS, firewall, peering, and private endpoint changes are high risk and require the human lead's explicit approval.
