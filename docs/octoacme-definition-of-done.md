# OctoAcme — Definition of Done (DoD)

## Purpose
Establish a shared, team-agreed checklist that every work item must satisfy before it can be considered "Done." This prevents partial shipments and keeps quality consistent across sprints.

See [Roles & Personas](./octoacme-roles-and-personas.md) for ownership details and [Project Planning](./octoacme-project-planning.md) for how the DoD is established during planning.

---

## Owners
| Activity | Owner |
|---|---|
| Define & maintain DoD | QA Lead (with Developer and Project Manager input) |
| Verify DoD per story | Developer (self-check) + QA Lead (sign-off) |
| Enforce DoD at sprint boundary | Scrum Master / Project Manager |
| Documentation completeness | Technical Writer |

---

## Code & Implementation
- [ ] Code implemented and peer-reviewed (at least one approval)
- [ ] Automated tests written (unit and/or integration) and passing in CI
- [ ] No new linting errors or warnings introduced
- [ ] Security scanning passes (no new critical/high findings)
- [ ] Acceptance criteria verified by the Developer

## Quality Assurance
- [ ] QA Lead has reviewed and signed off on test coverage
- [ ] All acceptance criteria validated (automated or manual)
- [ ] No open blocking or critical bugs related to this work item
- [ ] Regression tests updated or added where applicable
- [ ] End-to-end smoke tests pass for affected flows

## Documentation
- [ ] In-code documentation (comments, docstrings) updated
- [ ] User-facing docs updated or new docs created (Technical Writer review)
- [ ] API/schema changes documented in the relevant spec or changelog
- [ ] Release notes entry drafted (Release Manager review)

## Design & Accessibility
- [ ] Implementation matches approved design spec (UX Designer sign-off if UI changes)
- [ ] Accessibility standards met (WCAG AA minimum for user-facing changes)

## Deployment Readiness
- [ ] Feature flags configured if applicable
- [ ] Database migrations tested in staging
- [ ] Monitoring/alerting updated for new functionality
- [ ] Rollback steps documented in the [Release Readiness Checklist](./octoacme-release-readiness-checklist.md)

## Process
- [ ] Work item closed or moved to "Done" in the project board
- [ ] Any follow-up tasks or tech-debt items logged as new issues

---

## Notes
- The DoD applies to every story/task unless explicitly waived by the Project Manager and QA Lead with a documented reason.
- The DoD should be reviewed and updated at each retrospective. See [Retrospective & Continuous Improvement](./octoacme-retrospective-and-continuous-improvement.md).
