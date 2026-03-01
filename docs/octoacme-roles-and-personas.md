# OctoAcme Personas

This document defines typical roles and responsibilities used in OctoAcme project docs and exercises.

---

## Developers

### Role Summary
Developers design, build, test, and deliver software components. They collaborate with product and project leads to implement features that meet acceptance criteria and quality standards.

### Responsibilities
- Implement features and fixes to meet acceptance criteria
- Write and maintain tests and documentation
- Participate in design and code reviews
- Assist in estimating and planning work
- Help identify technical risks and propose mitigations

### Goals
- Deliver reliable, maintainable code
- Reduce cycle time from idea to production
- Maintain high test coverage and observability

### Typical Communication
- Daily standups and sprint planning
- PR descriptions and code review comments
- Technical design docs when needed

---

## Product Managers

### Role Summary
Product Managers define what should be built to deliver customer and business value. They own the product vision, prioritize the backlog, and measure outcomes.

### Responsibilities
- Define problem statements and success metrics
- Prioritize the roadmap and backlog
- Collaborate with stakeholders and engineering on trade-offs
- Validate solutions through user research and metrics

### Goals
- Maximize customer value and impact
- Make clear, data-driven prioritization decisions
- Ensure product-market fit and usability

### Typical Communication
- Weekly alignment with PM and engineering leads
- Roadmap updates and stakeholder briefings
- Acceptance criteria and feature specs

---

## Project Managers

### Role Summary
Project Managers coordinate delivery activities, manage schedules, risks, and communications. They enable the team to deliver on commitments efficiently.

### Responsibilities
- Create and maintain project plans and timelines
- Manage risks, dependencies, and resource constraints
- Facilitate meetings (kickoff, planning, retrospectives)
- Ensure consistent project documentation and status reporting
- Coordinate cross-team and stakeholder communication

### Goals
- Deliver projects on time and within scope
- Minimize unplanned work and escalations
- Maintain transparency and alignment across stakeholders

### Typical Communication
- Weekly status updates and stakeholder reports
- Risk registers and decision logs
- Coordination via project boards and meeting facilitation

---

## Release Manager

### Role Summary
The Release Manager owns the release calendar and coordinates everything needed to ship safely and on schedule. They bridge engineering, QA, and operations to ensure every deployment is planned, communicated, and reversible.

### Responsibilities
- Own and maintain the release calendar and deployment schedule
- Coordinate go/no-go decisions with QA Lead, DevOps, and Project Manager
- Draft and distribute release notes and announcements
- Ensure rollback and mitigation plans are in place before every deployment
- Track post-release metrics and confirm stability before closing a release

### Goals
- Ship reliably with minimal unplanned downtime
- Maintain a clear audit trail for every release
- Reduce release-related incidents through process discipline

### Typical Communication
- Release readiness reviews with QA Lead and DevOps/Platform Engineer
- Pre-release announcements to stakeholders via the [Communication Plan](./octoacme-communication-plan-template.md)
- Coordinates with Project Manager on timeline and milestone tracking

### Interactions with Other Roles
- **Project Manager**: aligns release dates with project milestones and escalates blockers
- **QA Lead**: reviews test sign-off and release readiness before go/no-go
- **DevOps/Platform Engineer**: confirms deployment pipeline, infrastructure readiness, and rollback capability
- **Product Manager**: aligns feature scope and communicates what ships in each release

---

## Scrum Master / Delivery Manager

### Role Summary
The Scrum Master (or Delivery Manager in non-Scrum teams) facilitates Agile ceremonies, removes impediments, and coaches the team on continuous-improvement practices. While the Project Manager focuses on schedule, scope, and stakeholder communication, the Scrum Master focuses on team health, process efficiency, and ceremony quality.

> **Distinction from Project Manager**: The Project Manager is accountable for delivery commitments and external stakeholder communication. The Scrum Master is accountable for the team's process and removing internal impediments. On some teams these roles overlap; where they are distinct, close partnership is essential.

### Responsibilities
- Facilitate standups, sprint planning, sprint reviews, and retrospectives
- Identify and remove team impediments promptly
- Coach the team on Agile/Scrum practices and continuous improvement
- Shield the team from unplanned interruptions during a sprint
- Track team velocity and surface trends to the Project Manager

### Goals
- Keep ceremonies focused and time-boxed
- Continuously raise team throughput and quality
- Foster a psychologically safe, self-organizing team culture

### Typical Communication
- Daily standups and retrospective facilitation
- Impediment log shared with Project Manager
- Sprint metrics and velocity shared in weekly PM sync

### Interactions with Other Roles
- **Project Manager**: shares velocity data and escalates impediments that require external resolution
- **Developers**: coaches on Agile practices and removes blockers day-to-day
- **Product Manager**: ensures backlog refinement is timely and acceptance criteria are clear before sprint planning

---

## QA Lead / Test Engineer

### Role Summary
The QA Lead defines the test strategy, coordinates test execution across the team, and acts as the final quality gate before release. They advocate for quality throughout the entire delivery lifecycle, not just at the end.

### Responsibilities
- Define and maintain the test strategy (unit, integration, E2E, exploratory)
- Coordinate test execution and manage bug triage
- Establish and enforce the [Definition of Done](./octoacme-definition-of-done.md)
- Sign off on release readiness using the [Release Readiness Checklist](./octoacme-release-readiness-checklist.md)
- Report quality metrics (defect density, test coverage, open critical bugs) to the Project Manager

### Goals
- Prevent regressions and catch defects early
- Maintain high confidence in every release
- Integrate quality practices into the development workflow (shift-left testing)

