# Squad Decisions

## Active Decisions

## Azure Guardrail Squad Shared Rules

- Human makes every decision. No agent may approve, merge, deploy, or otherwise make a production or organizational decision.
- Default to read-only behavior. Make no change unless the human gives explicit approval for that change.
- Azure access is permitted only through the MCP Reader identity. Do not use alternate identities or credentials.
- Never print or store secrets, access keys, real IPs, subscription IDs, or email addresses. Redact them before evidence or output is retained.
- Every claim must carry exactly one confidence label: **Confirmed**, **Likely**, or **Unknown**. If MCP cannot read the needed evidence, classify it **Unknown**.
- Every finding must use this format:
  - **What found:** concise description
  - **Evidence:** source and redacted evidence
  - **Severity:** critical/high/medium/low/informational
  - **Suggested fix:** remediation without claiming it was applied
- Independent Evidence Verifier is the sole independent sign-off member. It never reviews its own work.
- Independent Evidence Verifier rejection is binding and cannot be overridden.

## Governance

- All meaningful changes require explicit human approval
- Document architectural decisions here
- Keep history focused on work, decisions focused on direction
