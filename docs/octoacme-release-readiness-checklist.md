# OctoAcme — Release Readiness Checklist

## Purpose
Provide a shared, repeatable checklist to verify that a release is safe to deploy to production. The Release Manager drives this checklist during the go/no-go review. All gates must be cleared before proceeding to production.

> **Owner:** Release Manager.
> See [Roles & Personas](./octoacme-roles-and-personas.md) for full role descriptions.

---

## Release Information

| Field | Value |
|-------|-------|
| Release name / version | |
| Target deployment date | |
| Deployment window | |
| Release Manager | |
| On-call contact | |

---

## Pre-Release Checklist

### Scope & Code
- [ ] All planned user stories and bug fixes are merged to the release branch
- [ ] No unintended commits or partial features are included in the release
- [ ] All feature flags for this release are configured correctly (owner: Developer / DevOps)
- [ ] Change log / release notes are drafted and reviewed (owner: Technical Writer / Documentation Owner)

### Quality Gates
- [ ] All acceptance criteria for in-scope items are met (owner: QA Lead / Test Engineer)
- [ ] Full test suite passes in CI — no failing or skipped tests without documented justification (owner: QA Lead)
- [ ] Manual QA sign-off completed for features requiring human validation (owner: QA Lead)
- [ ] Definition of Done satisfied for all items in scope (see [Definition of Done](./octoacme-definition-of-done.md))
- [ ] No open P0 or P1 defects targeting this release

### Security
- [ ] SAST scan passes with no new high/critical findings (owner: Security / AppSec Representative)
- [ ] Dependency vulnerability scan reviewed and triaged (owner: Security / AppSec)
- [ ] Secrets detection scan clean (owner: DevOps / Platform Engineer)
- [ ] Security sign-off received for changes that affect the attack surface

### Infrastructure & Deployment
- [ ] Deployment pipeline tested in staging environment (owner: DevOps / Platform Engineer)
- [ ] Staging smoke tests pass (owner: QA Lead / DevOps)
- [ ] Database migrations (if any) tested in staging; rollback migration verified
- [ ] Deployment window and maintenance page (if needed) coordinated with Support (owner: Release Manager)
- [ ] Monitoring and alerting confirmed active for production environment (owner: DevOps)

### Rollback Plan
- [ ] Rollback procedure documented and verified (owner: DevOps / Platform Engineer)
- [ ] Previous known-good release version identified and rollback tested in staging
- [ ] On-call rotation confirmed for the deployment window (owner: Engineering Manager / DevOps)

### Stakeholder Readiness
- [ ] Support / Customer Success briefed on changes and support documentation ready (owner: Support Rep / Technical Writer)
- [ ] Internal stakeholder announcement prepared (owner: Project Manager / Release Manager)
- [ ] External communications drafted if customer-facing changes are significant (owner: Product Manager)

### Documentation
- [ ] User-facing documentation published or scheduled to publish at release time (owner: Technical Writer)
- [ ] API documentation updated and published (if API changes included)
- [ ] Internal runbooks updated (if operational procedures changed)

---

## Go / No-Go Sign-Off

| Role | Name | Decision | Notes |
|------|------|----------|-------|
| QA Lead / Test Engineer | | ☐ Go / ☐ No-Go | |
| Security / AppSec Representative | | ☐ Go / ☐ No-Go | |
| DevOps / Platform Engineer | | ☐ Go / ☐ No-Go | |
| Product Manager | | ☐ Go / ☐ No-Go | |
| Engineering Manager / Tech Lead | | ☐ Go / ☐ No-Go | |
| Release Manager (final decision) | | ☐ Go / ☐ No-Go | |

---

## Post-Deployment Verification

- [ ] Production deployment completed successfully
- [ ] Post-deploy smoke tests pass
- [ ] Key dashboards and monitors confirm healthy system state (owner: DevOps)
- [ ] Release announcement sent to stakeholders (owner: Release Manager / Project Manager)
- [ ] Support team notified that release is live (owner: Support Rep)
- [ ] Release notes published

---

## Related Docs
- [Roles & Personas](./octoacme-roles-and-personas.md)
- [Definition of Done](./octoacme-definition-of-done.md)
- [Release & Deployment Guide](./octoacme-release-and-deployment.md)
