---
description: "Facilitator-owned event configuration and approval template for HVE contract-bid judging."
---

# Event Brief

Template status: DRAFT. Complete as much as practical before judging. Blank or `UNKNOWN` fields reduce comparison confidence or leave related gates unverified; they do not block a provisional TRIAGE score. Git hosting, commit history, formal approval dates, work-start dates, and a starter repository are optional. Keep the facilitator copy outside attendee control. This brief configures [rubric.md](rubric.md); it does not silently change scoring rules.

## Authority and Timing

| Field | Value |
|-------|-------|
| Event ID and brief version | London |
| Facilitator/customer role and approval date | UBS 9 October |
| Rules publication date and work start | OPTIONAL; record if known |
| Submission deadline and timezone | 9 October |
| Bundle/rubric version and immutable release or digest | Rubric 1.0.0; digest optional |
| Interview snapshot SHA-256 | OPTIONAL; identify the supplied interview file |
| Starter repository and immutable revision | OPTIONAL; use NONE or UNKNOWN when unavailable |
| HVE distribution/version and allowed equivalent workflows | NONE |
| Team/solo-track eligibility and peer-review arrangement | NONE |
| Scope approver and change-record location | Shane Peckham |

## Common Scope

Default slice: simulated observation -> provenance/freshness -> human response review -> authorized simulated dispatch -> outcome reconstruction. No real response assets. A fixture-driven harness is sufficient. Local isolated rehearsal is the deployment expectation unless a different equal-resource requirement is published here before work starts.

| Decision | Approved value |
|----------|----------------|
| Shared slice, beneficiaries, and measurable business outcome | REQUIRED |
| Delivery/rehearsal environment and shared resource limits | REQUIRED |
| Included requirement IDs, priorities, acceptance-case IDs, thresholds, and owners | REQUIRED; link an immutable contract matrix |
| Approved deferrals/N/A with customer rationale across BR-01..BR-15 | REQUIRED; link dispositions, or NONE if all committed |
| Authority/delegation and emergency-exception policy | REQUIRED |
| Asset availability, capacity, reserve, and escalation definitions | REQUIRED |
| Additional critical requirements/cases | REQUIRED; NONE permitted |
| Alternative tracks and equivalence approval | REQUIRED; NONE permitted |

Every committed requirement is Must or Should. Every Must and all critical cases must pass for acceptance. All K cases are Musts. K-case coverage does not automatically mean the entire associated BR family is delivered. Record case-to-requirement mappings so counts are by unique requirement ID.

Specify which checks belong to the engineering verification gate before work starts. A Should gap need not fail G3, but a failed applicable engineering check prevents E3 and fails G4 even if it tests a Should requirement. The judge cannot retroactively exclude failed checks from that set.

## Common Critical Fixtures

Supply accessible, revisioned fixtures and precise expected outcomes before work. These rows specify parameters for the rubric's cases, not permission to weaken them. Use synthetic data and simulated actions only.

| Case | Fixture and version | Parameters and expected outcomes | Requirement IDs |
|------|---------------------|---------------------------------|-----------------|
| K1 | REQUIRED | Freshness threshold, clock basis, stale/unknown display, recovery result | REQUIRED |
| K2 | REQUIRED | Roles/permissions, target-change trigger, renewed confirmation, cancellation and positive authorized path | REQUIRED |
| K3 | REQUIRED | Lost acknowledgement, retry/reconnect sequence, radio-order identity and single-effect expectation | REQUIRED |
| K4 | REQUIRED | Earlier decision and later correction times; preserved as-known-then evidence and recipient update | REQUIRED |
| K5 | REQUIRED | Benign untrusted-content fixture and expected unchanged authority; legitimate-input control | REQUIRED |
| K6 | REQUIRED | Conflicting/uncertain evidence, finite assets, explanation/refusal/escalation and no autonomous commitment | REQUIRED |

Define preannounced variant ranges for the exact-tie scenario: REQUIRED. Variation must stay within published requirements.

## Judge Environment

| Setting | Approved value |
|---------|----------------|
| Judge model/version and host/tool versions | REQUIRED; record actual values, not guesses |
| Default mode and budget | TRIAGE, 12 minutes; human defense 8 minutes; record approved changes here |
| Sandbox identity and isolation controls | REQUIRED; separate from production and without credentials |
| Network policy | NONE by default; external activity requires separate approval outside this judging prompt |
| Allowlisted commands and exact working directories | REQUIRED; NONE permitted for static triage, but runtime verification remains pending |
| Reviewed scripts, side effects, and permitted sandbox outputs | REQUIRED; NONE permitted only if no commands allowed |
| Pre-provisioned dependencies and fixtures | REQUIRED; no judge-driven installs or hooks |
| Build/check/rehearsal/rollback commands and pass conditions | REQUIRED; link allowlist entries |
| Independent human witness arrangement for critical runs | REQUIRED |
| Report destination | Chat only by default; optional facilitator-controlled path outside attendee source |
| Environment failure, evidence correction, and appeal window | REQUIRED; same opportunity for all teams |
| Code-change/new-revision and rerun policy | REQUIRED |
| Reference-submission calibration and second-judge procedure | REQUIRED; review gates and rankings within three points |

## Assessment Snapshot Records

Record one assessment snapshot per team when practical. A Git commit is optional. The facilitator may identify a local folder, copied directory, archive, or other snapshot and record the assessment time. If files may change during review, state that limitation; the judge can still produce a provisional score for the files observed.

| Team ID and member aliases/roles | Repository or folder location | Snapshot identifier or assessment time | Evidence bundle identifier/digest | Scope source/status |
|--------------------------------|-------------------------------|----------------------------------------|----------------------------------|---------------------|
| UNKNOWN | UNKNOWN | UNKNOWN | UNKNOWN | UNKNOWN |

## Human Award Process

Apply the rubric's four gates before ranking eligible teams. Exact ties use B, then C+D+G, then the preannounced variant, then a joint award if still inseparable. No eligible team means conditional preferred-bidder recognition, not contract acceptance. Preserve the AI score, any human adjustment, and its evidence. This remains a fictional workshop assessment, not authorization for emergency operations.