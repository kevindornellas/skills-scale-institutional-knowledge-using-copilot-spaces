# OctoAcme — Release Readiness Checklist

## Purpose
Provide a structured go/no-go checklist that the Release Manager, QA Lead, and DevOps/Platform Engineer complete before every release. Reduces the risk of incomplete or unstable deployments reaching production.

See [Roles & Personas](./octoacme-roles-and-personas.md) for ownership details and [Release & Deployment Guide](./octoacme-release-and-deployment.md) for the broader release process.

---

## Release Metadata
- **Release name / version:**
- **Target release date:**
- **Release Manager:**
- **Go/no-go decision owner:** Release Manager (with QA Lead and DevOps sign-off)

---

## Code & Feature Completeness
- [ ] All features scoped for this release are merged to the release branch
- [ ] All acceptance criteria verified and signed off by QA Lead
- [ ] Definition of Done met for all items (see [Definition of Done](./octoacme-definition-of-done.md))
- [ ] No blocking or critical bugs open against this release
- [ ] Feature flags set to the correct state for release

## CI / Build
- [ ] All CI pipeline checks pass on the release branch
- [ ] Security scans pass (no new critical/high findings)
- [ ] Dependency and license checks pass
- [ ] Build artifacts are versioned and available

## Testing
- [ ] Regression test suite passes — **Owner: QA Lead**
- [ ] End-to-end smoke tests pass in staging — **Owner: QA Lead / DevOps**
- [ ] Performance/load tests completed (if applicable) — **Owner: QA Lead**
- [ ] Exploratory testing completed for high-risk areas — **Owner: QA Lead**

## Infrastructure & Deployment
- [ ] Deployment runbook reviewed and up to date — **Owner: DevOps/Platform Engineer**
- [ ] Rollback plan documented and tested — **Owner: DevOps/Platform Engineer**
- [ ] Target environments (staging, production) are healthy — **Owner: DevOps/Platform Engineer**
- [ ] Database migrations tested in staging — **Owner: Developer + DevOps**
- [ ] Feature flags and configuration reviewed — **Owner: Developer + Release Manager**
- [ ] Monitoring and alerting updated for new functionality — **Owner: DevOps/Platform Engineer**

## Documentation & Communication
- [ ] Release notes drafted and reviewed — **Owner: Release Manager + Technical Writer**
- [ ] User-facing docs updated and published (or scheduled) — **Owner: Technical Writer**
- [ ] Stakeholder communication drafted per [Communication Plan](./octoacme-communication-plan-template.md) — **Owner: Release Manager + Project Manager**
- [ ] Support team briefed on changes — **Owner: Project Manager / Release Manager**

## Go / No-Go Decision
| Role | Sign-off | Date |
|---|---|---|
| QA Lead | ☐ Go / ☐ No-Go | |
| DevOps/Platform Engineer | ☐ Go / ☐ No-Go | |
| Release Manager | ☐ Go / ☐ No-Go | |
| Project Manager (final) | ☐ Go / ☐ No-Go | |

**Decision:** [ ] Go / [ ] No-Go

**Notes / Conditions:**

---

## Post-Release
- [ ] Deployment verified in production (smoke tests pass) — **Owner: DevOps / QA Lead**
- [ ] Release announcement sent to stakeholders — **Owner: Release Manager**
- [ ] Release tagged in version control — **Owner: DevOps/Platform Engineer**
- [ ] Release closed in project board — **Owner: Project Manager**
- [ ] Retrospective scheduled if needed — **Owner: Scrum Master / Project Manager**
