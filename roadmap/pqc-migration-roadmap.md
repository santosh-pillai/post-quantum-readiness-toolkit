# Post-Quantum Cryptography Migration Roadmap

## 1. Purpose

This roadmap provides a structured approach for assessing cryptographic exposure, preparing for post-quantum cryptography (PQC), and planning a controlled transition to appropriate quantum-resistant cryptographic standards.

It is intended to help organizations establish governance, discover cryptographic dependencies, assess risks, evaluate technical options, validate migration approaches, and manage implementation through measurable outcomes.

The roadmap is designed to support business and technology decision-making. It does not prescribe an immediate replacement of every cryptographic implementation or predict when cryptographically relevant quantum computers will become available.

## 2. Objectives

The roadmap aims to:

- Establish accountable governance for PQC readiness and migration.
- Develop and maintain an evidence-based cryptographic inventory.
- Identify relevant cryptographic dependencies across internal and third-party services.
- Assess cryptographic exposure in the context of business impact and confidentiality requirements.
- Evaluate migration complexity separately from cryptographic risk.
- Identify vendor dependencies, technical constraints, and cryptographic agility gaps.
- Validate proposed migration approaches through testing and assurance.
- Track implementation progress, exceptions, and residual risks through established governance.
- Provide executive leadership with clear information for funding, prioritization, and risk decisions.

## 3. Guiding Principles

### Evidence-Based Decisions

Base assessment and migration decisions on documented evidence, validated findings, applicable requirements, and the actual use of cryptography.

### Risk-Based Prioritization

Prioritize investigation and treatment according to cryptographic exposure, business impact, confidentiality requirements, and relevant dependencies. Do not assume that every system using public-key cryptography has the same level of risk.

### Separate Risk from Migration Complexity

Assess cryptographic risk independently from the complexity of implementation. Migration complexity informs sequencing, resources, and delivery planning, but must not independently increase the cryptographic risk rating.

### Third-Party Visibility

Include cryptographic dependencies operated by cloud providers, SaaS vendors, software suppliers, payment processors, managed service providers, and other relevant third parties.

Where details are unavailable, record the information gap and pursue appropriate vendor assurance rather than assuming readiness.

### Standards Alignment

Monitor relevant standards and guidance from recognized bodies, including NIST. Evaluate algorithms, protocols, and implementation options according to their intended use, standardization status, interoperability, and applicable requirements.

### Controlled Migration

Validate proposed changes through appropriate testing, security assurance, operational planning, and rollback arrangements before production deployment.

### Continuous Governance

Treat PQC readiness as an ongoing programme that evolves with changes in technology, business requirements, standards, vendor capabilities, and available evidence.

## 4. Phase 1: Establish Governance

**Objective:** Establish accountability, scope, and decision-making arrangements.

### Key Activities

- Appoint an executive sponsor and accountable programme owner.
- Define scope across business services, applications, infrastructure, cloud platforms, and relevant third-party dependencies.
- Establish roles for Information Security, Enterprise Architecture, Technology, Application Owners, Data Owners, Procurement, Risk, and Compliance.
- Define assessment criteria, evidence requirements, escalation paths, and reporting expectations.
- Establish a process for recording decisions, exceptions, and residual risks.
- Determine how the programme will be funded and monitored.
- Align the programme with applicable regulatory, contractual, and business obligations.

### Deliverables

- Approved programme scope and objectives.
- Governance and responsibility model.
- Assessment methodology and evidence requirements.
- Initial stakeholder and dependency register.
- Executive reporting approach.

### Exit Criteria

Accountability, scope, assessment methods, and governance arrangements are documented and approved by the appropriate authority.

## 5. Phase 2: Discover Cryptographic Dependencies

**Objective:** Establish a validated view of cryptographic assets and their business and technical dependencies.

### Key Activities

