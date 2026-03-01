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

## QA Lead / Test Engineer

### Role Summary
QA Leads and Test Engineers own the quality strategy for the project. They define quality gates, write and execute test plans, and act as the last line of defense before release.

### Responsibilities
- Define and maintain the test strategy (unit, integration, end-to-end, performance)
- Author and execute test plans aligned to acceptance criteria
- Maintain and expand automated test suites
- Sign off on release readiness from a quality perspective
- Identify, triage, and track defects through resolution
- Contribute to and enforce the [Definition of Done](./octoacme-definition-of-done.md)

### Goals
- Ensure features meet acceptance criteria before reaching production
- Reduce defect escape rate and production incidents caused by regressions
- Build a fast, reliable automated test suite that supports continuous delivery

### Typical Communication
- Sprint planning and backlog refinement (quality perspective)
- Daily standup and bug triage sessions
- Pre-release sign-off and release readiness reviews
- Defect reports and test summary reports

### Interactions with Existing Roles
- **Developers**: collaborate on unit and integration test coverage; review PRs for testability; pair on complex defect investigations.
- **Product Managers**: validate acceptance criteria for testability; confirm edge cases and negative scenarios are covered.
- **Project Managers**: provide test status and blocker visibility; confirm release readiness gate clearance.
- **Release Manager**: hand off test sign-off as a prerequisite for the go/no-go decision.
- **DevOps / Platform Engineer**: align on CI pipeline test stages, flaky test management, and test environment stability.

---

## Release Manager

### Role Summary
Release Managers own the end-to-end release process, from release planning through post-deployment verification. They coordinate cross-functional readiness and make or facilitate the go/no-go decision.

### Responsibilities
- Own the release plan and release calendar
- Drive the release readiness review using the [Release Readiness Checklist](./octoacme-release-readiness-checklist.md)
- Coordinate the go/no-go decision with QA, DevOps, and Product
- Communicate release timelines, freeze windows, and deployment windows to stakeholders
- Maintain the rollback plan and trigger incident response if a release fails
- Draft and publish release notes

### Goals
- Ship releases safely, predictably, and on schedule
- Reduce production incidents caused by insufficient release coordination
- Maintain a clear audit trail for every release

### Typical Communication
- Release planning and scheduling meetings
- Go/no-go calls with QA, DevOps, and Product leads
- Stakeholder announcements and release notes
- Post-release retrospectives for failed or incident-causing releases

### Interactions with Existing Roles
- **Developers**: confirm all PRs are merged, CI is green, and feature flags are correctly configured.
- **Product Managers**: align on feature scope for each release and communicate any scope changes.
- **Project Managers**: coordinate release milestones against the overall project timeline.
- **QA Lead / Test Engineer**: require test sign-off as a hard gate before going to production.
- **DevOps / Platform Engineer**: coordinate deployment execution, monitoring, and rollback capability.
- **Support / Customer Success**: brief on upcoming changes so they can prepare customer-facing communications.

---

## DevOps / Platform Engineer

### Role Summary
DevOps and Platform Engineers build and maintain the infrastructure, CI/CD pipelines, and tooling that enable the delivery team to ship software reliably and safely.

### Responsibilities
- Design, implement, and maintain CI/CD pipelines
- Manage cloud infrastructure, environments, and deployment tooling
- Ensure platform reliability, scalability, and security posture
- Own the observability stack (logging, metrics, alerting)
- Support incident response and rollback execution
- Drive automation to reduce toil across the delivery lifecycle

### Goals
- Enable fast, safe deployments with minimal manual intervention
- Maintain high environment stability and deployment success rates
- Provide the team with actionable observability into production systems

### Typical Communication
- Infrastructure change proposals and post-mortems
- CI/CD pipeline status and incident alerts
- Platform roadmap updates in engineering syncs
- On-call rotation handoffs

### Interactions with Existing Roles
- **Developers**: provide tooling, environment access, and deployment guidance; review infrastructure-as-code PRs.
- **Project Managers**: surface infrastructure risks and capacity constraints that could affect the project timeline.
- **Release Manager**: execute deployment steps; maintain and test rollback procedures.
- **QA Lead / Test Engineer**: provision and stabilize test environments; integrate automated tests into CI.
- **Security / AppSec Representative**: implement security controls in the pipeline (SAST, dependency scanning, secrets detection).

---

## UX Designer / Researcher

### Role Summary
UX Designers and Researchers ensure that features are usable, accessible, and aligned to real user needs. They translate user insights into design artifacts that guide development.

### Responsibilities
- Conduct user research, interviews, and usability testing
- Create wireframes, prototypes, and high-fidelity designs
- Define interaction patterns and maintain a design system
- Collaborate with Product Managers on problem framing and solution validation
- Review implemented features for design fidelity and accessibility
- Contribute usability acceptance criteria to the backlog

