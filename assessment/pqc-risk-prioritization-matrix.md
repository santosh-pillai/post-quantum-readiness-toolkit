# PQC Risk Prioritization Matrix

## Purpose

This matrix provides a structured approach to evaluating cryptographic exposure and prioritizing post-quantum cryptography (PQC) assessment and migration activities.

It separates cryptographic risk from migration complexity so that implementation difficulty does not automatically inflate a risk rating.

This is a preliminary assessment aid, not a standardized risk model, certification, or prediction of when a cryptographically relevant quantum computer will become available.

## 1. Cryptographic Risk Assessment

Assess each factor using a scale of 1 to 4. Base every rating on documented evidence and record the rationale.

| Score | General Interpretation |
|---|---|
| 1 | Lower concern based on current evidence |
| 2 | Moderate concern |
| 3 | Significant concern |
| 4 | High concern requiring detailed evaluation |

### Assessment Factors

| Factor | Assessment Considerations |
|---|---|
| Business Criticality | Potential business impact if the affected system or service is compromised or disrupted |
| Data Confidentiality Requirements | Data sensitivity and the period for which confidentiality must be maintained |
| Cryptographic Exposure | Dependence on cryptographic mechanisms vulnerable to relevant quantum attacks, considering their use and context |

These factors support structured judgment. They should not be treated as a validated mathematical risk model or as a probability of a successful quantum attack.

### Recording Results

| Asset ID | Business Criticality | Confidentiality Requirements | Cryptographic Exposure | Evidence and Rationale | Required Follow-up |
|---|---|---|---|---|---|
| [Asset ID] | [1–4] | [1–4] | [1–4] | [Evidence] | [Action] |

Do not calculate a combined numerical risk score unless the organization has defined, justified, and validated an appropriate methodology. Assess the factors together using professional judgment and the organization's established risk criteria.

## 2. Migration Complexity Assessment

Evaluate migration complexity separately from cryptographic risk.

| Factor | Assessment Considerations |
|---|---|
| Technical Dependencies | Legacy systems, application dependencies, and architecture constraints |
| Vendor Readiness | Vendor roadmaps, supported standards, and upgrade availability |
| Cryptographic Agility | Ability to change algorithms, protocols, and cryptographic implementations |
| Testing Requirements | Interoperability, performance, security validation, and regression testing |
| Operational Impact | Potential disruption, resource requirements, cost, and implementation constraints |

Record complexity as **Low, Moderate, High, or Not Yet Assessed**, with supporting evidence.

A high-complexity migration may require earlier planning and additional resources. It does not, by itself, establish that the underlying cryptographic exposure is high.

## 3. Prioritization Decisions

Use cryptographic risk findings, migration complexity, applicable obligations, and business constraints to determine the appropriate response.

| Priority | Indicative Decision Guidance |
|---|---|
| Priority 1 | Material exposure or urgent concern requiring prompt investigation, accountable ownership, and a documented treatment decision |
| Priority 2 | Meaningful exposure requiring planned assessment, dependency resolution, and an agreed treatment timeline |
| Priority 3 | Lower immediate concern based on available evidence, with continued monitoring and reassessment |

These priority categories are proposed internal guidance, not standardized industry or NIST classifications. Assign priorities using documented criteria and organizational risk appetite rather than an unsupported numerical threshold.

### Escalation Conditions

Escalate for further assessment when findings involve:

- Sensitive information requiring confidentiality over a long period.
- Critical systems with unknown or unsupported cryptographic dependencies.
- Significant third-party dependencies without a credible transition path.
- Material regulatory, contractual, or operational constraints.
- Unclear accountability, funding, or risk ownership.

An escalation does not automatically require immediate replacement of a cryptographic implementation. Determine the appropriate treatment based on validated exposure, available mitigations, dependencies, and business impact.

## 4. Risk Treatment Register

| Finding ID | Asset ID | Risk Finding | Priority | Treatment Decision | Accountable Owner | Target Date | Status |
|---|---|---|---|---|---|---|---|
| [ID] | [Asset ID] | [Evidence-based finding] | [Priority] | [Action] | [Owner] | [Date] | [Status] |

Document accepted risks and exceptions through the organization's established governance process, including the approving authority, rationale, review date, and any required compensating measures.

## 5. Governance and Review

- Assign an accountable owner for each material finding.
- Validate material findings with system owners and relevant technical specialists.
- Reassess priorities when new evidence, standards, vendor capabilities, or business requirements emerge.
- Track treatment actions and overdue decisions through the established risk governance process.
- Review migration complexity alongside risk findings when approving program sequencing and resource allocation.

## Limitations

This matrix is a practical screening aid. Its factors and priority categories are proposed guidance, not a validated quantitative risk model or official NIST scoring methodology.

The assessment does not predict quantum computing timelines, establish compliance, or replace detailed cryptographic discovery, technical validation, or formal enterprise risk assessment.

Organizations should align decisions with applicable regulatory obligations, current standards, and guidance from recognized bodies, including NIST.
