# Post-Quantum Cryptography Migration Roadmap

## Purpose

This roadmap provides a structured approach to preparing for post-quantum cryptography (PQC). It connects cryptographic discovery and risk assessment with architecture decisions, controlled testing, implementation, and ongoing governance.

The roadmap should be tailored to the organization's risk profile, technology environment, vendor dependencies, regulatory obligations, and business priorities. The phases are planning stages rather than fixed deadlines.

## Phase 1: Establish Governance

**Objective:** Define accountability, scope, and programme priorities.

Key activities:

- Assign an accountable executive sponsor and programme owner.
- Establish responsibilities across cybersecurity, enterprise architecture, infrastructure, application teams, procurement, and risk management.
- Define scope and reporting requirements.
- Identify critical business services and relevant stakeholders.
- Establish a mechanism for tracking decisions, risks, dependencies, and progress.

**Expected outcomes:** Approved scope, assigned ownership, governance arrangements, and an initial programme plan.

## Phase 2: Discover Cryptographic Dependencies

**Objective:** Establish a reliable view of where cryptography is used.

Key activities:

- Build and validate the cryptographic inventory.
- Identify algorithms, protocols, certificates, key-management systems, and relevant dependencies.
- Engage technology vendors and service providers to establish available product information.
- Identify gaps in discovery coverage and assign follow-up actions.
- Record evidence and distinguish confirmed findings from assumptions.

**Expected outcomes:** A maintained inventory, documented discovery gaps, and a view of critical dependencies.

## Phase 3: Assess Risk and Prioritize

**Objective:** Determine where further assessment and migration planning should begin.

Key activities:

- Assess business criticality and data confidentiality requirements.
- Identify relevant dependencies on quantum-vulnerable public-key cryptography.
- Consider long-lived sensitive data and potential harvest-now-decrypt-later exposure.
- Assess migration complexity, vendor constraints, and interoperability requirements.
- Apply the risk prioritization matrix and document material exceptions.

**Expected outcomes:** A prioritized set of assets, documented risk decisions, and an agreed sequence for further investigation.

## Phase 4: Evaluate Architecture and Migration Options

**Objective:** Establish technically appropriate migration approaches.

Key activities:

- Review applicable post-quantum cryptography standards and current implementation guidance.
- Engage vendors on product support, upgrade paths, and lifecycle commitments.
- Evaluate compatibility with existing applications, protocols, hardware, and external integrations.
- Define architecture options and identify systems requiring redesign.
- Assess operational, performance, resilience, and support implications.

**Expected outcomes:** Documented architecture decisions, dependency plans, vendor actions, and candidate systems for controlled testing.

## Phase 5: Test and Validate

**Objective:** Establish that proposed changes meet technical and business requirements before production deployment.

Key activities:

- Define test scope, acceptance criteria, and accountable approvers.
- Test interoperability, performance, application compatibility, and operational resilience.
- Validate implementation against applicable standards and vendor guidance.
- Assess monitoring, incident response, rollback, and recovery requirements.
- Record findings and resolve material issues before approval.

**Expected outcomes:** Test evidence, documented exceptions, approved implementation approaches, and deployment recommendations.

## Phase 6: Implement and Transition

**Objective:** Introduce approved changes through controlled implementation.

Key activities:

- Sequence implementation according to risk, dependencies, and business priorities.
- Coordinate application, infrastructure, vendor, and operational changes.
- Maintain change control and rollback arrangements.
- Validate deployed configurations and operational readiness.
- Update architecture records, cryptographic inventories, and support documentation.

**Expected outcomes:** Validated implementations, updated records, operational handover, and tracked residual risks.

## Phase 7: Govern and Improve

**Objective:** Maintain oversight as standards, technology, and organizational dependencies evolve.

Key activities:

- Review programme progress and material risks with accountable stakeholders.
- Track inventory coverage, unresolved dependencies, testing outcomes, and implementation progress.
- Reassess priorities when business requirements, technology, vendor support, or relevant guidance changes.
- Monitor emerging standards and cryptographic developments.
- Maintain accountable owners and target dates for outstanding actions.

**Expected outcomes:** Ongoing oversight, transparent progress reporting, and a maintained migration plan.

## Executive Oversight

Management reporting should focus on decisions and material risks rather than activity counts alone.

Recommended reporting indicators include:

- Percentage of in-scope systems inventoried and validated.
- Number of critical systems with unresolved cryptographic dependencies.
- Status of vendor readiness and major technology constraints.
- Progress of approved testing and implementation activities.
- Material risks, accepted exceptions, overdue actions, and required executive decisions.

Metrics should have clear definitions, accountable owners, and an agreed reporting frequency.

## Programme Principles

- Prioritize using evidence and business risk.
- Avoid assuming that all cryptographic assets require the same migration approach.
- Align implementation decisions with applicable standards and validated technical options.
- Maintain accountability for unresolved risks and dependencies.
- Treat migration as a managed programme rather than a one-time technology upgrade.

## Limitations

This roadmap is a planning framework. It does not prescribe universal migration dates or guarantee that a particular approach is suitable for every environment. Detailed implementation requires organization-specific assessment, specialist cryptographic expertise, and validation against current standards and product capabilities.
