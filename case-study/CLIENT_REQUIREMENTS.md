# CPUS synthetic client requirements — scenario contract

**Status:** DERIVED FROM the frozen master execution prompt, not an actual RFP or tenant statement. **Client:** Cascadia Public University System (CPUS), fictional public university system. **Scenario date:** October 31, 2026. This document is a structured extraction; the controlling exercise is the attached owner's execution prompt, not an Oracle implementation specification.

## Business needs and acceptance questions

| ID | Client outcome | Acceptance evidence required |
|---|---|---|
| C01 | Identify right employee/assignment population for Time and Labor, Payroll, Absence | Legal employer, payroll relationship(s), work assignments, effective dates, time profiles and eligibility with documented source |
| C02 | Resolve DST-crossing shift accurately | Original clock events, timezone/UTC offsets, compensable meal evidence, workweek boundaries and authorized expected-hours computation |
| C03 | Apply nonexempt, union and premium policies by worker group | Signed jurisdiction- and agreement-specific rules, positive/negative calculation cases; no invented overtime amount |
| C04 | Enforce approval before payroll where required | Test of reject, correction, reapproval, transfer permission and audit log |
| C05 | Map worked/absence time to payroll correctly | Consumer rules, elements, rates, absence integration and payroll run-result comparison |
| C06 | Process effective-dated corrections and retro safely | Versioned timecard, change event, retro run, correction, costing and journal record |
| C07 | Allocate to general funds and two external grants | Grant/sponsor allowability decisions, segment mappings, allocation totals and variance reports |
| C08 | Reconcile Payroll, Projects, SLA and General Ledger | Line-level provenance, journal statuses, ledger and project amounts, suspense and duplicate controls |
| C09 | Prevent unauthorized transactions and protect data | Least privilege, segregation of duties, separated approval, audit and redaction tests |
| C10 | Produce defensible RFP and demo claims | Six-way support taxonomy, sourced release/country, prerequisites, negative cases and explicit unknowns |
| C11 | Keep Ontario separate | Canadian localization/legislative review and T4/ROE acceptance independent of US W-2 configuration |
| C12 | Evaluate AI with human decisions | Deterministic alternative first, read-only proof, no self-generated payroll policy or writes |

## Population and scenario inputs (illustrative)

- Oregon and Washington campuses; a separate Ontario research affiliate; U.S. biweekly pay period; actual governing employer and workweek definitions not provided.
- Nonexempt hourly, faculty/adjunct, graduate assistants, union/non-union groups; their legal statuses/eligibility cannot be generalized.
- One synthetic nonexempt worker has two campus assignments and pay rates; split general-fund and two grant charges; a midnight-crossing Oct 31/Nov 1 Pacific shift; ambiguous repeated hour in the November 1 DST fallback; scheduled unpaid meal; holiday and differential request; approved absence; edited time after approval; later effective-dated rate change.
- No wage figures, exact in/out instants or offsets, grant authorization, bargaining agreements, licensed features, product release, tenant setup, contractual scope or customer data provided. No definitive overtime result or 90-day deployment promise is authorized.

## Six false premises to falsify

1. OTBI exception display automatically blocks time cards.
2. Owning HCM/ERP guarantees every interfund/grant transaction and posting.
3. US W-2/deduction/overtime configuration can be copied to Ontario T4/ROE work.
4. HCM subscription proves all advanced Time and Labor/Studio/Claw features are owned.
5. An ungoverned agent can approve and change payroll, costing and journals.
6. Every requirement can be labeled Fully Supported/Native with a guaranteed 90-day go-live.

## Acceptance authority

CPUS business/legal/finance owners must supply and approve policies and sign off tenant tests. The user's RFP, product, deployment, system-write and release authority remains reserved. No customer-production deployment or commitment is made by this synthetic case.