- Build and validate the cryptographic inventory.
- Identify algorithms, protocols, certificates, key-management systems, cryptographic implementations, and relevant dependencies.
- Review applications, infrastructure, software libraries, cloud services, identity systems, secure communications, and data protection mechanisms.
- Identify third-party cryptographic dependencies, including vendor-managed services and key-management arrangements.
- Engage technology vendors and service providers to obtain available cryptographic details, PQC support information, and migration commitments.
- Document unknown or unverified information, evidence gaps, accountable owners, and follow-up actions.
- Distinguish confirmed findings from assumptions and record supporting evidence.
- Identify assets and dependencies requiring additional technical discovery.

### Deliverables

- Cryptographic inventory with assigned owners.
- Discovery evidence and validation records.
- Third-party dependency register or linked inventory records.
- Record of unresolved information gaps.
- Initial view of cryptographic implementation and dependency coverage.

### Exit Criteria

The organization has an inventory of identified assets within the agreed scope, documented evidence limitations, and accountable owners for material gaps.

Inventory completion should be measured against the defined scope. It must not be interpreted as proof that every cryptographic dependency has been discovered.

## 6. Phase 3: Assess Risk and Prioritize

**Objective:** Evaluate cryptographic exposure and establish justified treatment priorities.

### Key Activities

- Assess business criticality, data confidentiality requirements, and relevant cryptographic exposure using documented evidence.
- Identify dependencies on cryptographic mechanisms vulnerable to relevant quantum attacks.
- Consider long-lived sensitive data and potential harvest-now-decrypt-later exposure.
- Assess migration complexity, vendor constraints, cryptographic agility, and interoperability separately from cryptographic risk.
- Apply the risk prioritization matrix using documented criteria and professional judgment.
- Use risk findings, migration complexity, applicable obligations, and business constraints to determine treatment sequencing and resource requirements.
- Document material findings, accountable owners, treatment decisions, and exceptions.
- Escalate material findings through established risk governance processes.

### Deliverables

- Documented cryptographic risk findings.
- Prioritized treatment register with evidence and rationale.
- Separate migration complexity assessments.
- Record of material third-party risks and information gaps.
- Recommendations for risk treatment, further investigation, and executive decisions.

### Exit Criteria

Material findings have documented evidence, an assigned owner, a justified priority, and an agreed next action or formal escalation.

A priority is not a prediction of when a quantum attack will occur. An unknown implementation should be recorded as an information gap rather than automatically treated as secure or assigned an unsupported risk rating.

## 7. Phase 4: Evaluate Architecture and Migration Options

**Objective:** Identify technically appropriate migration approaches for prioritized assets and services.

### Key Activities

- Review existing cryptographic architecture and its ability to accommodate algorithm or protocol changes.
- Assess supported PQC standards and implementation options relevant to each use case.
- Evaluate vendor roadmaps, supported product versions, upgrade requirements, and contractual dependencies.
- Identify interoperability constraints across applications, networks, endpoints, partners, and external services.
- Evaluate key and certificate lifecycle requirements, including implications for PKI and key-management systems.
- Consider hybrid approaches where appropriate and supported by relevant standards and implementation guidance.
- Assess operational impact, performance, capacity, cost, and service continuity requirements.
- Define target architecture options, assumptions, dependencies, and validation requirements.
- Develop migration options that address both the underlying exposure and practical delivery constraints.

### Deliverables

- Target architecture and migration options.
- Cryptographic agility gap assessment.
- Vendor readiness and dependency analysis.
- Technical feasibility and interoperability findings.
- Recommended approach for prioritized assets.
- Preliminary implementation estimates and resource requirements.

### Exit Criteria

Recommended approaches have documented technical rationale, dependencies, assumptions, and validation requirements. Material constraints have accountable owners and agreed follow-up actions.

A vendor roadmap or proposed architecture is not evidence that an implementation has been delivered or validated.

## 8. Phase 5: Test and Validate

**Objective:** Demonstrate that proposed migration approaches satisfy security, interoperability, and operational requirements before production implementation.

### Key Activities

