# Cryptographic Inventory Guide

## 1. Purpose

A cryptographic inventory establishes visibility into the cryptographic algorithms, protocols, implementations, certificates, key-management arrangements, and dependencies supporting an organization's business services.

It provides a foundation for assessing post-quantum cryptography (PQC) readiness, identifying cryptographic exposure, understanding third-party dependencies, and planning a controlled transition to quantum-resistant cryptographic standards where appropriate.

The inventory should be treated as a maintained governance and technical asset, not a one-time spreadsheet exercise.

## 2. Scope

Define the inventory scope based on business services, information assets, technology environments, regulatory obligations, and confidentiality requirements.

Consider the following areas:

- Business applications, websites, APIs, and digital services.
- Servers, endpoints, databases, middleware, and network infrastructure.
- Cloud platforms, hosted workloads, SaaS applications, and managed services.
- Cryptographic libraries, SDKs, software frameworks, and embedded components.
- Public key infrastructure (PKI), certificates, public keys, and key-management services.
- Hardware security modules (HSMs), cloud key management services (KMS), and other cryptographic appliances.
- Identity, authentication, digital signatures, secure communications, and code-signing processes.
- Backup, archival, disaster recovery, and long-term data storage.
- Third-party integrations, payment processors, external APIs, and vendor-operated systems.
- Operational technology or other specialized systems where relevant.

Document the boundaries of the assessment, exclusions, assumptions, and accountable owners. An exclusion should have a rationale and, where appropriate, a planned follow-up.

## 3. Establish Ownership and Governance

Assign responsibilities before beginning discovery.

| Role | Responsibility |
|---|---|
| Information Security | Define assessment criteria, coordinate discovery, assess exposure, and oversee governance |
| Enterprise or Solution Architecture | Identify application architecture, protocols, libraries, and technical dependencies |
| Infrastructure and Cloud Teams | Identify platform-level cryptographic capabilities and key-management arrangements |
| Application Owners | Confirm business purpose, criticality, dependencies, and service impact |
| Data Owners | Establish information sensitivity and confidentiality requirements |
| Procurement and Vendor Management | Obtain third-party information and coordinate vendor assurance |
| Risk and Compliance | Assess applicable obligations, document material findings, and oversee treatment decisions |

A person may hold more than one role in smaller organizations. Each material inventory record should have an accountable business or technology owner.

## 4. Discover Cryptographic Assets

Use multiple discovery methods because no single source is likely to provide complete coverage.

### 4.1 Automated Discovery

Where supported and authorized, use configuration analysis, software composition analysis, cryptographic discovery tools, certificate inventories, cloud configuration reviews, and network or protocol analysis.

Potential discovery sources include:

- TLS configurations and certificate stores.
- Application and operating system configurations.
- Cryptographic library dependencies and software bills of materials.
- Cloud KMS and HSM inventories.
- PKI and certificate-management platforms.
- Source code and configuration reviews.
- Infrastructure-as-code and deployment definitions.
- Approved network and protocol discovery tools.

Automated discovery can identify candidates but may miss dormant functionality, dynamically loaded components, embedded cryptography, and cryptography managed by external providers.

### 4.2 Manual Discovery

Engage application owners, architects, infrastructure teams, data owners, and vendors to identify cryptographic use that automated tools may not reveal.

Confirm the purpose of each implementation, its environment, the information it protects, and the business services that depend on it.

### 4.3 Validate Findings

Validate material findings with the relevant technical owner and supporting evidence.

Record the discovery method, evidence reference, review date, and assessment status. Distinguish confirmed findings from assumptions and unverified information.

Do not infer that an algorithm is used solely because a library is installed. Establish whether and how the implementation is used wherever practical.

## 5. Inventory Third-Party Cryptographic Dependencies

Third-party cryptographic dependencies are within scope when they support an in-scope business service, even if the organization cannot directly inspect the underlying implementation or key material.

Consider dependencies operated or managed by:

- Cloud service providers and hosted platforms.
- SaaS providers and managed application vendors.
- Software suppliers, libraries, SDKs, and embedded components.
- Payment processors, financial service providers, and external API operators.
- Managed security service providers and outsourced infrastructure teams.
- Certificate authorities, HSM providers, and key-management service providers.
- Business partners that exchange sensitive information or rely on cryptographic trust relationships.

### 5.1 Information to Capture

For each relevant third-party dependency, record the available information:

- Provider, product, business service, and internal service owner.
- Cryptographic purpose, algorithms, protocols, and implementation details disclosed by the provider.
- Key ownership and management responsibilities.
- Whether keys are customer-managed, provider-managed, or managed under a shared responsibility model.
- Certificate or key references, where available and appropriate.
- Vendor support for relevant PQC standards and migration options.
- Technical, contractual, interoperability, and upgrade dependencies.
- Evidence source, date reviewed, and unresolved information gaps.
- Accountable internal owner and follow-up action.

Record the provider's stated capabilities separately from independently validated capabilities. A vendor roadmap or written assurance is useful evidence, but it does not by itself establish that a product has implemented, enabled, or validated a particular cryptographic capability.

### 5.2 When Details Are Unavailable

If a provider does not disclose its algorithms, key parameters, implementation details, or migration plans:

1. Record the information as unknown or unverified.
2. Identify the affected service and business impact.
3. Request appropriate technical documentation, product roadmaps, security assurance, or written confirmation.
4. Document the accountable internal owner and follow-up date.
5. Evaluate the uncertainty through the organization's risk governance process.

Do not mark a dependency as ready simply because the provider does not disclose its implementation. Lack of visibility is an information gap requiring appropriate follow-up.

Do not request or store private keys, passwords, access tokens, or other secret material in the inventory. Record approved identifiers and references instead.

## 6. Complete the Inventory Template

Use the accompanying `templates/cryptographic-inventory.csv` file as the central working template.

### 6.1 Asset Identification and Ownership

Capture the asset identifier, application or system, business service, environment, asset owner, and technology owner.

Use stable identifiers wherever possible so that records can be reconciled with existing configuration management, application, certificate, and risk registers.

### 6.2 Cryptographic Implementation

Record the cryptographic purpose, algorithm or cipher, component or library, key length or parameter set, protocol or standard, and certificate or key-management arrangement.

Capture the actual implementation and usage context when available. An algorithm name alone is insufficient to establish the security posture of an implementation.

For certificate or key references, use approved identifiers or references to controlled systems. Do not put secret values in the inventory.

### 6.3 Data and Exposure Context

Record data sensitivity, the period for which confidentiality must be maintained, internet exposure, and third-party dependencies.

The confidentiality period should reflect business, legal, contractual, and regulatory requirements where applicable. It should not be inferred solely from a data classification label.

Internet exposure is one consideration in the assessment, not a complete measure of cryptographic risk.

### 6.4 Discovery and Evidence

Record the discovery method and evidence reference. Suitable evidence may include configuration exports, architecture diagrams, software dependency reports, certificate inventories, approved vendor documentation, or references to controlled assessment records.

Record enough information for an authorized reviewer to locate the evidence without copying sensitive content into the CSV.

### 6.5 Risk and Migration Planning

Use the risk assessment reference to link an inventory record to the separately documented risk finding.

Record migration complexity independently, considering technical dependencies, vendor readiness, cryptographic agility, testing requirements, and operational constraints.

Capture the target migration approach only when supported by sufficient assessment. Record an accountable remediation owner, assessment status, recommended next action, and last-reviewed date.

Do not combine migration complexity with cryptographic risk into a single score unless the organization has defined and validated an appropriate methodology.

## 7. Assess Cryptographic Exposure

Inventory discovery and risk assessment are related but distinct activities.

After identifying an asset, assess its cryptographic exposure using documented evidence and relevant business context. Consider:

- The cryptographic mechanism and how it is used.
- Whether the mechanism is vulnerable to relevant quantum attacks.
- The sensitivity of the information protected.
- How long confidentiality must be maintained.
- Business criticality and potential impact.
- External exposure and trust relationships.
- Third-party dependencies and information gaps.
- Applicable regulatory, contractual, and business obligations.

