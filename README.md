# Enterprise AI Advisory System
### Oracle Fusion Cloud HCM + ERP — SLED Solution Advisor

**AI-Assisted, Requirements-Driven Enterprise Advisory System Design & Evaluation**

> **What it does:** Uses a source-governed, instruction-driven ChatGPT Project to analyze Oracle Fusion HCM/ERP questions for government and education, separate documented capability from unverified customer assumptions, and draft conditional design/RFP recommendations with human authority and validation requirements.

**Why I built it:** To demonstrate how I direct an AI-assisted engineering workflow for a high-stakes enterprise-advice problem: specifying rules, challenging false certainty, preserving an original answer, designing adversarial tests, and publishing evidence rather than just persuasive outputs.

**Under the hood:** ChatGPT Project Instructions · four retained knowledge files · Oracle HCM/Payroll/Time and Labor and ERP/GL domain workflows · official-source review · six-way fit/gap classification · ABVOS-inspired behavioral gates · 10-role same-context simulated challenge · T01–T30 / M01–M08 regression test design · 12 new CPUS adversarial probes · SHA-256 artifact verification.

**Verification status:** **Portfolio artifact packaging is locally audited; the Advisor is NOT independently behaviorally accepted or Oracle-tenant validated.** The 30 original tests, 8 variants and 12 new adversarial probes are **designed, NOT RUN**. Ten reviewers are *simulated roles in one AI session*, not external human experts. I provide human red-team**.

**Name and compatibility:** **Enterprise AI Advisory System** is the portfolio title; **Oracle Fusion Cloud HCM + ERP — SLED Solution Advisor** is the technical title. The exact v1.0 instruction and knowledge files are preserved. This project contains **no Python application, custom-trained model, RAG deployment, running agent or connected Oracle tenant**.

[See the case study](case-study/CLIENT_REQUIREMENTS.md) · [Frozen first answer](case-study/EXPERT_ORIGINAL_RESPONSE.md) · [Reviewed recommendation](case-study/FINAL_RECOMMENDATION.md) · [Evaluation and limits](verification/ACCEPTANCE_RESULTS.md) · [System design](docs/SYSTEM_ARCHITECTURE.md) · [Release status](RELEASE_STATUS.md)

## At a glance

| Question | Answer |
|---|---|
| **What did I build?** | A domain-specific ChatGPT **instruction and knowledge** package, a controlled synthetic demonstration, expert challenge and a reproducible behavioral test *design*. |
| **What problem does it address?** | AI-generated enterprise advice can confuse delivered features with proposed integrations, reports with preventive controls, or vendor announcements with customer entitlement. Errors can affect payroll, grants, privacy and procurement. |
| **What skills does it show?** | Enterprise AI systems thinking, requirements/specification design, domain modeling, source provenance, stakeholder governance, risk-based decision systems, evaluation/QA design, adversarial review and technical communication. |
| **What was actually demonstrated?** | One original synthetic CPUS advisory answer, frozen before ten same-context review lenses, revised design, primary-source reference checks and local document/archive checks. |
| **What verification is missing?** | Independent fresh-chat behavioral tests (30+8), 12 CPUS adversarial runs, live Oracle product/tenant testing, qualified SME and legal/finance review and human production approval. |
| **Is it deployable Oracle software or a trained AI model?** | **No.** It is an instruction-driven advisory project and documentation, not a deployed application or autonomous agent. |

## The client-style problem

**Cascadia Public University System (CPUS) is fictional.** The scenario involves Oregon and Washington campuses, a separately governed Ontario research affiliate, nonexempt/union/faculty populations, two concurrent assignments at different pay rates, project/grant funding and a shift crossing the November 1, 2026 Pacific daylight-saving fallback. It also includes an approved absence, after-approval corrections, effective-dated pay changes and payroll costs that must reconcile to finance/GL.

The client deliberately presents six flawed requests, including that an **OTBI report automatically blocks** payroll errors, every interfund journal is automatically posted by HCM+ERP, U.S. tax setup applies to Canada, any HCM customer owns Studio/Claw features, an agent can autonomously change deductions and post journals without policy, and every RFP requirement can be guaranteed native within 90 days.

The Advisor must answer the useful solution question **without inventing overtime amounts, licenses, mapping, law, integrations or commitments**. See [complete synthetic client requirements](case-study/CLIENT_REQUIREMENTS.md).

## The demonstration — original versus reviewed

