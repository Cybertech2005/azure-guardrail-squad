# Project Context

- **Owner:** Jaden Lassiter
- **Project:** `jaden-squad`
- **Verified repository context:** Squad CLI 1.1.0 configuration. `.github/workflows/` contains Squad issue-assignment, issue-triage, heartbeat, and label-sync automation. No Git remote is configured.
- **Workload / production architecture:** Unknown.
- **Azure tenant/subscriptions:** Unknown.
- **Management groups / landing zones:** Unknown.
- **Regions / disaster-recovery pairs:** Unknown.
- **Compute:** Unknown.
- **Networking:** Unknown.
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

- There is no verified Azure subscription, workload, or delivery configuration in the repository. Confirm active tenant, subscription, organization, project, repository, and branch before commands.
- For production delivery investigations, connect the approved pull request to build, artifact, approval, deployment, and running version.
