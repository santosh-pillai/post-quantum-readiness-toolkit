# PQC Risk Prioritization Matrix

## Purpose

This matrix helps organizations prioritize cryptographic assets for further assessment and post-quantum migration planning.

It combines business impact, data confidentiality requirements, cryptographic exposure, and migration dependencies to support consistent decisions.

The resulting priority is a planning indicator. It is not a prediction of when a cryptographically relevant quantum computer will become available, nor proof that a system is currently compromised.

## 1. Assessment Factors

Assess each asset against the following factors. Record the evidence and rationale supporting each rating.

### Business Criticality

- **1 | Low:** Limited business impact if the asset is unavailable or requires modification.
- **2 | Moderate:** Material operational impact, with established alternatives or recovery options.
- **3 | High:** Significant disruption to business services, customers, or important operations.
- **4 | Critical:** Severe impact on essential services, safety, financial stability, or major business obligations.

### Data Confidentiality Requirements

- **1 | Limited:** Information has little long-term confidentiality requirement.
- **2 | Moderate:** Confidentiality is required for a defined period.
- **3 | High:** Sensitive information must remain confidential for many years.
- **4 | Very high:** Highly sensitive information has a long confidentiality requirement or significant consequences if disclosed in the future.

Consider the data's required confidentiality period, not only its current classification.

### Cryptographic Exposure

- **1 | Low:** No material dependency on quantum-vulnerable public-key cryptography has been identified, based on documented evidence.
- **2 | Moderate:** Limited or indirect dependencies exist, or exposure is subject to further validation.
- **3 | High:** Relevant public-key cryptography is confirmed in a significant system or data flow.
- **4 | Very high:** Material dependence on quantum-vulnerable public-key cryptography is confirmed in a critical service or sensitive data flow.

Unknown configurations must be recorded as unknown. They must not automatically receive the lowest rating.

### Migration Complexity

- **1 | Low:** Dependencies are understood and changes appear straightforward to test.
- **2 | Moderate:** Some application, protocol, or vendor coordination is required.
- **3 | High:** Multiple integrations, legacy systems, or hardware dependencies complicate migration.
- **4 | Very high:** Migration requires substantial redesign, extensive coordination, or resolution of significant compatibility constraints.

Higher migration complexity increases the need for early planning. It does not, by itself, mean an asset has greater cryptographic exposure.

## 2. Initial Priority Calculation

For an initial screening exercise, calculate:

**Priority score = Business criticality + Data confidentiality requirements + Cryptographic exposure + Migration complexity**

The possible score ranges from 4 to 16.

Use the following indicative bands:

- **13 to 16 | Priority 1:** Early review and migration planning.
- **9 to 12 | Priority 2:** Planned assessment and dependency analysis.
- **4 to 8 | Priority 3:** Maintain visibility and review as evidence develops.

These bands are a proposed starting point for this toolkit, not a standardized industry scoring model.

## 3. Override and Escalation Rules

Do not rely on the total score alone.

Escalate an asset for prompt review when:

- Sensitive data must remain confidential for a long period and relevant cryptographic exposure is confirmed.
- A critical business service depends on cryptography that requires post-quantum assessment.
- Important cryptographic dependencies remain unknown.
- A vendor, protocol, or hardware constraint could materially delay migration.
- Regulatory obligations, contractual commitments, or an identified threat require earlier action.

Document the reason for any override and obtain the appropriate risk-owner approval.

## 4. Decision and Action Register

For each assessed asset, record:

- Asset identifier and accountable owner.
- Assessment evidence and identified cryptographic dependencies.
- Ratings for each factor and the resulting priority.
- Key assumptions, uncertainties, and escalation decisions.
- Recommended action, responsible owner, and target date.
- Review status and approval history.

Recommended actions may include additional discovery, vendor engagement, architecture review, controlled testing, migration planning, or a documented decision to defer action with appropriate risk oversight.

## 5. Governance and Review

Review priorities when material changes occur in technology, business criticality, data sensitivity, threat intelligence, vendor support, or relevant standards.

Use the results to inform management decisions, resource allocation, and migration sequencing.

A priority rating should always be supported by evidence and a documented rationale.

## Limitations

This matrix is an initial screening tool. It does not replace a formal risk assessment, detailed cryptographic analysis, or specialist engineering validation.

The score is not a measure of the probability or timing of a quantum attack. Migration decisions must account for the specific cryptographic function, system architecture, applicable standards, and validated implementation options.
