# Daily use, Oracle evidence, and human red-team ownership

**Status:** Owner-stated working practice for portfolio description, captured 2026-10-31. It is not an amendment to the five byte-preserved v1.0 source files and has not been independently acceptance-tested as an installed new policy.

## Real use and confidentiality

The Oracle Fusion Cloud HCM + ERP SLED Advisor is used regularly during professional work. It supports questions spanning functional design, configuration, implementations, RFP and demo preparation, troubleshooting, reporting, integration, and architecture. The public CPUS scenario is a **fictional confidentiality-safe demonstration**. No identifiable customer requirements, tenant evidence or employee data are published as its example.

## Product coverage

Read the authoritative [v1.0 operating standard, section 2](01_OPERATING_STANDARD.md#2-capability-coverage-search-and-reason-across-the-correct-ownership-boundary) for the complete coverage boundary. In summary: Core HR; U.S. and Canadian Payroll; Time and Labor; Workforce Scheduling; Absence; Compensation; Benefits; Talent, Recruiting and Learning; ERP/Financials, Projects, Budgetary Control and Procurement; HCM data exchange, reports and integrations; security/workflows; public-sector-specific requirements; and applicable Oracle AI capabilities. Coverage is the **scope of questions the tool can analyze**, not a statement that every feature is available to an employer.

## Strict citation-before-recommendation requirement

**Owner requirement:** Do not recommend a specific Oracle product capability, configuration, implementation step, integration pattern, report behavior, security setup, feature entitlement or licensing conclusion **without a real, relevant, attributable Oracle resource citation**.

For each material Oracle recommendation:

1. Identify the Oracle module/product and applicable country, environment, release and UI version, or label missing information explicitly.
2. Verify a real Oracle Help Center guide, Cloud Readiness/What's New publication, official Oracle API reference or authorized My Oracle Support reference with sufficient applicability. Cite title, direct link, appropriate section and release/date when identifiable.
3. Explain what the Oracle source actually establishes and what it does **not** establish. Never extrapolate generic documentation to customer-specific licensing, configuration, privileges or successful execution.
4. If no suitable Oracle reference can be verified, **withhold the product-specific recommendation as an established fact**, record `UNVERIFIED`, and give a precise research/tenant-validation action instead. No invented links, navigation, behavior, functions or RFP support claims.
5. For legal, tax, union, statutory and labor matters, authoritative primary legal and governing agreement/policy sources are additionally required. Oracle citations are not substitutes for those authorities.

The archived [`PROJECT_INSTRUCTIONS.txt`](../PROJECT_INSTRUCTIONS.txt) and [`01_OPERATING_STANDARD.md`](01_OPERATING_STANDARD.md) call for official sources and consequential-claim citations, and some archived language says *when possible*. The owner requirement above is **stricter**. The portfolio documents the requirement accurately but does not pretend the untouched v1.0 sources were rewritten or that a future stricter policy has passed fresh-context testing. A formal v1.1 Project Instruction revision and targeted regression tests would be needed to establish unconditional, enforceable behavior.

## Configuration and implementation questions

The expected answer ties a real Oracle source to the business requirement, supported mechanism, relevant setup preconditions, cross-module dependencies, security/approval impact, test evidence and unknowns. The advisor may recommend a **validation plan** without asserting unsupported product functionality. It must distinguish guidance from performing a configuration change. The human decides what, if anything, is implemented.

## Red-team accountability

**Red-team owner: the human user.** The user challenges assumptions and responses, requests stronger evidence, identifies defects and makes final accept/reject decisions. Simulated AI expert roles and prewritten adversarial cases in the CPUS study can be aids for that work. They are not evidence of an independent review, a qualified consultant signing off, or proof that the user's personal challenge procedure was executed during this publication exercise.

The user retains authorization authority for customer recommendations, RFP commitments, architecture changes, payroll, GL, security, production operations and AI actions. ChatGPT cannot grant itself transactional authority.

## Evidence and evaluation boundaries

The [citation ledger](../verification/EVIDENCE_AND_CITATIONS.md) documents limited official references checked during the CPUS exercise. The [behavioral ledger](../verification/ACCEPTANCE_RESULTS.md) records original tests as designed and not run in required fresh contexts. An archived product source is not an independently measured day-to-day citation-compliance rate. Treat the real-use statement as user-reported practice and the test status as separately documented verification.
