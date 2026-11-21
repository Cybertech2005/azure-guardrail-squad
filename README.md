# Azure Guardrail Squad

An AI-powered Cloud Security, Governance, and DevSecOps review team built with GitHub Copilot CLI and Squad. **Azure Guardrail Squad** reviews live Azure environments (via a Reader-only Azure MCP Server connection), Terraform code, and GitHub Actions pipelines to find security, access, and cost gaps.

## Members

1. **Triage and Incident Commander:** Takes each request, sends it to the right specialists, and combines their findings into one clean report.
2. **Network and Storage Defender:** Reviews VNets, subnets, NSGs, and storage accounts for open ports (such as RDP or SSH open to `0.0.0.0/0`) and public blob exposure.
3. **Identity and RBAC Auditor:** Reviews who has access. Flags leftover access keys, overly broad roles, and missing managed identities.
4. **Policy and FinOps Controller:** Reviews Azure Policy, budgets, and expensive running resources, and maps controls to NIST CSF.
5. **IaC and CI/CD Inspector:** Reviews Terraform code and GitHub Actions pipelines for mistakes (such as unencrypted disks) before deployment.
6. **Independent Evidence Verifier:** Checks every finding against real evidence before sign-off, and never reviews its own work. The lead cannot override a rejection.

## Shared Guardrails

- A human makes every decision. Default to read-only analysis.
- Azure access comes only through the MCP connection, which uses a **Reader-only identity**. Never attempt to create, change, or delete anything.
- Ask for explicit human approval before any change of any kind.
- Never print or store secrets, access keys, real IP addresses, subscription IDs, or emails. Redact them.
- Label every claim **Confirmed**, **Likely**, or **Unknown**. Do not invent details. If something cannot be read through MCP, mark it **Unknown**.
- Report each finding as: **what I found**, **evidence**, **severity**, **suggested fix**.

## Setup & Usage

1. Authenticate GitHub and a Reader-scoped Azure identity:
   ```bash
   gh auth login
   az login