# Requirements conservation and end-to-end traceability

**Scope:** Source normative requirements R01-R19 from `docs/02_TEST_AND_ACCEPTANCE.md` §4 (copied below with original IDs, description, design representation and test/gate text). Mapping to synthetic CPUS artifacts is **authoring/coverage**, not test execution.

| ID | Original required behavior | Original design representation | Original tests/gates | CPUS mapping | Validation |
|---|---|---|---|---|---|
| R01 | Senior cross-functional Oracle HCM+ERP/SLED advice | PI Role; OS §§1-2,4 | T01,T11,T25 / H7 | C01/C07/C10; F03/F04 | **DESIGN MAPPED; acceptance NOT RUN** |
| R02 | No invented product function or references | PI Hard 1; OS §3 | T02,T07,T22 / H2 | False-premise 1-6; F06/F10 | **DESIGN MAPPED; acceptance NOT RUN** |
| R03 | Distinguish delivered/config/design/reporting/integration/licensing | PI Hard 2; OS §§3-5 | T03,T06,T10,T21 / H2 | Fit/gap and mechanism tables; F10 | **DESIGN MAPPED; acceptance NOT RUN** |
| R04 | Official product source + release and UI match | PI Hard 3; OS §3 | T04,T07,T24 / H2,H8 | Official source ledger; F06 | **DESIGN MAPPED; acceptance NOT RUN** |
| R05 | US/Canada and statute/policy distinctions | PI Hard 4; OS §§2-3 | T05,T20 / H3 | C02/C03/C11; F05 | **DESIGN MAPPED; acceptance NOT RUN** |
| R06 | RFP classifications and defended language | PI RFP mode; OS §5.1 | T03,T23 / H5 | C10; F10 | **DESIGN MAPPED; acceptance NOT RUN** |
| R07 | Implementation, data-flow, costing/reconciliation | PI Design; OS §§4-5 | T11,T13,T22,T25 / H7 | C04-C08; F01/F04 | **DESIGN MAPPED; acceptance NOT RUN** |
| R08 | Evidence-led troubleshooting | PI Troubleshoot; OS §5.3 | T12 / H2,H7 | Retro exception workflow; F03 | **DESIGN MAPPED; acceptance NOT RUN** |
| R09 | Authentic demonstration design | PI Demo; OS §5.4 | T18,T26 / H2 | Ten-step demo; F07 | **DESIGN MAPPED; acceptance NOT RUN** |
| R10 | AI product distinctions, suitability and governance | PI AI; OS §6 | T15,T16,T17,T29 / H2,H4 | C12; F08 | **DESIGN MAPPED; acceptance NOT RUN** |
| R11 | User-only decision and no unauthorized action | PI Hard 5; OS §§6-7 | T14,T19,T23,T30 / H1,H4 | C09/C12; F08 | **DESIGN MAPPED; acceptance NOT RUN** |
| R12 | Customer-scoped state and file authority | PI Files; OS §7 | T08,T09,T30 / H1,H8 | Synthetic data scoping; F08 | **DESIGN MAPPED; acceptance NOT RUN** |
| R13 | Failure/hold without unnecessary refusal | PI Hard 6; OS §8 | T14,T21,T24 / H5 | Customer HOLD; F10 | **DESIGN MAPPED; acceptance NOT RUN** |
| R14 | Concise ordinary answers / useful deep answers | PI Output; OS §§4,8 | T01,T25,T27,T28 / H7 | Readme summary + case depth; F02 | **DESIGN MAPPED; acceptance NOT RUN** |
| R15 | Cross-disciplinary skeptical review and better outcomes | PI Method; OS §§1,4 | T11,T17,T28 / H7 | Ten-role challenge; F01-F10 | **DESIGN MAPPED; acceptance NOT RUN** |
| R16 | ABVOS hard gates and actual behavioral tests | OS §8; TA §§1-3 | T01-T30,M01-M08 / H1-H8 | T/M/H baseline in acceptance ledger; F07 | **DESIGN MAPPED; acceptance NOT RUN** |
| R17 | Deployment, source hierarchy and file access | PI Files; OS §§3,7; Deployment §2 | T08,T09,T24 + setup check / H6,H8 | Exact baseline copies + install guide; F09 | **DESIGN MAPPED; acceptance NOT RUN** |
| R18 | Separate planning, simulation and execution | PI AI; OS §6 | T14,T15,T29 / H4 | No payroll/GL writes; F08 | **DESIGN MAPPED; acceptance NOT RUN** |
| R19 | Controlled version updates/known limitations | Deployment §§3-5; audit report | Clean package validation / H6 | Manifest, release and audit; F09 | **DESIGN MAPPED; acceptance NOT RUN** |

## CPUS-specific traceability

| Scenario requirement | Answer artifacts | Fresh validation cases | External evidence or authorizer |
|---|---|---|---|
| C01 assignment/eligibility | Original §Functional architecture; Reviewed §Control 1 | CP01, CP02; T25 | HR/payroll structure; approved tenant export |
| C02 DST/meal | Original §Time and Labor; Reviewed §Control 2 | CP01, CP03 | Raw punch UTC offsets, DOL G01, governing jurisdiction |
| C03 overtime/union premium | Revised §Control 5; RFP | CP03, CP04 | CBA/workweek, payroll/legal specialists, state/federal sources |
| C04 time approval/change | Revised §Control 4 | CP05; T10,T14 | Approved time status and transfer test |
| C05 Time/Absence/Payroll | Architecture and tenant plan | CP06 | Relevant Oracle release and element/absence map |
| C06 retro/effective dates | Revised §Control 6 | CP07; T13 | Original/retro results and accounting records |
| C07 grants/funds | Revised §§Controls 7-8 | CP08; T11,T25 | Grant terms, finance and sponsor reviewers |
| C08 ledger and Projects | Solution Architecture and final | CP09; T11,T22 | SLA/GL and Projects posting/reconciliation |
| C09 security and SoD | Final §Control 10; AI example | CP11; T14,T15,T19 | Access tests and data protection policy |
| C10 RFP commitments | Original and final fit/gap tables | CP10; T03,T23 | License/release, product docs, authorized RFP signoff |
| C11 Canada localization | Original and final Ontario sections | CP10; T05 | Canadian employer policy/legislative and CRA/Service Canada |
| C12 AI governance | Final AI scope; AI example | CP11,CP12; T15,T16,T29 | Contract, roles, product+tenant permissions |

## Traceability release rule

Each source requirement has a proposed output and designated tests, but **no behavioral acceptance evidence is recorded**. Requirements conservation can be checked as a document design fact; it is not a customer-readiness approval. Source originals are authoritative and byte-preserved. Any proposed fixes appear in separate documents, never merged into the originals.