- Define test scope, acceptance criteria, and assurance requirements.
- Establish controlled test environments and representative use cases.
- Validate supported algorithms, protocols, libraries, certificates, and key-management arrangements.
- Test interoperability with internal systems, external services, and relevant third parties.
- Assess performance, capacity, latency, reliability, and operational impact.
- Conduct security testing and review implementation configurations.
- Validate monitoring, logging, incident response, backup, recovery, and rollback arrangements.
- Record test evidence, defects, exceptions, and residual risks.
- Obtain the required technical and business approvals before production deployment.

### Deliverables

- Test plans and acceptance criteria.
- Technical validation and security assurance records.
- Interoperability and performance results.
- Defect and remediation register.
- Documented deployment and rollback approach.
- Approval records and residual risk decisions.

### Exit Criteria

Required tests have been completed, material defects have been addressed or formally accepted through governance, and deployment readiness has been approved by the appropriate authority.

## 9. Phase 6: Implement and Transition

**Objective:** Execute approved migration plans in a controlled and measurable manner.

### Key Activities

- Confirm implementation scope, accountable owners, dependencies, resources, and delivery milestones.
- Sequence deployment according to justified risk treatment priorities and operational constraints.
- Coordinate required changes with vendors, service providers, and business partners.
- Implement validated changes through established change management processes.
- Monitor security, service availability, performance, and interoperability during deployment.
- Maintain tested rollback or recovery options where appropriate.
- Update cryptographic inventory records and supporting architecture documentation.
- Validate implementation outcomes and obtain closure evidence.
- Track outstanding issues, approved exceptions, and residual risks.

### Deliverables

- Approved implementation and change records.
- Updated cryptographic inventory.
- Deployment and validation evidence.
- Updated architecture and operational documentation.
- Risk treatment and exception status.
- Closure records for completed actions.

### Exit Criteria

Implemented changes have passed the agreed validation requirements, supporting documentation is updated, and residual risks or outstanding actions have accountable owners.

## 10. Phase 7: Govern and Improve

**Objective:** Maintain readiness and adapt the programme as technology and requirements evolve.

### Key Activities

- Review inventory completeness and evidence quality at defined intervals.
- Reassess material cryptographic risks when new evidence or significant changes arise.
- Monitor relevant standards, implementation guidance, vendor capabilities, and regulatory requirements.
- Track vendor commitments and unresolved third-party dependencies.
- Review migration progress, overdue actions, approved exceptions, and residual risks.
- Reassess migration complexity when architecture, resources, or dependencies change.
- Update executive reporting and programme plans.
- Capture lessons learned and improve assessment and implementation practices.

### Deliverables

- Updated cryptographic inventory and risk records.
- Periodic readiness and programme reports.
- Vendor dependency and commitment reviews.
- Exception and remediation tracking.
- Updated migration plans and governance decisions.
- Documented lessons learned.

### Exit Criteria

The organization maintains accountable ownership, a defined review process, evidence of progress, and a mechanism for addressing changes in cryptographic exposure and migration requirements.

## 11. Executive Oversight Indicators

Use a concise set of indicators that measures coverage, exposure, accountability, and delivery progress.

Suggested indicators include:

- Percentage of in-scope systems with validated cryptographic inventory records.
- Number of critical systems with unresolved cryptographic dependencies.
- Number of material risk findings without approved treatment plans.
- Number of critical third-party dependencies with unresolved PQC readiness questions.
- Percentage of material findings with assigned owners and agreed target dates.
- Migration plans approved and validation milestones completed.
- Overdue remediation actions and unresolved governance decisions.
- Approved exceptions and their next review dates.

Define the calculation, evidence source, accountable owner, reporting frequency, and target for each indicator.

Report the scope and limitations of the underlying data. A high inventory coverage figure should not be presented as proof that every cryptographic dependency has been identified.

## 12. Programme Governance and Accountability

Maintain clear ownership throughout the programme.