| Decision point | Frozen first-pass advisory response | After simulated expert challenge |
|---|---|---|
| Reporting versus enforcement | Explains report detects exceptions but does not itself block transactions | Adds explicit validation-action/transfer negative tests and report-as-detection rule |
| Two assignments + DST | Requests offset-qualified clock events and valid workweek policies | Adds distinct UTC instants, event identity, workweek aggregation and approval/version invariants |
| Grants, Payroll, Projects and GL | Shows candidate parallel Payroll/Project Costing paths and reconciliation | Requires explicit source-of-truth and no-double-count checks; separates project expenditure from GL expense |
| RFP representation | Uses conditional generic “Supported through configuration” on some rows | Uses **Requires validation for CPUS-specific outcomes** until license, rule and tenant proof |
| AI controls | Prefers read-only anomaly triage and human authorization | Specifies untrusted-note/prompt injection, empty write-tool inventory and separate approval boundaries |
| Verification | Ten-step demo plan **NOT RUN** | 30+8 original cases + 8 gates mapped, 12 CPUS probes **designed / NOT RUN**; independent handoff created |

The original has been preserved, not rewritten. See [frozen original](case-study/EXPERT_ORIGINAL_RESPONSE.md), [ten-role challenge and dispositions](case-study/EXPERT_CHALLENGE_REPORT.md), and [reviewed final recommendation](case-study/FINAL_RECOMMENDATION.md). **These are a same-context AI demonstration, not independent or blind acceptance.**

## How it works

```text
User / decision maker
       |
       v
ChatGPT Project short governing instructions
       |
       +--> 01 Operating Standard (module, source, work modes, authority)
       +--> 02 Test & Acceptance (test design, NOT product facts)
       +--> 03 Deployment/Maintenance (setup, change control)
       +--> 04 ABVOS Auditor Report (same-context design self-audit)
       |
       v
Scope: module, release, country, customer proof, policy, license
       |
       v
Official evidence where available + conditional architecture choices
       |
       v
Hard gates: product truth, country, authority, privacy, financial controls
       |
       +--> Supported insight + proof plan --> Human decision
       |
       +--> Unsafe / unknown claim held --> Safer alternative + next proof
```

**Functional flow for the CPUS case (logical, not tenant-verified):** HR/assignment eligibility → Time and Labor entry and calculations → approval/consumer validation → Payroll elements and retro → payroll costing → Subledger Accounting → GL; conditional Project Costing path reconciled separately to protect against grant double counting. A dashboard/report may identify a defect but cannot be equated with the control that prevents submission/transfer.

Read [system architecture](docs/SYSTEM_ARCHITECTURE.md), [CPUS solution architecture](case-study/SOLUTION_ARCHITECTURE.md), [design rationale](docs/DESIGN_DECISIONS.md) and [engineering case study](docs/ENGINEERING_CASE_STUDY.md).

## Three examples you can inspect

| Synthetic output | What it demonstrates |
|---|---|
| [RFP fit/gap](examples/RFP_FIT_GAP.md) | Six support categories, prerequisites, truthful sales wording and unproved customer entitlements |
| [Payroll-to-GL](examples/PAYROLL_TO_GL.md) | A transparently *illustrative* $1,000 accounting allocation and source-to-ledger reconciliation, not overtime math or tenant evidence |
| [Safe AI anomaly reviewer](examples/AI_AGENT_GOVERNANCE.md) | Redacted review-only proposal, no write tools, approval steps and an injected false-authority attack |

## Why this architecture

- **Control first:** deterministic business rules, approvals, reporting and reconciliation are safer than an unsupervised agent for policy-driven payroll/finance changes. Reporting and prevention have different authority and guarantees.
- **Evidence over confidence:** a current official product guide supports only its actual general claim; an applicable statute supports legal interpretation within its scope; customer-specific entitlement, policy and tenant execution need their own proof.
- **Failure is explicit:** unknown is not “native Yes” and not automatically “unsupported.” Hold the unsafe representation and provide an actionable proof path.
- **Human-directed:** I set objectives, inputs, expert perspectives, test boundaries, review requirements and retained human authorization. AI helped generate the analytical and documentation artifacts. No independent human reviewers or personal software authorship is fabricated.

## How the design was evaluated

| Evaluation activity | Scope | Actual status |
|---|---|---|
| Five original files, source versions and SHA-256 | Project Instructions + four knowledge files | **READ and COPIED**, integrity check in manifest |
| Frozen original CPUS answer | Synthetic case; initial advice | **AUTHORED and FROZEN** (one in-session demonstration) |
| Ten expert review lenses | AI Architect, Portfolio, Oracle HCM, Oracle ERP, SLED, Knowledge, QA, Security, GitHub, Auditor | **SAME-CONTEXT SIMULATED REVIEW**, not independent |
| Source check | Oracle online guides, 26D Studio docs, government wage/Canada reporting | **PUBLIC REFERENCES CHECKED**, application to CPUS unknown |
| T01–T30 original behavioral tests | Preserved verbatim and mapped | **DESIGNED / NOT RUN** in fresh chats |
| M01–M08 metamorphic variants | Preserved exact test design | **DESIGNED / NOT RUN** |
| H1–H8 critical gates | Required for customer use | **INCONCLUSIVE / HOLD** |
| CP01–CP12 adversarial payroll/GL/AI probes | New pre-registered input and expected/forbidden behaviors | **DESIGNED / NOT RUN** |
| Real Oracle tenant + independent SME/finance/legal review | Software, licenses, permissions, payroll/journals | **NOT RUN / NOT ESTABLISHED** |
| ZIP and document checks | Extraction, hashes, links, source preservation, layout | **LOCALLY AUDITED**; see [publication audit](verification/PORTFOLIO_PUBLICATION_AUDIT.md) |

