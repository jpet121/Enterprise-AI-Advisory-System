# Synthetic example 2 | time-to-payroll-to-GL reconciliation

**Illustrative accounting numbers, not CPUS payroll, not legal overtime computation, not observed Oracle output.** The intent is to demonstrate end-to-end *verification logic*, not claim an accounting configuration was delivered.

## Input and policy boundary

Assume a **hypothetical already-validated $1,000 costed payroll earning** for a controlled test record. The amount is an *input given for an accounting illustration*, not derived from worked time or pay rates. Payroll/legal, union, time-card/absence and actual effective-date rules remain outside this calculation and must be independently approved. Proposed funding distribution:

| Finance-owned distribution | Percent | Illustrative payroll expense | Example identifier |
|---|---:|---:|---|
| General institutional fund | 60% | $600 | GENERAL-COST-01 (fictional) |
| Sponsor grant A | 25% | $250 | GRANT-A-01 (fictional) |
| Sponsor grant B | 15% | $150 | GRANT-B-01 (fictional) |
| **Total costed payroll input** | **100%** | **$1,000** | **Reconcile exactly** |

**Illustrative invariant:** `600 + 250 + 150 = 1,000`. This tests a proposed reconciliation property only. It does not determine taxes, employer liabilities, fringe, premium rates, earnings eligibility, allowability or actual Oracle costing segment derivation.

## Trace the process to evidence

```text
Time events (UTC & offsets; approved assignment/version)
  ├─[if configured]--> Project time consumer --> project expenditure records
  └─[if configured]--> Payroll time consumer --> earnings/retro results
                                           --> Payroll costing source lines
                                           --> Subledger Accounting events
                                           --> draft/final entries
                                           --> approved GL posting
Project expenditure + Payroll costing + GL actuals
  --> business-rule-specific reconciliation, not naive addition
```

| Evidence checkpoint | Illustrative assertion to test | Negative test |
|---|---|---|
| Time source | Correct single event/version and assignment; all required approvals | Replayed correction/double local hour |
| Payroll earning | $1,000 approved costed base, not overtime legal advice | Wrong eligible element or backdated rate |
| Payroll costing | General $600, Grant A $250, Grant B $150 sum to approved base | Overallocated, unmapped or default/suspense distributions |
| SLA draft and final | Reference to costed source, balanced accounting by configured method | Incorrect fund/interfund account; unapproved journal |
| GL | Final posting status and correct accounting period | Closed-period rejection, missing debit/credit or journal duplicate |
| Projects (if used) | Separate project time/expense representation reconciles to approved business interpretation | Mistakenly add Projects $250 to payroll-GL $250 and claim $500 expense |
| Grant review | Sponsor allowability and eligible grant dates are approved | Valid segment but prohibited expense; hold until reviewer signs |

### Retro example

A **synthetic** rate or assignment correction occurs after the payroll run. The possible response is *not* to revise the old $1,000 illustration in place without proof. Capture original run, correction effective date, retro event, revised results, resulting costing reversal/adjustment, SLA events and accounting date. Closed-period policy determines permissible current-period adjustment; finance validates the target ledger. Oracle documents retro/costing patterns generally; no CPUS run or posting happened. See [Oracle source ledger](../verification/EVIDENCE_AND_CITATIONS.md) (O04,O05,O08,O09).

### Financial acceptance rules (proposed)

- Whole payroll cost maps to approved distribution or an explicitly controlled suspense account; no missing or duplicated source line.
- Debit and credit totals must balance under the applicable SLA/GL configuration, but **account numbers, segments and balancing journal logic cannot be invented here**.
- Project expenditure and ledger expense are compared on a signed accounting basis; they are **not** necessarily summed as separate institutional wage expenses.
- Unknown allowable sponsor charging, unmatched journal or after-close adjustment keeps production authorization on **HOLD** until business signoff.
