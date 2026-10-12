# Post-Quantum Cryptography Readiness Assessment

## Executive Report Template

**Classification:** [Internal / Confidential]  
**Organization:** [Organization Name]  
**Assessment Period:** [Start Date to End Date]  
**Report Date:** [Date]  
**Prepared By:** [Name / Function]  
**Executive Sponsor:** [Name / Role]  
**Report Version:** [Version]

> **Purpose:** Provide executive leadership with an evidence-based view of post-quantum cryptography readiness, material cryptographic exposure, migration considerations, and decisions required to manage the transition effectively.

## 1. Executive Summary

**Overall Readiness Assessment:** [Initial / Developing / Advancing / More Established]

**Assessment Scope:** [Systems, business services, environments, and third-party dependencies covered]

**Executive Summary:**  
[Summarize the current state, the most material findings, limitations in the available evidence, and the actions requiring leadership attention.]

### Key Findings

1. **[Finding 1]:** [Business impact, supporting evidence, and recommended response.]
2. **[Finding 2]:** [Business impact, supporting evidence, and recommended response.]
3. **[Finding 3]:** [Business impact, supporting evidence, and recommended response.]

### Executive Attention Required

[Identify the decisions, funding, accountable ownership, vendor engagement, or risk treatment approvals required.]

The summary should distinguish confirmed findings from assumptions, unresolved information gaps, and planned activities.

## 2. Assessment Scope and Confidence

| Assessment Item | Details |
|---|---|
| Business services in scope | [Services and business units] |
| Systems and applications in scope | [Number and description] |
| Systems assessed | [Number and percentage] |
| Third-party dependencies reviewed | [Number and scope] |
| Discovery methods | [Automated discovery, configuration review, interviews, vendor evidence] |
| Assessment period | [Dates] |
| Evidence coverage | [High / Moderate / Limited, with rationale] |
| Significant exclusions | [Excluded systems or dependencies and rationale] |
| Key assumptions | [Assumptions affecting conclusions] |
| Assessment limitations | [Known constraints and unresolved gaps] |

Explain how scope and evidence quality affect the conclusions. A high inventory coverage percentage does not necessarily demonstrate that every cryptographic implementation has been identified or validated.

## 3. Readiness Overview

| Assessment Domain | Result | Principal Observation |
|---|---|---|
| Governance and accountability | [Result] | [Finding or gap] |
| Cryptographic discovery | [Result] | [Finding or gap] |
| Risk and business impact | [Result] | [Finding or gap] |
| Technology and migration readiness | [Result] | [Finding or gap] |
| Planning and assurance | [Result] | [Finding or gap] |

**Overall Readiness Score:** [Score, if applicable]

**Interpretation:**  
[Explain what the results mean in practical terms, including material weaknesses that an aggregate score may conceal.]

If the questionnaire scoring model is used, identify the method, applicable questions, treatment of N/A responses, and limitations. Do not present proposed readiness bands as official NIST maturity levels or as proof of cryptographic security or regulatory compliance.

Review domain-level findings separately. A high overall score must not conceal a critical weakness, missing evidence, or unresolved cryptographic dependency.

## 4. Material Cryptographic Risk Findings

| Finding ID | Affected Asset or Service | Risk Finding | Business Impact | Priority | Accountable Owner |
|---|---|---|---|---|---|
| PQC-01 | [Asset or service] | [Evidence-based finding] | [Potential impact] | [Priority] | [Owner] |
| PQC-02 | [Asset or service] | [Evidence-based finding] | [Potential impact] | [Priority] | [Owner] |
| PQC-03 | [Asset or service] | [Evidence-based finding] | [Potential impact] | [Priority] | [Owner] |

Assess cryptographic risk using documented evidence of cryptographic exposure, business impact, data confidentiality requirements, and relevant dependencies. Evaluate migration complexity separately.

Use both assessments, together with applicable obligations and business constraints, to determine treatment sequencing, resource requirements, and delivery plans. Migration complexity must not independently increase the cryptographic risk rating. Do not interpret priorities as predictions of when a quantum attack will occur.

For each material finding, document the supporting evidence, affected assets, existing controls, treatment decision, accountable owner, target date, and residual risk where applicable.

## 5. Cryptographic Inventory and Exposure

Summarize the completeness and quality of the cryptographic inventory.

| Indicator | Result | Notes |
|---|---|---|
| In-scope systems identified | [Number / percentage] | [Scope and calculation] |
| Systems with validated cryptographic records | [Number / percentage] | [Evidence standard] |
| Critical systems with unresolved cryptographic dependencies | [Number] | [Principal dependencies] |
| Assets with unknown or unverified cryptographic details | [Number] | [Follow-up required] |
| Sensitive data requiring long-term confidentiality | [Findings] | [Business context] |
| Material third-party dependencies | [Number / summary] | [Providers and services] |
| Material inventory gaps | [Summary] | [Impact and next action] |

Distinguish the presence of a cryptographic library from confirmed use of that library. Record whether findings are confirmed, inferred, or still under investigation.

## 6. Third-Party and Supply-Chain Dependencies

Summarize relevant dependencies operated or managed by cloud providers, SaaS vendors, software suppliers, payment processors, managed service providers, and other external parties.

| Provider or Product | Business Service | Cryptographic Information Available | Key Management Responsibility | PQC Readiness Evidence | Outstanding Action |
|---|---|---|---|---|---|
| [Provider] | [Service] | [Known details / unknown] | [Customer / provider / shared] | [Evidence and date] | [Action and owner] |
| [Provider] | [Service] | [Known details / unknown] | [Customer / provider / shared] | [Evidence and date] | [Action and owner] |