### Typical Communication
- Bug triage meetings with Developers
- Release readiness sign-off with Release Manager
- Test coverage reports in sprint review

### Interactions with Other Roles
- **Developers**: reviews acceptance criteria and test plans early; pairs on difficult test scenarios
- **Release Manager**: provides formal test sign-off before go/no-go
- **DevOps/Platform Engineer**: aligns on CI test gates and environment provisioning
- **Product Manager**: clarifies acceptance criteria and edge cases to inform test coverage

---

## DevOps / Platform Engineer

### Role Summary
DevOps/Platform Engineers build and maintain the infrastructure, CI/CD pipelines, and tooling that enable safe, fast, and repeatable delivery. They are the operational backbone of the delivery process.

### Responsibilities
- Design, implement, and maintain CI/CD pipelines
- Manage infrastructure-as-code (IaC) and environment configuration
- Implement and monitor observability (logs, metrics, alerts)
- Own the deployment runbook and rollback procedures
- Participate in incident response and post-mortems

### Goals
- Maximize pipeline reliability and deployment frequency
- Minimize mean time to recovery (MTTR) for incidents
- Provide stable, self-service environments for developers and QA

### Typical Communication
- Release readiness reviews with Release Manager and QA Lead
- Incident notifications to on-call and Project Manager
- Infrastructure change reviews in technical design discussions

### Interactions with Other Roles
- **Release Manager**: confirms pipeline readiness and executes deployments on agreed schedule
- **QA Lead**: provides test environments and integrates quality gates into CI
- **Developers**: supports local environment setup and reviews infrastructure impact of code changes
- **Security/AppSec Representative**: implements security scanning and compliance controls in the pipeline

---

## UX Designer / Researcher

### Role Summary
UX Designers and Researchers ensure that product decisions are grounded in user needs. They translate research findings into design artifacts that guide development and validate assumptions before code is written.

### Responsibilities
- Conduct user research (interviews, usability tests, surveys)
- Create wireframes, prototypes, and design specifications
- Maintain the design system and ensure consistency across features
- Collaborate in backlog refinement to ensure designs are implementation-ready
- Validate shipped features against design intent

### Goals
- Deliver intuitive, accessible, and delightful user experiences
- Reduce rework by resolving UX unknowns before development begins
- Align design decisions with product strategy and success metrics

### Typical Communication
- Design reviews with Product Manager and Developers
- Usability test readouts to the full delivery team
- Design specs shared in the project board before sprint planning

### Interactions with Other Roles
- **Product Manager**: co-owns user story definition and validates that designs address the problem statement
- **Developers**: provides implementation-ready specs and answers design questions during development
- **QA Lead**: shares design intent so testers can catch UX regressions
- **Technical Writer**: shares design flows to inform user-facing documentation

---

## Technical Writer / Documentation Owner

### Role Summary
Technical Writers create and maintain user-facing, technical, and process documentation. They ensure that institutional knowledge is captured, accurate, and discoverable—reducing onboarding time and support burden.

### Responsibilities
- Author and update user guides, API docs, and process documentation
- Review and edit documentation contributions from developers and PMs
- Maintain a documentation style guide and templates
- Ensure documentation is updated as part of the [Definition of Done](./octoacme-definition-of-done.md)
- Work with the UX Designer to align in-product guidance with external docs

### Goals
- Ensure every shipped feature has accurate, discoverable documentation
- Reduce support escalations caused by documentation gaps
- Build a culture where documentation is maintained continuously, not as an afterthought

### Typical Communication
- Documentation review in sprint review / release sign-off
- Collaborative editing with Developers and Product Manager
- Coordinates with Release Manager to publish docs alongside releases

### Interactions with Other Roles
- **Developers**: sources technical details and reviews docs for accuracy
- **Product Manager**: aligns on messaging, audience, and scope of documentation
- **QA Lead**: confirms documented behavior matches tested behavior
- **Release Manager**: times documentation publication with each release

---

## Role Interaction & Ownership Matrix (RACI)

This lightweight RACI table maps key ceremonies and artifacts to roles.
**R** = Responsible (does the work), **A** = Accountable (final sign-off), **C** = Consulted, **I** = Informed.

| Ceremony / Artifact | Project Manager | Product Manager | Developer | QA Lead | Release Manager | DevOps/Platform | Scrum Master | UX Designer | Technical Writer |
|---|---|---|---|---|---|---|---|---|---|
| Project One-pager | A | R | C | I | I | I | I | C | I |
| Backlog & Acceptance Criteria | C | A/R | C | C | I | I | C | C | I |
| Definition of Done | A | C | R | R | C | C | R | I | C |
| Sprint Planning & Ceremonies | C | C | R | R | I | I | A/R | C | I |
| Risk Register | A/R | C | C | C | C | C | I | I | I |
| Release Readiness / Go-No-Go | A | C | C | R | R | R | I | I | C |
| Deployment & Rollback | I | I | C | C | A | R | I | I | I |
| Incident & Rollback Comms | A | C | C | C | R | R | I | I | I |
| Stakeholder Status Updates | A/R | C | I | I | I | I | I | I | I |
| Communication Plan | A/R | C | I | I | C | I | I | I | C |
| Retrospective Facilitation | C | I | R | R | I | I | A/R | I | I |
| Documentation Updates | C | C | R | C | C | I | I | C | A/R |

---

## How these personas are used in the exercise
- Use these persona definitions to frame scenarios and sample interactions in the Skills Exercise.
- Each persona can be used as a persona prompt for Copilot Spaces to shape role-specific guidance.

