# Work Routing

How to decide who handles what.

## Routing Table

| Work Type | Route To | Examples |
|-----------|----------|----------|
| Triage, coordination, multi-domain issues, active incidents | Konrad | Severity, ownership, incident coordination, cross-domain synthesis |
| Azure SRE, compute, identity, policy, root cause | Talos | AKS, App Service, Functions, VMs, quotas, Azure Policy, Entra ID, RBAC, Key Vault |
| Delivery engineering and failures | Talos | Azure Pipelines, GitHub Actions, agents, runners, service connections, OIDC, artifacts, deployments |
| Azure networking and connectivity | Octavia | VNets, peering, DNS, Private Link, firewalls, gateways, Front Door, connectivity |
| Azure data platforms and integrity | Variel | Databases, Redis, Storage, replication, backups, restores, migrations, data integrity |
| Azure observability | Cyrion | Azure Monitor, KQL, Application Insights, alerts, dashboards, SLOs |
| Incident and operational documentation | Septimus | Timelines, updates, postmortems, runbooks, Azure Boards items, GitHub issues |
| Independent review and challenge | Sevatar | Pull request review, security checks, test plans, go/no-go, root-cause challenges |

## Issue Routing

| Label | Action | Who |
|-------|--------|-----|
| `squad` | Triage: analyze issue, assign `squad:{member}` label | Konrad |
| `squad:{name}` | Pick up issue and complete the work | Named member |

### How Issue Assignment Works

1. When a GitHub issue gets the `squad` label, **Konrad** coordinates triage and assigns the right `squad:{member}` label.
2. When a `squad:{member}` label is applied, that member picks up the issue in their next session.
3. Members can reassign by removing their label and adding another member's label.
4. The `squad` label is the "inbox" — untriaged issues waiting for Konrad's coordination.

## Rules

1. Konrad owns triage and coordination; the named specialist owns technical work in their domain.
2. At active incident start, Konrad engages Talos and Cyrion first and Septimus from the start. Add Octavia or Variel when evidence indicates their domain.
3. Sevatar independently reviews the proposed root cause and remediation before incident work is called complete. Sevatar does not review their own work.
4. Route one accountable owner per outcome. Add collaborators only for a bounded need; do not launch speculative downstream work.
5. Scribe runs in the background after substantial work when durable decisions require merging; Scribe does not block specialist work.
6. Quick factual questions may be answered directly when evidence is sufficient.
7. When a `squad:{member}` label is applied, route to that member. Konrad coordinates triage for the base `squad` label.
8. Production work follows the approved pull-request and deployment path. Sevatar reviews checks and evidence; the human lead gives final approval before deployment.