Distinguish confirmed exposure from potential exposure and unresolved uncertainty.

An inventory record is not automatically a high-risk finding simply because it uses public-key cryptography. Equally, an incomplete inventory should not be treated as proof that exposure is absent.

Use the separate PQC risk prioritization matrix to document findings, rationale, and treatment priorities.

## 8. Evaluate Migration Complexity Separately

Migration complexity helps determine implementation sequencing and resource requirements. It does not independently determine cryptographic risk.

Consider:

- Legacy architecture and application dependencies.
- Vendor support and third-party upgrade constraints.
- Cryptographic agility and algorithm replacement options.
- Interoperability and protocol compatibility.
- Performance, capacity, and operational requirements.
- Testing, validation, and rollback requirements.
- Implementation cost, resources, and service disruption.

Record the complexity assessment and its supporting evidence separately from the risk assessment.

Where an asset presents material cryptographic exposure and high migration complexity, initiate appropriate planning early. Complexity should inform the delivery strategy rather than obscure the underlying risk.

## 9. Plan Remediation and Migration

Use the validated inventory and risk findings to develop an appropriate migration plan.

Potential activities include:

- Confirming ownership and resolving discovery gaps.
- Engaging vendors to establish supported migration paths.
- Evaluating relevant standardized PQC algorithms and protocol support.
- Reviewing cryptographic agility and architecture dependencies.
- Testing compatibility, performance, interoperability, and security.
- Planning controlled deployment, rollback, and operational monitoring.
- Tracking milestones, exceptions, and residual risk through governance.

Avoid committing to a specific algorithm, product, or implementation before evaluating applicable standards, use cases, interoperability, and vendor support.

PQC migration may involve hybrid approaches or changes to protocols and supporting infrastructure. These decisions require technical validation and should not be inferred from the inventory alone.

## 10. Maintain the Inventory

The inventory should be updated when material changes occur, including:

- New applications, infrastructure, or business services.
- Changes to cryptographic libraries, algorithms, protocols, or certificates.
- New or changed cloud services and third-party dependencies.
- Changes in key ownership or management arrangements.
- Major architecture changes, acquisitions, or technology transformations.
- New evidence of vendor readiness or relevant standards developments.
- Closure of material findings or changes to migration plans.

Define review frequency according to business criticality, change velocity, applicable requirements, and risk. Record the last-reviewed date and retain evidence of material changes.

## 11. Governance and Reporting

Use the inventory to support measurable oversight, not merely to count records.

Suggested indicators include:

- Percentage of in-scope systems with validated inventory records.
- Number of critical systems with unresolved cryptographic dependencies.
- Number of third-party dependencies with unknown cryptographic details.
- Percentage of material findings with assigned owners and treatment plans.
- Coverage of vendor readiness reviews for critical services.
- Number of overdue actions and unresolved governance decisions.

Define each indicator, its data source, accountable owner, and reporting frequency. Explain significant coverage limitations alongside reported metrics.

## 12. Practical Limitations

The inventory is a living record based on available evidence. It may not capture every cryptographic implementation, especially where cryptography is embedded, dynamically invoked, or managed by third parties.

Discovery results should therefore be treated as evidence of identified assets, not proof that all cryptographic dependencies have been found.

This guide supports internal PQC readiness and migration planning. It does not establish certification, guarantee security, or demonstrate regulatory compliance by itself. Align implementation with applicable obligations and current guidance from recognized standards bodies, including NIST.

## 13. Related Resources

- [Cryptographic Inventory Template](../templates/cryptographic-inventory.csv)
- [PQC Readiness Questionnaire](../assessment/pqc-readiness-questionnaire.md)
- [PQC Risk Prioritization Matrix](../assessment/pqc-risk-prioritization-matrix.md)
- [PQC Assessment Scoring Guide](../tools/pqc-assessment-scoring-guide.md)
- [PQC Migration Roadmap](../roadmap/pqc-migration-roadmap.md)
- [PQC Executive Assessment Report Template](../templates/pqc-executive-assessment-report.md)
