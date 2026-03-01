# OctoAcme — Communication Plan Template

## Purpose
Ensure that all stakeholders receive timely, accurate, and appropriately detailed information throughout the project lifecycle. Complete this template during project initiation and update it whenever scope, schedule, or stakeholders change.

See [Roles & Personas](./octoacme-roles-and-personas.md) for role descriptions and [Project Initiation Guide](./octoacme-project-initiation.md) for when to create this plan.

---

## Plan Metadata
- **Project name:**
- **Communication Plan Owner:** Project Manager
- **Last updated:**

---

## Stakeholder Register

| Stakeholder / Group | Role | Interest / Need | Preferred Channel | Frequency |
|---|---|---|---|---|
| Executive Sponsor | Decision-maker | High-level status and risk | Email summary | Monthly |
| Product Manager | Strategy owner | Feature progress, trade-offs | Slack + weekly sync | Weekly |
| Engineering Lead | Delivery oversight | Technical blockers, velocity | Slack + standup | Daily / Weekly |
| QA Lead | Quality gate | Test progress, release readiness | Jira/GitHub + review meeting | Per sprint |
| Release Manager | Release coordination | Release schedule, go/no-go status | Release readiness review | Per release |
| Support / Customer Success | Customer-facing | Known issues, release contents | Release notes email | Per release |
| End Users | Product recipients | New features, breaking changes | In-product notice + docs | Per release |
| _(add rows as needed)_ | | | | |

---

## Communication Types & Cadence

### Regular Updates
| Communication | Audience | Owner | Frequency | Channel |
|---|---|---|---|---|
| Weekly status report | Sponsor, stakeholders | Project Manager | Weekly | Email / Confluence |
| Sprint review / demo | Full team + stakeholders | Scrum Master / PM | Per sprint | Video call |
| Stakeholder briefing | Executives | Project Manager | Monthly | Meeting / deck |
| Release announcement | All stakeholders | Release Manager | Per release | Email + Slack |

### Event-Driven Communications
| Event | Audience | Owner | Template / Notes |
|---|---|---|---|
| Project kickoff | All stakeholders | Project Manager | See [Project Initiation Guide](./octoacme-project-initiation.md) |
| Risk escalation | Sponsor, relevant leads | Project Manager | Use Risk Register entry |
| Incident notification | On-call, stakeholders | Release Manager / DevOps | See [Risks & Communication](./octoacme-risks-and-communication.md) |
| Go/no-go decision | Release team, stakeholders | Release Manager | See [Release Readiness Checklist](./octoacme-release-readiness-checklist.md) |
| Project closure | All stakeholders | Project Manager | Final status + retro summary |

---

## Weekly Status Update Template
```text
Subject: [Project Name] — Weekly Status (Week of YYYY-MM-DD)

Overall Status: 🟢 On Track / 🟡 At Risk / 🔴 Off Track

Progress this week:
- 

Next steps:
- 

Risks & blockers:
- 

Decisions needed:
- 
```

---

## Escalation Path
1. Team-level triage (daily standup)
2. Project Manager → Product Lead (blocker persists >1 day)
3. Project Manager → Sponsor (business-impacting risk)
4. For security incidents: follow the security incident runbook and notify Security on-call immediately

See [Risks & Communication](./octoacme-risks-and-communication.md) for the full escalation framework.

---

## Communication Checklist
- [ ] Stakeholder register completed and reviewed with sponsor
- [ ] Communication cadence agreed with key stakeholders
- [ ] Channels and tools confirmed (Slack workspace, email lists, project board)
- [ ] Escalation path documented and communicated to the team
- [ ] Plan reviewed and updated after each major milestone
