# Cryptographic Inventory Guide

## Purpose

A cryptographic inventory establishes visibility into where cryptography is used across an organization's applications, infrastructure, data flows, and third-party services.

This visibility supports risk assessment, technology planning, and the transition to post-quantum cryptography where appropriate.

The inventory is a working record that should be refined as discovery progresses and systems are validated.

## 1. Establish Scope

Begin with systems that process sensitive information, support critical business services, use public-key cryptography, or depend on external cryptographic services.

Consider applications, APIs, network protocols, digital certificates, public-key infrastructure, identity services, databases, backups, hardware security modules, and third-party platforms.

The initial scope should reflect business priorities and the organization's technology environment.

## 2. Collect Inventory Information

For each identified asset, record the information available in the inventory template.

Focus on:

- **Ownership:** Identify the accountable business owner and technical contact.
- **Cryptographic use:** Record the purpose of cryptography, such as encryption, key establishment, digital signatures, or authentication.
- **Algorithm and parameters:** Capture the algorithm, key size or parameter set, protocol, and relevant configuration where verified.
- **Data sensitivity:** Record the classification and confidentiality period of the information being protected.
- **Dependencies:** Identify applications, vendors, devices, protocols, and integrations that may affect migration.
- **Discovery evidence:** Record how the information was obtained and whether it has been validated.

Do not infer an algorithm or configuration from an application name alone. Mark unknown or unverified information clearly.

## 3. Validate the Findings

Use appropriate evidence, such as configuration reviews, certificate inventories, approved architecture documentation, vendor information, software dependency analysis, and interviews with system owners.

Record unresolved gaps and assign an owner for further investigation.

Sensitive configuration data, private keys, credentials, and other secrets must not be included in the inventory or committed to a public repository.

## 4. Assess Risk and Prioritize Review

An inventory entry is not, by itself, a risk rating.

Consider the business criticality of the asset, the sensitivity and required confidentiality period of its data, the cryptographic function involved, exposure, known vulnerabilities, and the feasibility of migration.

Pay particular attention to data that must remain confidential for many years, systems that depend on vulnerable public-key cryptography, and services with complex third-party or legacy dependencies.

Prioritization should reflect the organization's threat assessment, applicable guidance, and business context. Internet exposure alone does not determine migration priority.

## 5. Record Migration Dependencies

Document compatibility constraints, vendor support, protocol dependencies, hardware limitations, performance considerations, and required testing.

Distinguish between confirmed vendor capabilities, announced plans, and information that remains unknown.

Migration decisions should be based on validated technical requirements and relevant standards, not on assumptions that every cryptographic component can be replaced in the same way.

## 6. Maintain the Inventory

Assign responsibility for maintaining each record. Review entries when systems change, certificates are renewed, vendors update their products, or new cryptographic dependencies are discovered.

Track the date of the last review and retain sufficient evidence to support decisions.

The inventory should evolve from an initial discovery exercise into a maintained organizational capability.

## Intended Outcome

A useful cryptographic inventory enables the organization to identify discovery gaps, understand dependencies, focus assessment efforts, and develop a defensible post-quantum migration plan.

It is a planning and governance resource, not a certification of cryptographic security.

## Reference

NIST Post-Quantum Cryptography Project: https://csrc.nist.gov/projects/post-quantum-cryptography