### Goals
- Deliver intuitive, accessible experiences that meet user needs
- Reduce post-release usability issues through early validation
- Maintain design consistency across the product

### Typical Communication
- Design reviews and critique sessions
- Usability test readouts with Product and Engineering
- Async Figma/design tool feedback on PRs or prototypes
- Participation in sprint demos to evaluate design fidelity

### Interactions with Existing Roles
- **Developers**: provide design specs and assets; collaborate on feasibility and edge-case handling; review implementations before release.
- **Product Managers**: co-define problem statements; validate designs against user needs and business goals.
- **Project Managers**: flag design dependencies (e.g., design review time) in the project plan.
- **QA Lead / Test Engineer**: contribute accessibility and usability criteria to acceptance criteria and the Definition of Done.

---

## Technical Writer / Documentation Owner

### Role Summary
Technical Writers and Documentation Owners ensure that product and process documentation is accurate, complete, and accessible to its intended audience.

### Responsibilities
- Author and maintain user-facing documentation (guides, API references, release notes)
- Own process documentation accuracy and versioning under `docs/`
- Collaborate with engineers and PMs to document new features before or alongside release
- Ensure documentation quality gates are met as part of the [Definition of Done](./octoacme-definition-of-done.md)
- Review PRs for documentation impact and accuracy
- Maintain the documentation style guide and templates

### Goals
- Ensure every shipped feature is documented before it reaches users
- Reduce support burden by providing clear, findable documentation
- Keep process docs up to date with actual team practices

### Typical Communication
- Feature spec reviews and documentation planning at sprint kickoff
- PR reviews with documentation change requests
- Documentation review sign-off before release
- Retrospective feedback on documentation gaps

### Interactions with Existing Roles
- **Developers**: gather technical details for documentation; review PRs for doc changes.
- **Product Managers**: align on user-facing messaging and documentation scope for each feature.
- **Project Managers**: flag documentation tasks as part of the Definition of Done; surface doc debt as a project risk.
- **Release Manager**: provide draft release notes as a release gate deliverable.
- **Support / Customer Success**: incorporate common support questions into documentation.

---

## Security / AppSec Representative

### Role Summary
Security and Application Security (AppSec) Representatives ensure that security is embedded into the development lifecycle and that the team ships products that meet security and compliance requirements.

### Responsibilities
- Conduct threat modeling for new features and architecture changes
- Review code and design for security vulnerabilities (OWASP Top 10, etc.)
- Define and enforce security acceptance criteria and quality gates
- Manage security scanning tooling in the CI pipeline
- Triage and track security findings through remediation
- Advise on compliance requirements (e.g., SOC 2, GDPR)

### Goals
- Prevent security vulnerabilities from reaching production
- Build security awareness and shift security left in the development process
- Maintain a clear, current view of the security risk posture for every release

### Typical Communication
- Threat modeling sessions at feature kickoff
- Security findings triage and remediation tracking
- Pre-release security sign-off for the go/no-go decision
- Security incident response participation

### Interactions with Existing Roles
- **Developers**: provide security guidance during design and implementation; review PRs for security issues.
- **Product Managers**: surface compliance requirements that affect feature design or scope.
- **Project Managers**: communicate security risks in the risk register; flag compliance-driven timelines.
- **DevOps / Platform Engineer**: collaborate on pipeline security controls (SAST, DAST, secrets scanning, dependency audits).
- **Release Manager**: provide security sign-off as a hard gate in the release readiness process.

---

## Engineering Manager / Tech Lead

### Role Summary
Engineering Managers and Tech Leads provide technical and people leadership for the engineering team. They are accountable for the technical quality of the team's output and the professional growth of individual engineers.

### Responsibilities
- Set technical direction and maintain architectural standards
- Lead or delegate technical design reviews and architecture decisions
- Remove engineering blockers and manage cross-team technical dependencies
- Coach and mentor engineers; conduct performance reviews
- Partner with Product Managers on scope, feasibility, and trade-offs
- Ensure technical debt is tracked and addressed alongside feature work

### Goals
- Deliver high-quality software that meets business goals
- Build a high-performing, engaged engineering team
- Maintain sustainable engineering velocity

### Typical Communication
- Engineering leadership syncs and architecture reviews
- 1:1s with direct reports
- Cross-team dependency coordination with Project Managers and other Tech Leads
- Escalation point for technical risks and blockers

