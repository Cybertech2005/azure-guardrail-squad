# Ceremonies

> Team meetings that happen before or after work. Each squad configures their own.

## Design Review

| Field | Value |
|-------|-------|
| **Trigger** | auto |
| **When** | before |
| **Condition** | multi-agent task involving 2+ agents modifying shared systems |
| **Facilitator** | Konrad |
| **Participants** | all-relevant |
| **Time budget** | focused |
| **Enabled** | ✅ yes |

**Agenda:**
1. Review the task and requirements
2. Agree on interfaces and contracts between components
3. Identify risks and edge cases
4. Assign action items

---

## Retrospective

| Field | Value |
|-------|-------|
| **Trigger** | auto |
| **When** | after |
| **Condition** | build failure, test failure, or reviewer rejection |
| **Facilitator** | Konrad |
| **Participants** | all-involved |
| **Time budget** | focused |
| **Enabled** | ✅ yes |

**Agenda:**
1. What happened? (facts only)
2. Root cause analysis
3. What should change?
4. Action items for next iteration


---

## Retrospective with Enforcement

| Field | Value |
|-------|-------|
| **Trigger** | auto |
| **When** | weekly |
| **Condition** | No *retrospective* log in .squad/log/ within the last 7 days |
| **Facilitator** | lead |
| **Participants** | all |
| **Time budget** | focused |
| **Enabled** | yes |
| **Enforcement skill** | retro-enforcement |

**Agenda:**
1. What shipped this week? (closed issues, merged PRs)
2. What did not ship? (open issues, blockers)
3. Root cause on any failures
4. Action items -- each MUST become a GitHub Issue labeled retro-action

**Coordinator integration:**
At round start, call Test-RetroOverdue (see skill retro-enforcement). If overdue, run this ceremony before the work queue.

**Why GitHub Issues, not markdown:**
Production data: 0% completion across 6 retros using markdown checklists, 100% after switching to GitHub Issues.

---

## Incident Kickoff

| Field | Value |
|-------|-------|
| **Trigger** | auto |
| **When** | before |
| **Condition** | Active production incident |
| **Facilitator** | Konrad |
| **Participants** | Talos, Cyrion, Septimus; add Octavia or Variel based on evidence |
| **Time budget** | focused |
| **Enabled** | ✅ yes |

**Agenda:**
1. Confirm severity, UTC start time, affected customers, subscriptions, regions, and services; mark unknown scope explicitly.
2. Check Azure Service Health, recent deployments, pipeline runs, workflow runs, and merged pull requests.
3. Establish the initial timeline, working hypothesis, read-only investigation owners, and action list.
4. Confirm the active tenant, subscription, organization, project, repository, and branch before commands.
5. Escalate proposed production actions to the human lead with impact, blast radius, verification, and rollback details.

---

## Production Change Review

| Field | Value |
|-------|-------|
| **Trigger** | auto |
| **When** | before |
| **Condition** | Proposed production change or deployment |
| **Facilitator** | Konrad |
| **Participants** | Owning specialist, Sevatar, human lead |
| **Time budget** | focused |
| **Enabled** | ✅ yes |

**Agenda:**
1. Verify the pull request, required checks, artifact, approvals, target subscription/environment, and declared platform of record.
2. Have Sevatar independently review the change, evidence, edge cases, and rollback path.
3. State the exact action, expected impact, blast radius, verification method, and rollback plan.
4. Obtain the human lead's explicit approval before deployment. This ceremony does not grant approval or bypass a required check.

---

## Post-Incident Review

| Field | Value |
|-------|-------|
| **Trigger** | auto |
| **When** | after |
| **Condition** | Incident mitigation is complete and service status has been verified |
| **Facilitator** | Konrad |
| **Participants** | All involved specialists, Septimus, Sevatar, human lead |
| **Time budget** | focused |
| **Enabled** | ✅ yes |

**Agenda:**
1. Confirm the UTC timeline, customer impact, and evidence links; separate facts, hypotheses, and open questions.
2. Review Sevatar's challenge of the root cause and remediation and document any remaining uncertainty.
3. Record mitigation, recovery verification, approved changes, and source-control reconciliation for any emergency change.
4. Produce a blameless postmortem and assign follow-up actions in the confirmed work-tracking system without duplicate tracking.