No test count, score, deployment duration, economic benefit or legal conclusion is stated as measured without matching evidence. Full [acceptance ledger](verification/ACCEPTANCE_RESULTS.md), [machine-readable test design](verification/TEST_DESIGN_INDEX.json), [requirements traceability](verification/REQUIREMENTS_TRACEABILITY.md), [new adversarial probes](verification/ADVERSARIAL_TESTS.md), [official evidence](verification/EVIDENCE_AND_CITATIONS.md), [independent handoff](verification/INDEPENDENT_REVIEW_HANDOFF.md), and [limitations](verification/LIMITATIONS.md).

## Try it yourself — in a staged ChatGPT Project

This is not a CLI. A reviewer needs a ChatGPT account with **Projects** access and the ability to use the provided baseline files. No Oracle tenant is needed to inspect the synthetic demo; verified real product claims/behavior would require authorized product/tenant access.

1. Create a **new test/staging ChatGPT Project**, named for the Advisor. Read [the original deployment guide](docs/03_DEPLOYMENT_AND_MAINTENANCE.md).
2. Open [`PROJECT_INSTRUCTIONS.txt`](PROJECT_INSTRUCTIONS.txt) and **paste its exact full contents into the Project Instructions** field. Do not replace it with this README or the longer operating file.
3. Upload the four knowledge documents unchanged: [`01_OPERATING_STANDARD.md`](docs/01_OPERATING_STANDARD.md), [`02_TEST_AND_ACCEPTANCE.md`](docs/02_TEST_AND_ACCEPTANCE.md), [`03_DEPLOYMENT_AND_MAINTENANCE.md`](docs/03_DEPLOYMENT_AND_MAINTENANCE.md) and [`04_ABVOS_AUDITOR_REPORT.md`](docs/04_ABVOS_AUDITOR_REPORT.md).
4. Check source access in a fresh chat by asking for the exact `H1–H8` descriptions and the six RFP categories. Compare to originals; record model and file version; this is a **smoke check**, not the acceptance suite.
5. Ask a sanitized synthetic case: *“A fictional public university uses Oracle Time and Labor and Payroll. An OTBI report shows late time cards. Does that report itself prevent unapproved time from reaching payroll? Explain what I would validate.”* Confirm that the response separates detection, configured validations/approvals and tenant proof.
6. Run each original [`T01–T30 and M01–M08`](verification/ACCEPTANCE_RESULTS.md) **in fresh chats per source procedure**, and independently score results including hard gates, with saved complete transcripts. Run the [12 CPUS probes](verification/ADVERSARIAL_TESTS.md) separately; do **not** claim they passed just because the answer key is present here.
7. For consequential Oracle facts, verify official documentation against release, country and tenant; seek qualified finance/payroll/legal and security review. Human owner authorizes any actual customer use.

If a policy/requirement change is proposed, keep the original version and add an approved versioned successor. **This ZIP does not edit your existing Advisor Project settings.**

## Sources, responsibility and release boundary

The source set is the exact v1.0 instruction file and four knowledge files. [`04_ABVOS_AUDITOR_REPORT.md`](docs/04_ABVOS_AUDITOR_REPORT.md) records a **pre-deployment same-context design self-audit**, not independent product certification. Official Oracle and government references are linked in the [claim ledger](verification/EVIDENCE_AND_CITATIONS.md), with checked date and what each *does not* establish.

**Publication versus customer use:** The GitHub-ready **documentation portfolio** can be reviewed for design and evidence integrity. Customer-facing fit claims, actual payroll calculation, RFP signatures, AI actions and production deployment remain **HOLD / NOT APPROVED** until independent behavioral acceptance, authoritative legal/contract/product evidence, tenant validation and human approvals are complete. See [release status](RELEASE_STATUS.md) and [publication audit](verification/PORTFOLIO_PUBLICATION_AUDIT.md).

**Recruiter description:** Human-directed, AI-assisted Oracle Fusion HCM/ERP advisory system design demonstrating instruction architecture, source-aware reasoning, cross-module solution analysis, red teaming, acceptance-test design and high-stakes human governance—with unexecuted tests explicitly distinguished from real verification.

**Suggested GitHub topics:** `enterprise-ai`, `oracle-fusion`, `oracle-hcm`, `oracle-erp`, `solution-architecture`, `ai-governance`, `llm-evaluation`, `red-teaming`, `requirements-engineering`, `public-sector`.
