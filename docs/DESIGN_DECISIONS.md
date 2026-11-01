# Design decision record (ADR register)

**Provenance:** ADRs below are DERIVED engineering rationale informed by the v1.0 governing instructions and operating standard; not proof of an Oracle tenant build. Proposed changes do not alter the four originals.

| ID | Decision | Why / tradeoff | Rejected alternative | Revisit trigger |
|---|---|---|---|---|
| ADR-01 | Short governing instruction core + four knowledge files | Keeps authority, support/verification and deployment distinct; avoids large conflicting instruction block | One monolithic prompt with unbounded source mix | Repeated behavioral regressions or context limitation |
| ADR-02 | Risk-tiered LIGHT / STANDARD / HIGH-ASSURANCE reasoning | Ordinary definitions can be concise, payroll/RFP/AI writes demand evidence and controls | Every prompt gets full audit, or every prompt gets quick answer | Tests T01/T27 or critical P0 fail |
| ADR-03 | Strict provenance classes and release qualifier | Product doc ≠ customer enabled feature; source trust separated from owner policy | Treat search snippet/marketing as customer truth | New official doc/release or tenant evidence |
| ADR-04 | Six RFP categories with ‘Requires validation’ for unknown | Avoids unsupported native/Yes while allowing a technical path | Blanket Fully Supported or outright unsupported for unknown | Formal gap proof by Oracle owner and customer SMEs |
| ADR-05 | Deterministic rules, approval and reporting before agentic action | Payroll/finance policy and transaction math need audit and accountable owners | Autonomously deciding deduction/overtime/GL entries | Signed policy, approved tools, testing and business case |
| ADR-06 | No agent/system-write access in prototype | Prevents unauthorized sensitive payroll and financial modifications | Grant broad agent connector permissions and inferred approvals | Security/finance human authorization plus tenant test |
| ADR-07 | Explicit time→cost→SLA→GL with conditional Projects branch | Grants and ledgers involve distinct accounting representations and reconciliation | Claim automatic journal generation by owning HCM+ERP | Verified COA, source mappings and journal tests |
| ADR-08 | DST time-event instants with offsets and workweek policy | Fall-back repeated hour and two rates make local time insufficient | Compute exact overtime from schedule labels | Actual punches + legal/CBA workweek and tests |
| ADR-09 | Freeze first answer before ten roles; preserve change record | Prevents retroactively pretending first answer was stronger; makes challenge inspectable | Replace original with revised final | New independent first-pass trial |
| ADR-10 | Preserve 30+8 and 8 hard gates as designed/unrun | Keeps test specs from masquerading as evidence; hard gates block scores | “38 tests passed” with no fresh-chat transcript | Completed actual test receipts |
| ADR-11 | Portfolio GitHub release ≠ customer use approval | Documentation can be accurate without a tenant or legal opinion | Call portfolio zip Oracle-certified/production-ready | External acceptance and human signoff |
| ADR-12 | Versioned exact original source bytes + hash checks | Provenance/audit integrity; minimizes accidental policy changes | Cosmetic rewrite of original instructions/files | Owner-approved v1.1 change process |

## Owner-directed practice and human review

**Current practice to describe:** This is a daily-use professional advisor across the full HCM and connected ERP coverage, with configuration and implementation guidance among its primary applications. The owner personally performs red-team challenge and final acceptance review. The owner also specifies a stricter rule than some archived v1.0 wording: every material Oracle-specific recommendation needs a real, directly relevant Oracle citation before being presented as supported. If that source is unavailable, withhold the factual recommendation and state a validation step. See [daily-use standard](DAILY_USE_AND_EVIDENCE_STANDARD.md).

These statements describe owner direction and reported use, not a completed change to the five source originals or demonstrated compliance in every session. The AI-generated ten-role CPUS challenge remains a distinct same-context exercise.

## Design repair proposals (NOT applied to baseline)

- **P-01:** Add a standard evidence-table output field for `Oracle release / country / customer entitlement / tested in tenant` with explicit UNKNOWN values. Impacts output template only, requires owner's approval and targeted T04/T06/T23 retest.
- **P-02:** Add a financial-reconciliation prompt pattern distinguishing payroll costing, Projects expenditure, SLA journal, grant compliance and source-of-truth. Validate T11/T22/T25 and CP08/CP09 after approval.
- **P-03:** Add DST duplicate-hour data evidence and no-calculation-without-policy rule to a future time-and-payroll case library, rather than claiming a universal payroll rule.
- **P-05:** For an approved v1.1 policy update, replace the v1.0 source's permissive "when possible" citation wording with the owner's strict official-Oracle-citation-before-recommendation gate. Validate response abstention, citation relevance, release applicability and failed-source cases in new fresh-context tests; do not mark it installed or passing without evidence.
- **P-06:** Attribute human-led red teaming to the owner in project documentation and distinguish it from same-context AI-simulated reviews.
- **P-04:** Enhance future agent rubric with untrusted attachment/notes injection examples, empty write-tool inventory and explicit separation of proposal vs authorization; fresh T08/T14/T15 and CP11/CP12 runs required.

These are proposed improvements, not claims of already-updated installed Project settings. The original v1.0 sources remain exact.
