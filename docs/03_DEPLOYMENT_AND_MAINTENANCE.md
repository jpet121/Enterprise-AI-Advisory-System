# Deployment, Use and Change Control

**Project name (suggested):** Oracle Fusion Cloud HCM + ERP — SLED Solution Advisor  
**Package version:** 1.0 | **Prepared:** 2026-10-27 | **Target:** ChatGPT Projects (no Codex, server code, or customer tenant connection required)

## 1. What is shipped

| File | Function | Placement |
|---|---|---|
| `PROJECT_INSTRUCTIONS.txt` | Short governing instructions, self-sufficient safety, operating rules and links to other files | **Paste its full contents** into Project settings → Instructions; do not upload as a knowledge file *instead of* pasting |
| `01_OPERATING_STANDARD.md` | Normative capability scope, source authority, behavior, response methods, AI governance and examples | Upload as Project source |
| `02_TEST_AND_ACCEPTANCE.md` | Behavioral oracle, negative/positive, regression tests and requirement map | Upload as Project source; *tests, not customer records* |
| `03_DEPLOYMENT_AND_MAINTENANCE.md` | Operator setup, version control and user guidance | Upload as Project source |
| `04_ABVOS_AUDITOR_REPORT.md` | Source/method decision and self-audit with unresolved limitations | Upload as Project source; *not Oracle documentation* |
| `README_FIRST.md` | Package orientation and fast installation | Local package reference; upload optional |
| `SHA256SUMS.txt` | Integrity for release files | Local check, not normative Project knowledge |

The Project Instructions deliberately remain short; the operating file holds detail. Do **not** paste the long operating file into the Project Instructions field. Do **not** upload both raw ABVOS ZIP archives and the entire Oracle brief into the live Project unless you explicitly need provenance research: redundant policy sources create conflicts and waste context. These originals are design inputs, not runtime requirements.

## 2. Setup in ChatGPT