| Role | Primary Responsibility |
|---|---|
| Executive Sponsor | Approves strategic direction, resolves material escalations, and supports resource decisions |
| Programme Owner | Coordinates delivery, dependencies, reporting, and governance |
| Information Security | Oversees assessment methodology, cryptographic exposure, risk treatment, and security assurance |
| Enterprise or Solution Architecture | Evaluates architecture, dependencies, and migration options |
| Technology and Application Owners | Validate implementation details, deliver changes, and maintain technical evidence |
| Data Owners | Confirm data sensitivity and confidentiality requirements |
| Procurement and Vendor Management | Coordinate vendor assurance and third-party commitments |
| Risk and Compliance | Support risk governance and applicable obligation assessment |
| Internal Audit or Independent Assurance | Provides independent review where required by the organization's assurance model |

Adapt responsibilities to the organization's operating model. Avoid assigning responsibility to a function that lacks the authority or information required to fulfil it.

## 13. Indicative Programme Sequencing

The phases provide a structured sequence, but they do not prescribe fixed durations. Actual timing depends on the size of the environment, inventory quality, technical dependencies, vendor readiness, regulatory obligations, and available resources.

| Phase | Primary Outcome | Key Dependency |
|---|---|---|
| Establish Governance | Approved scope and accountability | Executive sponsorship |
| Discover Dependencies | Evidence-based inventory | Access to technical and vendor information |
| Assess Risk and Prioritize | Documented findings and treatment decisions | Sufficient evidence and agreed criteria |
| Evaluate Architecture | Validated migration options | Standards, vendor support, and dependency analysis |
| Test and Validate | Demonstrated implementation readiness | Approved test plans and suitable environments |
| Implement and Transition | Controlled deployment | Approvals, resources, and operational readiness |
| Govern and Improve | Sustained oversight | Defined ownership and reporting |

Discovery, vendor engagement, risk assessment, and architecture evaluation may need to proceed iteratively. Material findings should not be delayed solely because the entire inventory is incomplete.

## 14. Key Programme Risks and Considerations

Monitor risks that could affect assessment quality or migration outcomes.

| Risk or Constraint | Potential Consequence | Suggested Response |
|---|---|---|
| Incomplete cryptographic discovery | Unknown exposure and unreliable prioritization | Improve discovery coverage and document evidence gaps |
| Limited third-party transparency | Unresolved dependencies and uncertain migration options | Obtain vendor assurance and establish accountable follow-up |
| Legacy architecture | Restricted migration options and longer delivery timelines | Evaluate cryptographic agility and target architecture |
| Limited cryptographic agility | Increased implementation effort | Identify reusable migration patterns and test options |
| Interoperability constraints | Service disruption or incompatible implementations | Validate representative end-to-end use cases |
| Inadequate testing | Security or operational failures | Define acceptance criteria and retain test evidence |
| Unclear ownership or funding | Delayed remediation and unresolved decisions | Assign accountable owners and escalate material dependencies |
| Unsupported readiness assumptions | Inaccurate reporting and premature closure | Require evidence and distinguish confirmed capabilities from plans |

Adapt this register to the organization's actual findings and governance requirements.

## 15. Limitations

This roadmap provides a practical programme structure for PQC readiness and migration planning. It does not establish certification, guarantee security, or demonstrate regulatory compliance.

The roadmap does not predict the availability of cryptographically relevant quantum computers or prescribe immediate replacement of every cryptographic mechanism.

Migration decisions should be based on documented exposure, business requirements, applicable obligations, relevant standards, implementation maturity, and validated technical options.

Organizations should align their activities with applicable regulatory requirements and current guidance from recognized standards bodies, including NIST.

## 16. Related Resources

- [Cryptographic Inventory Template](../templates/cryptographic-inventory.csv)
- [Cryptographic Inventory Guide](../docs/cryptographic-inventory-guide.md)
- [PQC Readiness Questionnaire](../assessment/pqc-readiness-questionnaire.md)
- [PQC Risk Prioritization Matrix](../assessment/pqc-risk-prioritization-matrix.md)
- [PQC Assessment Scoring Guide](../tools/pqc-assessment-scoring-guide.md)
- [PQC Executive Assessment Report Template](../templates/pqc-executive-assessment-report.md)
