# Post-Quantum Cryptography Readiness Assessment

## Purpose

This assessment helps organizations evaluate their preparedness for the transition to post-quantum cryptography (PQC). It examines governance, cryptographic discovery, risk assessment, technology dependencies, migration planning, and ongoing oversight.

The assessment provides an initial view of organizational readiness. It does not establish that an organization is secure or that a particular system is vulnerable.

## Assessment Instructions

For each question, select the response that best reflects the current state and record supporting evidence.

Use the following response scale:

- **0 | Not established:** No defined process or capability is in place.
- **1 | Initial:** Activities are informal, limited, or dependent on individuals.
- **2 | Developing:** A documented approach exists but coverage or implementation is incomplete.
- **3 | Established:** The approach is implemented, documented, and supported by evidence.
- **N/A | Not applicable:** The question does not apply. Record the rationale.

An unknown or unverified state should be recorded as an assessment gap rather than treated as evidence of readiness.

## Domain 1: Governance and Accountability

**Q1. Executive ownership**

Has an accountable executive or governance body been assigned responsibility for post-quantum readiness?

Evidence: Assigned responsibilities, governance records, or approved terms of reference.

**Q2. Strategy and policy**

Has the organization established a documented approach for assessing and managing post-quantum cryptographic risk?

Evidence: Security strategy, risk policy, or approved planning documents.

**Q3. Resourcing**

Have the skills, budget, and technical resources required for discovery and migration planning been considered?

Evidence: Resource plans, project proposals, or approved budgets.

## Domain 2: Cryptographic Discovery

**Q4. Inventory coverage**

Does the organization maintain an inventory of cryptographic assets, algorithms, protocols, certificates, and relevant dependencies?

Evidence: Cryptographic inventory and defined coverage.

**Q5. Discovery process**

Are cryptographic dependencies identified through repeatable discovery activities rather than relying exclusively on manual declarations?

Evidence: Discovery procedures, configuration reviews, or tool outputs.

**Q6. Third-party visibility**

Can the organization identify relevant cryptographic dependencies within critical vendor products and external services?

Evidence: Vendor assessments, technical documentation, or contractual requirements.

## Domain 3: Risk and Business Impact

**Q7. Sensitive data longevity**

Has the organization identified information that must remain confidential for many years and considered the implications of future cryptographic compromise?

Evidence: Data classification, retention requirements, and risk assessments.

**Q8. Critical system prioritization**

Are systems prioritized according to business criticality, cryptographic use, exposure, and migration constraints?

Evidence: Risk assessments and documented prioritization criteria.

**Q9. Cryptographic risk assessment**

Has the organization assessed where quantum-capable adversaries could affect its current public-key cryptographic protections?

Evidence: Threat assessments and documented cryptographic dependencies.

## Domain 4: Technology and Migration Readiness

**Q10. Standards awareness**

Are relevant post-quantum cryptographic standards and authoritative guidance reviewed as part of technology planning?

Evidence: Standards review records and architecture guidance.

**Q11. Vendor and product readiness**

Has the organization assessed vendor roadmaps, product support, and upgrade constraints for relevant systems?

Evidence: Vendor statements, product documentation, and lifecycle plans.

**Q12. Architecture and interoperability**

Have compatibility, performance, protocol, hardware, and integration requirements been considered for migration?

Evidence: Architecture assessments, testing plans, and dependency analysis.

## Domain 5: Planning and Assurance

**Q13. Migration roadmap**

Has the organization developed a prioritized roadmap with accountable owners, dependencies, and target milestones?

Evidence: Approved roadmap or documented implementation plan.

**Q14. Testing and validation**

Has the organization defined how proposed cryptographic changes will be tested and validated before production deployment?

Evidence: Test strategy, acceptance criteria, and rollback plans.

**Q15. Ongoing oversight**

Are readiness findings, risks, and migration progress reviewed periodically by accountable stakeholders?

Evidence: Governance reports, review minutes, and tracked actions.

## Scoring Method

Score each applicable question from 0 to 3 based on documented evidence. Use N/A only when a question genuinely does not apply, and record the rationale.

Calculate the readiness score as:

**Readiness score (%) = Total points achieved ÷ Maximum applicable points × 100**

- **Total points achieved:** Sum of scores for all applicable questions.
- **Maximum applicable points:** Number of applicable questions multiplied by three.
- **N/A responses:** Exclude these questions from both the total points achieved and the maximum applicable points.
- **Unknown or unverified responses:** Record these as assessment gaps. Do not treat missing evidence as readiness or mark a question N/A solely because its status is unknown.
- **No applicable questions:** If no questions are applicable, do not calculate a readiness score.

For example, if 12 questions apply, the maximum possible score is 36. If the organization achieves 24 points, its readiness score is 66.7%.

Use the overall percentage as an indicative assessment measure, not as a measure of cryptographic security or proof of PQC compliance. Review domain-level findings and material weaknesses separately, as an overall score can conceal critical gaps.

## Interpreting Results

- **0% to 24%:** Foundational capabilities require attention.
- **25% to 49%:** Initial capabilities exist, but significant gaps may remain.
- **50% to 74%:** Developing readiness with areas requiring further improvement.
- **75% to 100%:** More established readiness processes, subject to evidence validation.

These bands are indicative and are not an industry-standard rating scale. A high overall score must not obscure a critical weakness in cryptographic discovery, sensitive data protection, or migration planning.

## Required Follow-up

For each gap, document the finding, supporting evidence, business impact, accountable owner, proposed action, and target date.

Prioritize actions based on the organization's risk exposure and business context. Escalate material risks through established governance channels.

## Limitations

This questionnaire supports an initial organizational assessment. It does not replace detailed cryptographic discovery, specialist engineering analysis, vendor validation, or an organization-specific migration strategy.
