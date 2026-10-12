# PQC Assessment Scoring Guide

## Purpose

This guide provides a consistent approach to interpreting the Post-Quantum Cryptography (PQC) Readiness Questionnaire and translating assessment findings into practical improvement actions.

The assessment is intended to support organizational planning, risk discussions, and executive oversight. It is not a certification, a formal compliance assessment, or a prediction of when cryptographically relevant quantum computers will become available.

## 1. Assessment Scoring

For each applicable question, assign a score based on the evidence available.

| Score | Assessment | Interpretation |
|---|---|---|
| 0 | Not established | No documented capability or evidence |
| 1 | Initial | Ad hoc activities with limited coverage |
| 2 | Developing | Partial implementation with identified gaps |
| 3 | Established | Documented, implemented, and supported by evidence |
| N/A | Not applicable | Excluded with a documented rationale |

A score should reflect demonstrated capability rather than planned activity or verbal assurance alone.

## 2. Calculate the Readiness Score

Calculate the percentage using applicable questions only.

**Readiness Score = Total Points Achieved / Maximum Applicable Points × 100**

The maximum applicable points equal the number of scored questions multiplied by three.

Questions marked N/A should be excluded from both the achieved points and the maximum possible points. Record the rationale for each exclusion.

If no questions are applicable, do not calculate a score.

## 3. Indicative Readiness Bands

The following bands are proposed internal screening guidance. They are not NIST-defined maturity levels or industry-standard thresholds.

| Score | Indicative Status | Suggested Response |
|---|---|---|
| 0–24% | Initial | Establish accountability, scope, and a baseline discovery plan |
| 25–49% | Developing | Address major gaps in inventory, ownership, and risk assessment |
| 50–74% | Advancing | Validate coverage, resolve dependencies, and develop migration plans |
| 75–100% | More Established | Validate evidence, test migration assumptions, and maintain governance |

A high overall score must not conceal a critical weakness in an individual control area.

## 4. Review Results by Domain

Evaluate the five questionnaire domains separately:

- **Governance and Accountability:** Confirm executive sponsorship, ownership, and decision-making responsibilities.
- **Cryptographic Discovery:** Assess whether cryptographic assets and dependencies are identified and maintained.
- **Risk and Business Impact:** Evaluate exposure, data confidentiality requirements, business criticality, and third-party dependencies.
- **Technology and Migration Readiness:** Review vendor capabilities, architecture constraints, interoperability, and testing readiness.
- **Planning and Assurance:** Confirm that migration activities have accountable owners, milestones, resources, and assurance arrangements.

Identify the weakest domains and assess whether their gaps create material business or technology risks.

## 5. Translate Findings into Actions

For each material finding, document:

| Field | Description |
|---|---|
| Finding ID | Unique reference for tracking |
| Assessment Domain | Area in which the gap was identified |
| Finding | Evidence-based description of the gap |
| Business Impact | Potential effect on confidentiality, integrity, availability, or resilience |
| Priority | Priority assigned through the risk assessment process |
| Recommended Action | Specific action required to address the finding |
| Accountable Owner | Person or function responsible for delivery |
| Target Date | Agreed completion date |
| Status | Current delivery status |
| Closure Evidence | Evidence required to confirm completion |

Prioritization should consider business impact, cryptographic exposure, data confidentiality requirements, technical dependencies, and migration complexity. A numerical score should support, not replace, professional risk judgment.

## 6. Escalation Criteria

Escalate findings through the organization's established risk governance process when they involve:

- Sensitive information that may require confidentiality over a long period.
- Critical systems with unknown or unsupported cryptographic dependencies.
- Significant third-party or supply-chain dependencies without a credible migration path.
- Migration activities that could affect service availability or regulatory obligations.
- Material gaps in ownership, funding, or executive oversight.

Escalation does not automatically mean that a system must be replaced immediately. The appropriate response depends on validated exposure, available mitigations, operational constraints, and business risk appetite.

## 7. Reporting to Executive Leadership

Executive reporting should focus on decisions and risk exposure rather than scores alone.

Suggested indicators include:

- Percentage of in-scope systems assessed.
- Number of critical systems with unresolved cryptographic dependencies.
- Number of material risks without approved treatment plans.
- Vendor readiness for relevant post-quantum cryptographic standards.
- Migration plans approved and testing milestones completed.
- Overdue remediation actions and approved exceptions.

Report the assessment scope, evidence quality, key assumptions, and significant exclusions alongside the results.

## 8. Review and Governance

Reassess readiness at agreed intervals and when significant changes occur, such as major technology transformations, new third-party dependencies, changes to data confidentiality requirements, or relevant standards and vendor developments.

Assign an accountable owner for maintaining the assessment and obtaining evidence from technology, architecture, risk, procurement, legal, and business stakeholders as appropriate.

## Limitations

This guide provides a practical assessment approach and proposed scoring interpretation. It does not establish a recognized certification or replace a detailed cryptographic inventory, technical validation, threat assessment, or formal risk assessment.

Organizations should align their implementation with applicable regulatory requirements, current standards, and guidance from recognized bodies, including NIST.