Report material information gaps, vendor commitments, upgrade constraints, and dependencies that could affect migration planning.

Differentiate vendor statements, published roadmaps, technical documentation, and independently validated capabilities. A vendor roadmap alone does not prove that a capability has been implemented or validated.

Where details are unavailable, record the limitation and the planned follow-up. Do not assume that undisclosed cryptographic implementations are ready for PQC migration.

## 7. Migration Complexity and Delivery Constraints

Assess migration complexity separately from cryptographic risk.

| Asset or Service | Main Constraint | Complexity | Dependencies | Proposed Planning Response |
|---|---|---|---|---|
| [Asset or service] | [Legacy architecture, vendor support, interoperability, or other constraint] | [Low / Moderate / High / Not Yet Assessed] | [Dependency] | [Action] |
| [Asset or service] | [Constraint] | [Low / Moderate / High / Not Yet Assessed] | [Dependency] | [Action] |

Consider:

- Legacy architecture and application dependencies.
- Vendor support, third-party upgrade paths, and contractual constraints.
- Cryptographic agility and supported implementation options.
- Interoperability, protocol compatibility, and performance.
- Testing, validation, rollback, and operational resilience.
- Funding, staffing, and delivery dependencies.

Use these findings to plan sequencing and resources. Do not use migration complexity as a substitute for assessing cryptographic exposure.

## 8. Recommended Actions

| Action | Expected Outcome | Accountable Owner | Target Date | Status |
|---|---|---|---|---|
| Establish program governance and ownership | Clear accountability and decision rights | [Owner] | [Date] | [Status] |
| Improve cryptographic inventory coverage | Better visibility of assets and dependencies | [Owner] | [Date] | [Status] |
| Validate material cryptographic exposure | Evidence-based risk decisions | [Owner] | [Date] | [Status] |
| Resolve critical third-party information gaps | Improved vendor assurance and dependency visibility | [Owner] | [Date] | [Status] |
| Develop and validate migration plans | Controlled, tested transition approach | [Owner] | [Date] | [Status] |
| Establish executive oversight indicators | Measurable progress and escalation | [Owner] | [Date] | [Status] |

Adapt these actions to the actual findings. Do not assume that every system requires immediate cryptographic replacement.

## 9. Executive Decisions Required

| Decision | Business Rationale | Decision Owner | Required By |
|---|---|---|---|
| Approve accountable program ownership | Establish clear governance | [Role] | [Date] |
| Approve discovery and assessment resources | Resolve material visibility gaps | [Role] | [Date] |
| Confirm risk treatment and escalation approach | Align decisions with risk appetite | [Role] | [Date] |
| Support critical vendor engagement | Resolve external dependencies | [Role] | [Date] |
| Approve migration planning resources | Enable validated implementation planning | [Role] | [Date] |

**Decisions Requested:**  
[State the specific approvals, funding, risk acceptance, or direction required from leadership.]

For each request, specify the decision required, its business rationale, the accountable decision-maker, and the date by which a decision is needed.

## 10. Executive Oversight Indicators

Use a concise set of indicators that demonstrate coverage, exposure, accountability, and delivery progress.

Suggested indicators include:

- Percentage of in-scope systems with validated cryptographic inventory records.
- Number of critical systems with unresolved cryptographic dependencies.
- Number of material findings without approved treatment plans.
- Number of critical third-party dependencies with unresolved PQC readiness questions.
- Percentage of material findings with assigned owners and agreed target dates.
- Migration plans approved and validation milestones completed.
- Overdue remediation actions and unresolved governance decisions.
- Approved risk exceptions and their next review dates.

Define each indicator's calculation, source, owner, reporting frequency, and target. Explain scope limitations and evidence quality alongside the results.

## 11. Governance and Review

Document how the organization will maintain accountability and monitor progress.

**Executive Sponsor:** [Name / Role]

**Program Owner:** [Name / Function]

**Governance Forum:** [Committee or forum]

**Reporting Frequency:** [Monthly / Quarterly / Other]

**Next Review:** [Date or trigger]

Review the assessment when significant changes occur, including material architecture changes, new third-party dependencies, changes in confidentiality requirements, relevant standards developments, or new evidence of cryptographic exposure.

Record approved exceptions, residual risk decisions, accountable owners, review dates, and required compensating measures through established governance processes.

## 12. Conclusion

[Summarize the organization's readiness, material cryptographic exposure, significant information gaps, and immediate priorities.]

State the decisions required from leadership and the outcomes expected over the next reporting period.

**Report Owner:** [Name / Function]

**Prepared On:** [Date]

**Approval or Acknowledgment:** [Executive or governance forum]

## Important Notice

This template supports internal assessment and executive decision-making. It is not a certification, a guarantee of cryptographic security, or proof of regulatory compliance. Its conclusions depend on the scope, quality, and completeness of available evidence.

Risk priorities should reflect documented exposure and business context. Migration complexity should be assessed separately to support implementation planning. Align decisions with applicable obligations and current guidance from recognized standards bodies, including NIST.

## Related Resources

- [Cryptographic Inventory Template](cryptographic-inventory.csv)
- [Cryptographic Inventory Guide](../docs/cryptographic-inventory-guide.md)
- [PQC Readiness Questionnaire](../assessment/pqc-readiness-questionnaire.md)
- [PQC Risk Prioritization Matrix](../assessment/pqc-risk-prioritization-matrix.md)
- [PQC Assessment Scoring Guide](../tools/pqc-assessment-scoring-guide.md)
- [PQC Migration Roadmap](../roadmap/pqc-migration-roadmap.md)