### Interactions with Existing Roles
- **Developers**: provide technical direction, code review feedback, and career coaching.
- **Product Managers**: negotiate scope and technical trade-offs; ensure feasibility of proposed solutions.
- **Project Managers**: partner on timeline and capacity planning; escalate technical risks.
- **QA Lead / Test Engineer**: align on overall quality strategy and Definition of Done.
- **Security / AppSec Representative**: champion security requirements within the engineering team.
- **DevOps / Platform Engineer**: align on infrastructure and tooling investments.

---

## Support / Customer Success Representative

### Role Summary
Support and Customer Success Representatives act as the voice of the customer within the delivery team. They ensure that customer impact is considered in planning, and they prepare support channels for upcoming releases.

### Responsibilities
- Surface common customer pain points and feature requests to Product Managers
- Prepare support documentation and FAQs for upcoming features
- Validate that releases include adequate user-facing documentation
- Participate in release readiness reviews to confirm support readiness
- Provide post-release feedback on customer reception and issues
- Manage customer escalations that require engineering involvement

### Goals
- Reduce customer support burden through proactive communication and documentation
- Ensure the support team is prepared for every release
- Feed customer insights back into the product roadmap

### Typical Communication
- Sprint demos (as an observer or reviewer)
- Pre-release briefings with the Release Manager
- Weekly product feedback syncs with Product Managers
- Customer escalation calls and incident updates

### Interactions with Existing Roles
- **Product Managers**: provide customer feedback and market insights to inform prioritization.
- **Project Managers**: flag support readiness as a project deliverable; report customer impact during incidents.
- **Release Manager**: confirm support team readiness before go/no-go.
- **Technical Writer / Documentation Owner**: collaborate on user-facing documentation and FAQs.
- **Developers**: escalate critical customer-reported defects; provide reproduction steps.

---

## Data/Analytics Partner

### Role Summary
Data and Analytics Partners define, implement, and maintain the instrumentation and reporting needed to measure product outcomes and support data-informed decision-making.

### Responsibilities
- Define success metrics and KPIs in partnership with Product Managers
- Instrument features with event tracking and telemetry
- Build and maintain dashboards and reports for key project metrics
- Validate data quality and integrity after releases
- Conduct exploratory analysis to surface trends and insights
- Advise on A/B testing and experimentation design

### Goals
- Ensure the team can measure the impact of every shipped feature
- Enable data-driven prioritization and retrospective reviews
- Maintain reliable, accurate data pipelines and dashboards

### Typical Communication
- Metrics definition sessions at feature kickoff
- Dashboard reviews in sprint demos and stakeholder updates
- Post-release data validation reports
- Experimentation readouts with Product Managers

### Interactions with Existing Roles
- **Product Managers**: co-define success metrics; provide data to support prioritization decisions.
- **Developers**: collaborate on instrumentation and telemetry implementation; review analytics-related PRs.
- **Project Managers**: provide project-level metrics (velocity, defect rates) for status reporting.
- **QA Lead / Test Engineer**: validate that instrumentation is covered in test plans.
- **Engineering Manager / Tech Lead**: advise on data architecture and instrumentation standards.

---

## Cross-Role Interaction Matrix

The following table provides a lightweight RACI-style overview of ownership and participation across key artifacts and ceremonies. **R** = Responsible, **A** = Accountable, **C** = Consulted, **I** = Informed.

| Artifact / Ceremony              | Project Manager | Product Manager | Engineering Manager | Developer | QA Lead | Release Manager | DevOps | UX Designer | Technical Writer | Security Rep | Support Rep | Data Partner |
|----------------------------------|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|
| Project charter / one-pager      | A | R | C | C | I | I | I | C | I | C | I | I |
| Backlog & acceptance criteria     | C | A/R | C | C | C | I | I | C | I | C | I | C |
| Definition of Done               | C | C | A | C | R | C | C | C | R | C | I | I |
| Risk register                    | A/R | C | C | C | C | C | C | I | I | C | I | I |
| Release plan & go/no-go          | C | C | C | I | R | A | R | I | C | R | C | I |
| Incident / rollback comms        | C | I | C | C | I | A | R | I | I | C | C | I |
| Retrospective action items       | A/R | C | C | C | C | C | C | C | C | C | C | C |
| Communication plan               | A/R | C | I | I | I | C | I | I | C | I | C | I |
| Test plan & sign-off             | I | C | C | C | A/R | C | C | I | I | C | I | I |
| Architecture / design review     | I | C | A | R | C | I | C | C | I | C | I | I |
| Documentation sign-off           | I | C | C | C | C | C | I | I | A/R | I | C | I |
| Success metrics & dashboards     | I | A | C | C | I | I | I | I | I | I | I | R |

---

## How these personas are used in the exercise
- Use these persona definitions to frame scenarios and sample interactions in the Skills Exercise.
- Each persona can be used as a persona prompt for Copilot Spaces to shape role-specific guidance.

