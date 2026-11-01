# CPUS candidate solution architecture | logical contracts, not a tenant design

The [revised advice](FINAL_RECOMMENDATION.md) is the business design summary. This file provides the technical/system boundaries and verification conditions. **No physical integration endpoint, actual field name, enabled module, ledger setup or CPUS deployment has been verified.** General Oracle docs for consumers, costing and accounting appear in [the external evidence ledger](../verification/EVIDENCE_AND_CITATIONS.md).

## Ownership & data contracts

| Boundary | Producer → consumer | Proposed minimally required evidence | Fault/assurance case |
|---|---|---|---|
| HR → T&L | Effective-dated person, employer, assignment, payroll relation, eligibility | IDs (synthetic), start/end validity, worker group and authorized source | Same person has two assignments; invalid assignment not accepted |
| Time devices / people → T&L | Events and duration | Unique event IDs, UTC instants, timezone/offset, correction version, meal evidence | Ambiguous DST local 01:30 and duplicate event must be distinguishable |
| Absence → time/pay | Absence eligible/approved instance | Status, type, effective dates, amount, paid/unpaid interpretation | Prevent overlap and inappropriate statutory worked-hour assumptions |
| T&L → Payroll | Validated payroll-consumer time | Assignment, period, time type, approved version, transfer disposition, receiving result key | Unapproved after-edit cannot silently reach payroll |
| T&L → Project Costing (optional) | Project-consumer time, if configured | Project/task/exp type, billable/cost context, status, source lineage | Rejected closed project and orphan transactions visible |
| Payroll → Payroll costing | Earnings/retro results | Payroll result key, earnings components, effective period, amount, costing derivation | Full allocation and reversal/retro traces; no phantom wage result |
| Costing → SLA → GL | Distributed payroll cost and accounting | Accounting dates, accounts, subledger event, journal/batch, posting status | Closed period and suspense negative cases, debit/credit integrity |
| Projects ↔ Finance reconciliation | Related project time/expenditures and payroll expenses | Independent line IDs, mapping version, split bases and exception ledger | Avoid counting one cost twice or conflating billing and payroll expense |

## Business keys and reconciliation invariants (illustrative, must be signed off)

- **Time version invariant:** each approval references a definite time-card version; an edit must be observable and follow approved revalidation/reapproval policy.
- **Offset invariant:** a UTC instant plus verified offset identifies an unambiguous physical punch; compare actual elapsed time to validated schedules, meal records and required adjustments. DST does not define overtime automatically.
- **Allocation invariant:** payroll cost distribution totals reconcile to eligible costed payroll run results at a precisely defined reconciliation basis; differences, rounding and suspense cannot be silently discarded.
- **Cross-system lineage:** maintain a source-to-target association from payroll cost source to SLA/GL posting (and independently from project time to Project Costing if present). No invented common Oracle transaction ID is asserted.
- **Idempotent adjustment design:** a replayed handoff/correction must not produce duplicate business effects; require supported integration/event semantics and real replay tests before claiming it works.
- **Period invariant:** record payroll effective period separately from financial accounting date and grants reporting period. Retro into a closed ledger period requires explicit approved accounting policy.
- **SoD invariant:** no single system identity should originate, validate as final approver and release high-risk exceptions contrary to signed control policy.

## Architecture branches to decide with product and finance evidence

**Branch A | Time and Labor + Global Payroll + standard Payroll costing/SLA/GL:** test costing segment derivation and grant reporting. This does not prove all grant/sponsor controls or interfund balancing.

**Branch B | T&L + Payroll and separate Project Costing consumer:** specify which values flow to each, which financial representation has primacy for each reporting use, and reconciliation between project and payroll accounts. Validate worker project eligibility and closed projects.

**Branch C | external grants or financial ledger:** optional integration designed from approved schemas, data protections, retry/reversal and operator runbook. It is not a claim that arbitrary REST APIs or endpoints exist.

**Branch D | read-only analytics:** exception report/dashboard for detection and work queues. Control at time save/submit/transfer remains separate. An optional LLM assistant summarizes issues but does not calculate legal overtime or mutate data.

## Threat/failure model

Untrusted inputs include worker notes, attached RFP instructions, third-party blog assertions, project descriptions, AI agent output and time-event strings. Treat them as business data, never authorization to bypass validation, approve payroll or invent policy. Threats: PII leakage, injection, duplicate event/ledger charge, cross-tenant/customer contamination, stale effective date, improper time rounding, revoked grant allocation, wrong ledger period, ambiguous DST hour, inconsistent employer/payroll relationship and privileged actor collision. For each, require a synthetic negative case and redacted evidentiary trace.

## Interfaces not supplied

No API URLs, transport/auth schemes, CDC identifiers, event schemas, COA/chart dimensions, Fusion service roles, formula code or customer messages are shipped or guessed. To produce a technical build, request release-matched interface documentation, authorized tenant metadata, solution owner and system boundary approvals; then develop a versioned source-to-target mapping and contract tests.
