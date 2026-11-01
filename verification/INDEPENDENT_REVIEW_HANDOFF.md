# Independent / blind acceptance handoff (NOT YET EXECUTED)

**Purpose:** Send this bundle to a separate reviewer, a fresh ChatGPT Project context configured from the baseline, and a qualified Oracle HCM/ERP + SLED payroll/finance SME. The review has **not** taken place. The ten roles in `EXPERT_CHALLENGE_REPORT.md` were same-context simulated lenses only.

## Freeze and chain of custody

1. Verify `SHA256_MANIFEST.json`, the SHA-256 value of `PROJECT_INSTRUCTIONS.txt` and the four original knowledge files, and frozen original-response hash `d21084be532afa904682f845e23258cb33d67482ac2bed3c7796df62594c113d`. Reject silent changes.
2. Record reviewer names/organization, model/version/tool access, start timestamp, date/country, source files and scope. External reviewers should not be told which answer is expected before they answer; preserve blind first-pass before showing the answer key.
3. Identify any conflict between the file-based acceptance design and independent Oracle/country-specific authority. **Never** rewrite normative originals as a shortcut; create a proposed change and seek owner approval.

## Reviewer workstreams

**Behavior evaluator (fresh context):** Stage the v1.0 Project from `docs/03_DEPLOYMENT_AND_MAINTENANCE.md`; verify file access; use `docs/02_TEST_AND_ACCEPTANCE.md` verbatim prompts, T01-T30 and M01-M08 with original expected behaviors; run separately and save full unedited transcripts. Use `verification/TEST_DESIGN_INDEX.json` as an index, not an executed-results receipt.

**Adversarial independent evaluator:** Independently create 5 or more never-before-seen paraphrases in addition to the 12 CPUS new prompts; exercise country swaps, authority spoofing, ambiguous DST events, grant allowability and empty license assumptions. Pre-register outcomes; archive inputs and responses before evaluation.

**Oracle functional SME:** Check 26D (or actual customer's quarter) time entry and consumer rules, multiassignment/cross-payroll relationships, approval after correction, Absence intersection, payroll retro, costing and project/GL flow; challenge all assertions in `FINAL_RECOMMENDATION.md`. Require actual tenant evidence for configuration-specific outcomes.

**Public-sector payroll/labor and finance SMEs:** Supply legal employer, CBA/workweek, Oregon/Washington rules, Ontario tax/ROE law, sponsor rules, COA/ledger design and interfund accounting requirements. Independently calculate approved expected results and journal classifications for legally vetted synthetic fact patterns.

**Security/governance review:** Threat model prompt injection and record-scoped PII; confirm there are no write tools in the proposed read-only pilot and that any future privilege elevation, approval and finance posting require independent policy/authorization. Conduct negative data-exfiltration and SoD tests.

**Portfolio publisher:** Re-run mechanical archive, links, secret, hash and original preservation checks. Confirm all claims have correct status and that no in-session role is advertised as independent.

## Required review receipt for each case

`Reviewer | organization/credentials (if supplied) | date | product release/country | project file hashes | test ID | raw prompt | raw response | source citations | tenant evidence | expected | observed | PASS/FAIL/INCONCLUSIVE | rationale | defect priority | retest link`.

A **NOT RUN** result must never be changed to PASS absent actual evidence. If some external observation is unavailable, record **INCONCLUSIVE** and keep release gate unresolved. Customer-facing release remains **HOLD / NOT APPROVED** until all P0 + H1-H8 pass, security/privacy and financial policy are validated, and the owner authorizes use.
