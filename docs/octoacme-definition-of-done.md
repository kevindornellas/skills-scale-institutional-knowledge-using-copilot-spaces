# OctoAcme — Definition of Done

## Purpose
Establish a shared, team-agreed checklist that every work item must satisfy before it is considered complete and ready for release. The Definition of Done (DoD) reduces ambiguity around "done" and ensures consistent quality gates across the team.

> **Owner:** Engineering Manager / Tech Lead, in collaboration with QA Lead and Product Manager.
> See [Roles & Personas](./octoacme-roles-and-personas.md) for full role descriptions.

---

## Scope
This DoD applies to all user stories, features, and bug fixes delivered by the OctoAcme team unless explicitly noted otherwise (e.g., spikes or discovery tasks).

---

## Definition of Done Checklist

### Code Quality
- [ ] Code reviewed and approved by at least one peer (or per team policy)
- [ ] No unresolved review comments marked as blocking
- [ ] Code follows team style guide and linting standards
- [ ] No new linting errors or warnings introduced

### Testing
- [ ] Unit tests written for all new logic (coverage target met per team agreement)
- [ ] Integration tests written or updated where applicable
- [ ] All existing automated tests pass in CI
- [ ] Manual QA completed for features with UX changes or complex flows
- [ ] Edge cases and negative scenarios tested and documented
- [ ] No open P0/P1 defects related to this item

### Security
- [ ] Security scanning (SAST) passes with no new high/critical findings
- [ ] Dependency vulnerability scan reviewed; new CVEs triaged
- [ ] No hardcoded secrets or credentials introduced
- [ ] Threat model reviewed or updated if the feature changes the attack surface (consult Security / AppSec Rep)

### Documentation
- [ ] User-facing documentation written or updated (owner: Technical Writer / Documentation Owner)
- [ ] Inline code comments added for complex logic
- [ ] API documentation updated if API surface changed (endpoints, request/response schemas)
- [ ] Release notes entry drafted

### Observability & Monitoring
- [ ] Feature instrumented with appropriate telemetry/events (consult Data/Analytics Partner)
- [ ] Dashboards or alerts updated if new signals are introduced (consult DevOps / Platform Engineer)
- [ ] No new unhandled exceptions or error states introduced

### Deployment & Release Readiness
- [ ] Feature flag configured correctly (if applicable)
- [ ] Database migrations tested in a staging environment (if applicable)
- [ ] Rollback plan documented for high-risk changes
- [ ] Item meets all criteria in the [Release Readiness Checklist](./octoacme-release-readiness-checklist.md) (at release time)

### Acceptance
- [ ] All acceptance criteria defined in the ticket are met
- [ ] Product Manager or designated reviewer has accepted the implementation
- [ ] UX Designer has reviewed implementation for design fidelity (for UX-impacting features)

---

## Roles & Ownership

| Gate | Owner | Consulted |
|------|-------|-----------|
| Code quality | Developer | Engineering Manager / Tech Lead |
| Testing sign-off | QA Lead / Test Engineer | Developer |
| Security sign-off | Security / AppSec Representative | DevOps |
| Documentation sign-off | Technical Writer / Documentation Owner | Product Manager |
| Acceptance sign-off | Product Manager | UX Designer |

---

## Adapting This Template
Teams may add or remove checklist items to reflect their specific context. Document any team-specific adjustments in the project charter or a team agreement doc. Reference the [Roles & Personas](./octoacme-roles-and-personas.md) document when assigning gate ownership.
