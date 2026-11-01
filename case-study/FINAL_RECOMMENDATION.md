# CPUS — reviewed conditional recommendation

**State:** Revised after ten *same-context simulated* review roles. Separate from [frozen first answer](EXPERT_ORIGINAL_RESPONSE.md). **No Oracle tenant, legal opinion, payroll calculation or external independent review was completed.** All paths are logical designs until mapped and tested against the customer's product release and authorization.

## Final decision

**Recommend a phased, deterministic time-to-payroll-to-ledger control design, with an optional read-only AI anomaly reviewer.** Do not approve any blanket “Fully Supported / Native” RFP statement, universal interfund journal claim, US/Canadian configuration reuse, autonomous payroll/GL writes or a guaranteed 90-day deployment. Oracle documents relevant individual process capabilities, but CPUS-specific coverage, eligibility, entitlements and connected accounting remain **Requires validation**. Human owner approves policy, procurement and production commitments.

### Material changes relative to frozen answer

| Finding | Original first response | Reviewed correction |
|---|---|---|
| F01/F04 | Two paths shown but source-of-truth for Projects vs payroll GL unclear | Distinct payroll costing/GL and project expenditure reconciliations; independent transaction IDs and explicit no-double-count proof |
| F03 | DST capture described, but minimal cross-assignment event proof | Require event IDs, UTC instants, local offset, paid/unpaid meal actuals, campus assignment linkage and workweek grouping evidence |
| F05 | States US/Ontario/labor separation in general | Formal policy approval matrix per employer, population, jurisdiction, collective agreement and effective date; separate Canadian workstream |
| F06 | General docs with [V] tags | Link each material assertion to release/country/claim scope in evidence ledger; unknown CPUS release remains explicit |
| F07 | Tenant demo design described as not run | Distinct observation vs acceptance, unexecuted T01–T30/M01–M08, H1–H8 unresolved, ten+ case-specific probes |
| F08 | Read-only agent recommended | Reject prompt-injection authority, constrain to redacted read-only synthetic data and human-review proposals; no write tool inventory |
| F09/F02 | Technical advisory answer only | Reproducible portfolio publication, original documents, exact hashes, try-it-yourself instructions |
| F10 | Outcome categories “Supported through configuration” for CPUS rows | Reclassify CPUS-specific outcomes **Requires validation** pending entitlement and tenant demonstration; standard generic patterns explicitly documented where verified |

## Revised control architecture

```text
Policy authority by worker group / employer / workweek / effective date
                      |
                      v
HR assignment + payroll relationship + eligibility (controlled versions)
                      |
                      v
Raw time event ID, UTC instant, zone+offset, device, assignment ID
                      |                    Absence eligibility/effective dates
                      +----------------------------+
                      v
Time and Labor rules → exceptions → assignment/cost-center approvers
                      |                          |
                      |                          +--> approved corrections/version history
                      v
Validated Payroll consumer time   --> Payroll elements/rates/retro
                      |                         |
       [if configured]                         v
                      |                 Payroll costing distributions
                      v                         |
Project Costing time consumer              SLA accounting → approved GL
                      |                         |
                      +-----------+-------------+
                                  v
          Lineage & no-double-count reconciliation + grant compliance review
                                  v
                     Finance owner authorizes close
```

The two paths are *not* asserted to generate a common physical record; reconcile their separate measures and use approved source identifiers. Projects expenditure/billing cost and payroll-GL expense may describe related but not identical transactions; require finance-defined comparability and no-double-count criteria.

## Control specification and branch choices