1. In ChatGPT, choose **New project** and give it the suggested name. The OpenAI Help Center currently describes project creation and instructions under the sidebar and **Project settings**: https://help.openai.com/en/articles/10169521-projects-in-chatgpt .
2. Open the new project's **••• → Project settings**, paste **all** of `PROJECT_INSTRUCTIONS.txt` in the Project Instructions area, and save. It is approximately 3,700 characters; do not substitute the global account Custom Instructions field.
3. In project sources, upload `01_OPERATING_STANDARD.md`, `02_TEST_AND_ACCEPTANCE.md`, `03_DEPLOYMENT_AND_MAINTENANCE.md`, and `04_ABVOS_AUDITOR_REPORT.md`. Check that they appear and open. You may keep README/hash files only in the downloaded local archive.
4. Consider **Project-only memory** to reduce cross-project context leakage, where available. This setting does **not** isolate clients *within the same Project*: conversations may still reference one another. For actual confidential customer engagements, the stronger practice is a **separate customer Project with the same governing files** (subject to your organization's data and retention policies). Do not place unrelated clients' confidential tenant exports in one shared Project. Verify settings in your actual account/workspace; no package can enforce this platform control by text alone.
5. Start a new chat and send the smoke prompt below. Confirm that its answer follows scope, distinctions and file use; then run the P0 suite from `02_TEST_AND_ACCEPTANCE.md` before use for customer-facing commitments.

**Fresh-chat smoke prompt** (not a one-time boot command):

> I am preparing an RFP for a Texas public school district. The requirement is to prevent unapproved overtime from transferring to payroll and to allocate resulting costs to multiple grants. We have not supplied the Oracle release, licenses, union policies, or tenant configuration. Give your defensible initial assessment and validation plan. Do not invent setup paths.

**Expected acceptance:** no unconditional support claim, no fabricated navigation; distinguishes Time rules/approval, payroll costing/financial controls, customer-specific policy, evidence needed and tests. A concise, useful conditional response is preferred over total refusal. Confirm Project is able to consult the operating file rather than merely repeat these instructions.

## 3. Everyday usage

- **Simple question:** “Explain the distinction between payroll costing and GL posting in Fusion.”
- **RFP:** “Assess the following numbered requirements, apply six classifications, draft customer-safe language, and list proof conditions.” Attach RFP pages and known release/licensing as available.
- **Implementation:** “We need a public-university adjunct dual assignment and grant allocation flow. Identify functional ownership, integration and reconciliation tests.”
- **Troubleshooting:** “Here is the error screenshot and process history. Separate observations from hypotheses and give a check sequence.”
- **Demo:** “Build an accurate 8-minute district HR/payroll scenario with prerequisites and proof points.”
- **AI:** “Evaluate a pre-payroll exception agent versus native rules/reports, defining access, policies, decisions and approval boundaries.”

For precision supply relevant Oracle product/release, country, implemented module(s), Redwood status, licensing, customer policy, error evidence and sanitized data **when known**. These are inputs, not a mandatory questionnaire. The Project should find official public evidence itself where tools permit; it should not require you to find documentation the Project can inspect.

Do not assume a Project chat sees every uploaded file perfectly or always carries complete past-chat state. If a critical answer depends on a large or specific source, explicitly refer to its file or relevant section and ask it to cite what it used. For attached source evidence, verify extracted text/screenshots where material. If a file is not available to the model, it must say so rather than reconstruct it from a name.

## 4. Versioning and promotion

The baseline `v1.0` represents a **design-validated instruction package** that still requires **fresh-Project behavioral acceptance**. Do not call it independently verified, Oracle-certified or production proven.

For any change:

1. Record change request, source/owner authority, why it matters and expected behavior. Do not promote a vendor announcement or customer-specific fact into a universal rule.
2. Edit Project Instructions **only if** a core policy or file routing needs revision; otherwise edit the operating file. Avoid copying conflicting rules into multiple documents.
3. Update requirement map and affected tests for a material change; add at least one novel negative/metamorphic test for a repaired failure class.
4. Run static file checks, new-chat P0 tests and changed P1/regression cases. For release/AI/payroll claims, get official source and/or customer test evidence plus independent subject-matter review.
5. Record `major.minor.patch`, date, affected files, limitations, approvals and exact SHA-256 of the zipped release. Publish as a complete, immutable version. Keep a copy of previous instructions to support rollback; use Project settings to restore if regressions occur.

**Update triggers:** Oracle quarterly releases and What's New, AI Agent Studio/Claw changes, actual tenant results that disprove an assumption, legal/localization change, unsafe RFP or security failure, source hierarchy collision, new mandatory output, drift or repeated hallucination. Do not mechanically rewrite the package at every release; update only verified affected sections and tests.

## 5. Real-world evidence and final acceptance

| Gate | Required external evidence | Status at packaging |
|---|---|---|
| Files/instructions integrity | Manifest and hash check, clean ZIP extraction | See Auditor report for actual package checks |
| Fresh Project file loading | UI confirms uploads; new chat correctly consults file | **NOT RUN** (operator required) |
| P0/adversarial suite | Actual output and manual pass/fail observations | **NOT RUN** |
| Oracle capability claims | Relevant official current docs + release/country match | Only cited example references verified at build; **not every future claim** |
| Tenant/release/security claims | Customer's authorized test/screenshot/config/license evidence | **NOT AVAILABLE** |
| External customer RFP approval | User review/approval; procurement/legal/technical review if applicable | **NOT GRANTED** |
| Production Oracle operation | Customer tool permissions, explicit authorization and independent transaction controls | **OUT OF SCOPE** |

**Recovery:** If user-facing instruction behavior deteriorates, stop relying on new RFP/production-critical claims; revert to previously accepted version, rerun failing and related tests, and investigate the earliest source/authority/handoff defect. For uncertain Oracle features, isolate claim, confirm current primary product evidence, then correct the operating rule without weakening the accuracy gate.

**Operator limitation:** A ChatGPT Project cannot guarantee persistent, perfect retrieval, current Oracle knowledge or tenant authority. The governing files mandate evidence and bounded behavior; live enforcement depends on the actual model, tools, customer documentation and operator review. Do not treat an uploaded test file as proof its tests have executed.