1. **Identity and effective dates:** Verify legal employer, assignments, payroll relationship(s), time-processing group and element eligibility per effective date, including transfers and potentially distinct rate segments. If two payroll relationships exist, determine lawful pay aggregation by approved interpretation, **not** by assuming a product default. Freeze expected test master data.
2. **DST and meal:** Capture actual event UTC instants plus local timestamps and UTC offsets, employee/assignment IDs, device provenance, missing-punch flags, meal actuals and approval. For Nov 1 fallback, assert that distinct instants are not collapsed into a repeated local 01:xx label. Determine compensable worked time only under signed policy. Check the employer's workweek boundary; do not compute definitive overtime absent records.
3. **Validation that prevents vs detects:** Configure and test Time and Labor entry/calculation, consumer validation, approvals and transfer eligibility where supported for the actual rule. Report/OTBI/BI Publisher output is *detection*, not a blocking transaction mechanism. A rule may generate a warning rather than a transfer hold; confirm exact warning/error and status behavior in a tenant.
4. **Approval versioning:** Employee submits; appropriate managers/project approvers review; payroll receives only validated eligible data subject to tested workflow. Post-approval time correction must create an auditable new version, define whether resubmission is required and trigger reconciliation/retro as applicable. Never infer general rule from one test.
5. **Absence/holiday/union:** Separately validate paid/unpaid leave, meal, shift/holiday premiums, statutory compensation, overlap, multiple positions and applicable bargaining clauses. Secure business-owner approval for test expected results before execution.
6. **Payroll and retro:** Confirm rate, time elements and event groups; run controlled test with effective-dated rate change *after* original calculation, trace retro notifications and new run results. Historical results must remain auditable. Inspect payroll run result, not just a “complete” header. Oracle's U.S. retro and costing processes are documented; which CPUS route applies needs release+configuration evidence.
7. **Grants/funds:** Fund/grant/project/distribution dimensions, authoritative costing source, time allocation totals and fallback account behavior must be defined by finance and sponsor rules. A syntactically accepted grant code is not proof of allowable expense. Distinguish authorization-time controls from post-payroll grants review.
8. **SLA/GL and close:** Test accounting method, mappings, source identifiers, cost results, draft/final accounting, posting and ledger balances. Fail closed on unexplained suspense, duplicate expense or period mismatch. Closed-period retro must follow finance-approved accounting-date and adjusting-entry policy; cannot infer it automatically reopened or posted to a specific accounting period.
9. **Canadian independence:** Ontario work requires distinct legal employer/legislative payroll setup, labor policy, T4 and ROE business rules and acceptance tests; do not transfer US W-2 or tax element configuration uncritically. Whether Oracle supports the exact Canadian requirements in the chosen deployment must be verified.
10. **AI review scope:** Only after deterministic controls are demonstrated: human-approved policy corpus, allowed source list, redacted exception data, no write tools, evidence-linked anomaly observations, abstention for unknowns, separate approver for any future transaction. User retains authority.

## Final RFP language — selected outcomes

| CPUS request | Final support category | Why / proof needed |
|---|---|---|
| Policy-specific time validation, approval and Payroll consumer flow | **Requires validation** (general Oracle pattern documented) | Specific license, rule severity/transfer behavior, assignment coverage, enabled time consumers and signed acceptance test |
| Grant/project time allocation, payroll costing and GL reconciliation | **Requires validation** (standard components + potential configuration/integration) | COA and project models, integration and account derivation, grants approval, full line-level reconciliation |
| Automatic standard Oracle payroll-to-SLA accounting stages | **Supported through configuration** **only as a generic documented process**, *not a CPUS fit decision* | Oracle O05 provides process outline; CPUS mapping, permissions and actual postings unverified |
| Auto-create all interfund journals | **Requires validation** | Funds accounting design, balancing segments, accounting rules and legal/organizational structure |
| OTBI alone stops invalid time | **Not supported** as a report-only enforcement proposal | Show separate error/hold in supported transaction validation path |
| Copy U.S. payroll/W-2 configuration to Ontario/T4/ROE | **Not supported** as a valid design | Canadian statutory/localization and business-owned rules |
| AI autonomously approves payroll, changes deduction, posts GL without supplied policy | **Not supported** under stated governance design | No authorized decision rules or approval; no tool access demonstrated |
| Studio/Claw included for every HCM subscriber | **Requires validation** | 26D docs/announcement do not establish customer entitlement, roles or availability |
| Connect unsupported requirement with verified adapter | **Supported with integration or extension** only if interface feasibility proven | Approved schemas, security, error handling and tenant tests |
| Partially met complex rule with manual exception route | **Partially supported** only after verified test | Name each tested supported function and manual gap |
| Fully supported native end-to-end or 90-day guarantee | **Requires validation**; schedule/contract **not authorized** | Real scope, releases, contract, dependencies and named approvals |

**Six categories** remain: Fully supported; Supported through configuration; Supported with integration or extension; Partially supported; Not supported; Requires validation. None should be upgraded on marketing language or hypotheticals alone.

## Tenant validation sequence and hold criteria

Use the **ten-step validation design in the frozen answer** with strengthened specific proof artifacts: (1) signed subscriptions/release/roles; (2) actual assignment relationship topology; (3) raw DST offsets and double-01:xx test; (4) union/staff calculation negative cases; (5) post-approval edit/resubmission/transfer negative case; (6) leave-meal/holiday overlap; (7) payroll earning-rate verification; (8) before/after retro and cost proof; (9) two-grant and general-fund plus Projects/SLA/GL accounting and no-double-count reconciliation; (10) access/SoD, exception and complete ledger reconciliation. Each stage needs a named approver, evidence file, expected and observed outcomes, and documented remedial retest.

**STOP/HOLD** any production payroll or financial action when: no approved policy/working time evidence; no required license/access; invalid funding; failed/unapproved time data; unapproved retro; journal mismatch; unreconciled closed period; missing SoD; unsafe agent tool authority; or audit gap. **Safe predecessor:** write the implementation decision log, configure a synthetic test plan and request records, without making changes.

**Portfolio status:** documentation-level case study can be published as an illustrative, inspectable build when its artifact audit passes. **Customer-production status:** HOLD / NOT APPROVED until H1–H8/P0 fresh-chat evidence, Oracle SME review, customer release/licensing/tenant validation, security, legal and final human approval are complete.
