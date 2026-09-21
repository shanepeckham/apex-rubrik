---
description: "Canonical HVE contract-bid scoring anchors, acceptance catalogue, gates, and award rules."
---

# Apex Dynamics Contract Bid Challenge

Judging rubric v1.0.0, 2026-09-18. Approved for packaging. Publishing the [event brief](event-brief.md) before work begins strengthens fairness and final-award readiness, but provisional TRIAGE continues from the best available identifiable candidate snapshot when event metadata is incomplete. This is an AI-assisted workshop assessment, not production certification, legal advice, or authorization to operate an emergency-response system. Humans verify the evidence and award the fictional contract.

Use the bundled [fictional interviews](interviews.md) as stakeholder evidence, the [judging prompt](judge.prompt.md) to assess one submission, and the [scorecard](scorecard.md) to record results. This rubric is the scoring authority; templates do not change it. The event brief supplies agreed operational values, scope, and execution permissions, not silent scoring overrides.

## The Challenge

Win the contract by showing that your team can turn stakeholder uncertainty into a small, tested, defensible solution using HVE Core. A beautiful dashboard is not enough. Neither is a folder full of generated plans.

The evidence chain is:

`stakeholder statement -> problem and assumption -> agreed requirement -> researched design -> reviewed plan -> change -> test -> human evaluation -> learning`

The winning bid demonstrates that chain and leaves a practice another person can repeat.

## Publish the Contract First

The existing workshop favors individual feature exploration, reusable foundations, and a path to production rather than cloud deployment. Team bidding and scored delivery are new competition rules, not pre-existing obligations.

For the fairest cross-team comparison, facilitators should publish one trusted event brief before work begins containing:

* The rubric version, interview snapshot, starter repository revision, submission deadline, and eligible team members
* The same common acceptance cases, fixtures, priority labels, and expected outcomes for every team
* A small delivery slice and any approved extensions, with measurable acceptance thresholds and agreed exclusions
* The HVE Core version or distribution available, equivalent workflow entry points, and allowed development tools
* The execution environment, permitted test commands, network access, time budget, and treatment of environment failures
* The deployment expectation: local isolated rehearsal by default; actual cloud deployment only if explicitly announced with equal resources
* The evidence submission process, reviewer access, and common correction/appeal window

Recommended common slice: receive a simulated observation, show its provenance and freshness, let a person review a response proposal, authorize a simulated dispatch, and reconstruct its outcome. A fixture-driven harness around the prototype is sufficient; rebuilding the UI or controlling real response assets is not required.

This slice and the six common cases below are a proposed addition to the original workshop, not a claim that the interviews already prescribe an implementation. If facilitators retain different individual feature tracks, approve equivalent cases and comparable difficulty before work starts, or award separate track prizes. Do not compare a documentation-only track with a delivery track on one unqualified leaderboard.

All interview-derived rows must receive a disposition: `committed`, `deferred with customer approval`, or `not applicable with customer approval`. A facilitator role-playing the customer approves these, including thresholds, before implementation. Committed requirements are prioritized `Must` or `Should`; every Must is required for contract acceptance, while incomplete Should requirements affect the score. All common critical cases are Musts. Record later changes and their timing. A team cannot remove a failing requirement after seeing its score. Contract-critical cases cannot be deferred unilaterally.

## Scoring Rules

### Weights

| ID | Dimension | Weight |
|----|-----------|--------|
| A | Design Thinking and problem framing | 15 |
| B | Business requirements and acceptance | 20 |
| C | RPI discipline and traceability | 15 |
| D | Human evaluation and judgment | 10 |
| E | Engineering hygiene and delivery readiness | 15 |
| F | Safety, security, and Responsible AI | 10 |
| G | HVE Core use and reusable harness | 10 |
| H | Teamwork and multiple perspectives | 5 |

For each dimension, assign an integer level from 0 to 4. Points equal `weight * level / 4`. Sum without intermediate rounding; report the total to two decimal places. All dimensions remain in the 100-point denominator. Approved requirement exclusions affect B's acceptance set, not dimension weights.

A, C, D, E, G, and H contribute 70 points for practice and repeatability; B and F contribute 30 for business acceptance and safety/security outcomes. The same artifact can support different claims, but its existence alone never earns repeated credit.

### Evidence Levels

| Level | Meaning | General anchor |
|-------|---------|----------------|
| 0 | Not demonstrated | Relevant evidence absent after scoped search, or contradicted without credible resolution |
| 1 | Claimed | Template, plan, self-report, or generic content with no demonstrated application |
| 2 | Applied | Specific, coherent work tied to this slice, but material verification or closure is missing |
| 3 | Verified | Complete relevant evidence chain, credible results, and human review |
| 4 | Challenged and repeatable | Level 3 plus a meaningful challenge, disposition, and successful independent reuse or retest |

Use the highest level whose own conditions hold, retaining the substantive evidence requirements of lower levels. Lower-level shortfalls are replaced, not inherited: for example, B3 retains B2's complete disposition matrix and traceability, but replaces its below-80% or unresolved-critical condition with at least 80% acceptance and all critical requirements passing. Likewise, completing verification supersedes a lower level's incomplete-verification condition. Do not average a dimension's subcriteria. Explain what prevents the next level. Honest limitations are valuable evidence of judgment, but they do not turn incomplete behavior into a pass.

Classify each evidence claim separately:

* `observed`: the judge or identified facilitator witnessed the behavior at the submitted revision
* `corroborated`: revision-linked code, results, history, or a human-reviewed record supports the claim, but this judge did not rerun it
* `claimed`: a team or generated document says it happened without adequate supporting evidence
* `missing`: a targeted search completed and found no support
* `unverified`: access, environment, time, or tool limits prevented a check; name the blocker

For unavailable evidence, retain the best supported provisional level and report `unverified`; do not silently treat it as either a pass or an actual failure. No final award while a critical check is unverified. Claimed-only evidence cannot support a level above 1. Tests need assertions against behavior and evidence of execution, not just filenames or a green badge.

### Dimension Anchors

#### A. Design Thinking and Problem Framing

* Level 2: synthesizes all four interview perspectives, names the primary beneficiary and problem, separates observations from assumptions, considers alternatives, and justifies one coherent slice.
* Level 3: links stakeholder passages to a problem statement and measurable outcome; records a real human workshop conversation or concept evaluation that influenced the chosen approach. Resolves or explicitly escalates a stakeholder tension, such as fast dispatch versus command authority.
* Level 4: compares at least two credible options with a low-fidelity test, records what evidence changed or sustained the choice, and carries that result into requirements and implementation.

Evidence may be concise synthesis notes, a journey, a concept sketch, a decision record, and feedback with a named participant or workshop alias. Fictional interviews and role-play are labelled as such, never represented as real user research. Screenshots and personas without source links are insufficient.

#### B. Business Requirements and Acceptance

First require traceability from the interview-derived obligations below to customer-agreed, testable requirements. Each committed requirement has a stable ID, owner, priority, predeclared acceptance cases, and current status. Count acceptance per requirement, not per test file: a requirement passes only when all of its mandatory cases pass.

When a mandatory case requires a human participant, non-author evaluation, or witnessed outcome, a machine result alone cannot establish that condition. Require corroborated participant/task/revision evidence. If it is unavailable, mark that case and requirement unverified and exclude the requirement from confirmed passes; do not invent a participant or label the software behavior a confirmed failure.

* Level 2: complete disposition matrix and traceability, with some committed requirements passing, but less than 80% passing or a critical requirement unresolved.
* Level 3: at least 80% of committed requirements pass and every contract-critical requirement passes; remaining gaps are explicit and cannot be disguised by a successful demo.
* Level 4: every committed requirement passes, the agreed business outcome is demonstrated in a scenario, and an independent reviewer confirms the result with a variant or adverse case.

If no committed requirement passes, the maximum is 1. Without a complete disposition matrix and testable traceability, the maximum is 1. Report both `passed / committed requirements` and `passed / contract-critical requirements`. Separately list deferred and approved-not-applicable obligations; neither counts as delivered. A smaller scope earns no automatic advantage: scope equivalence is agreed before the event.

#### C. RPI Discipline and Traceability

* Level 2: code-grounded research, a phased plan with entry/exit criteria, and bounded changes trace to one another; verification or review closure remains incomplete.
* Level 3: evidence shows research before implementation, human review of the plan before the relevant work, acceptance and risk checks planned early, checked increments, and a closed review for at least one end-to-end slice.
* Level 4: a further iteration responds to a discovered risk, failed check, changed assumption, or independent challenge; research/plan/implementation/test evidence stays synchronized and the changed behavior is reverified.

A generated retrospective is useful documentation but not proof that planning preceded code. Corroborate order through PRs, commits, dated coach checkpoints, or exported session events. Squashed history is not a penalty when equivalent evidence exists. Do not demand seven ceremonial loops; inspect the substantive loops actually needed for the agreed slice. Do not reward breaking code merely to manufacture a repair story.

#### D. Human Evaluation and Judgment

* Level 2: an identified human reviews a plan, output, or scenario with a recorded observation, but an important decision or its follow-through is missing.
* Level 3: records who evaluated what revision, using which criteria, what they accepted or challenged, and the rationale; includes both a plan checkpoint and a hands-on evaluation by a non-author or role-playing stakeholder.
* Level 4: a human challenge leads to a supported correction or reasoned acceptance, followed by a retest; another person can explain why the outcome is acceptable and what remains uncertain.

Use a compact record: `participant/role | revision | task | expected | observed | decision/reason | follow-up | retest`. A typed name or checkbox alone is not corroboration. An agent playing four personas is not four human reviewers. No private full-chat export is required. This dimension judges the development process; operational authorization is assessed under B and F.

#### E. Engineering Hygiene and Delivery Readiness

* Level 2: reproducible setup instructions, bounded changes, controlled dependencies and configuration, meaningful tests, and a documented verification command exist; execution or operational evidence is incomplete.
* Level 3: the submitted revision builds and passes applicable lint/type/test checks in the agreed environment; CI or an equivalent repeatable runner preserves results. Tests cover the touched failure paths. Setup separates secrets from examples. A release artifact or local deployment rehearsal, health check, ownership, and rollback procedure are demonstrated for the agreed slice.
* Level 4: a non-author performs the setup and verification, demonstrates a relevant failure/recovery and rollback, and confirms that an invalid fixture actually fails the gate. Operational evidence identifies the affected capability rather than merely reporting a generic error.

Inspect lockfiles where the toolchain uses them, dependency/security findings and dispositions, test assertions, PR review, error handling, audit/privacy controls, release instructions, and named operational ownership. No credit for raw code volume, commit counts, test counts, or coverage percentages without relevance. Do not mandate this teaching repository's HTML checks in a different stack. Local isolated delivery can earn full marks under the default contract; an unused deployment template cannot.

Should priority does not exempt a check from the agreed engineering verification set. If an applicable agreed check fails, E cannot reach level 3 and G4 fails, even when that check covers a Should requirement and B/G3 otherwise qualify. Distinguish a Should gap outside the agreed engineering gate from a failing check inside it using the preapproved brief, never a judging-time exclusion. For example, 8/10 acceptance with all Musts passing can support B3 while failed applicable Should checks require E2 and G4 FAIL.

#### F. Safety, Security, and Responsible AI

* Level 2: scoped threat and harm assessments identify data/tool/authority boundaries, populations affected, assumptions, mitigations, and accountable owners; enforcement or evaluation is incomplete.
* Level 3: constraints are reflected in implementation and negative tests: untrusted content cannot authorize tools, sensitive commands enforce authority at the execution boundary, uncertain recommendations reveal limitations, and high-consequence decisions retain meaningful human control. Privacy and proportionate logging are addressed.
* Level 4: an independent adverse-input exercise verifies the controls and their recovery/escalation path; fairness and uncertainty claims are supported by relevant evaluation, and remaining risk has a named human disposition.

A confidence percentage is not evidence of calibration. If no calibrated model exists, explicitly label uncertainty and abstention rules rather than inventing precision. An approval button is not sufficient if the system executes anyway, hides material changes, or prevents informed refusal. Test refusal, cancellation, changed evidence, and emergency-authority review. A justified decision not to use runtime AI is valid; evaluate the relevant system risks and the team's AI-development boundaries instead. Do not require an LLM feature to earn points.

#### G. HVE Core Use and Reusable Harness

* Level 2: identifies the actual HVE Core distribution/version and substantive workflows used, with outputs adapted to this problem and durable repository guidance for context, permitted tools, and verification.
* Level 3: selected workflow evidence is corroborated by session excerpts, coach observation, or equivalent provenance; a fresh session or second person can find the current decision, execute the checks, and use a team-created or adapted accelerator without the original chat.
* Level 4: that accelerator succeeds on a second, materially different input; a demonstrated correction becomes a scoped instruction, skill, or executable gate that prevents recurrence without unnecessary context bloat.

Installation, copied HVE files, or the phrase "we used RPI" earns at most 1. Require meaningful use of Design Thinking and an RPI workflow plus a relevant evaluation/review capability, not every historical agent name. Accept legacy task agents, skill-forward RPI, and installed-extension artifacts outside the repository when corroborated. Do not require vendoring HVE Core or a specific artifact folder. Technical resemblance alone proves practice, not tool provenance.

#### H. Teamwork and Multiple Perspectives

* Level 2: identifies contributions from at least two humans, including non-coding work, and considers more than one relevant role; the effect of collaboration is not yet verified.
* Level 3: a non-author review and a recorded disagreement or alternative materially influence a decision; role/contribution records show each team member participated in reasoning, evaluation, or delivery.
* Level 4: cross-role challenge and a handoff are corroborated; a non-author can operate or explain the slice, and each member can describe their own contribution and one decision they influenced.

Pairing notes, customer-role decisions, test observations, PR comments, and coach checkpoints are valid. One shared Git account or one keyboard is not a penalty. Multiple commit authors are not proof of collaboration. Solo participants need a predeclared peer/coach arrangement or a separate track, not invented teammates. Model personas can broaden analysis but cannot replace human participation.

## Interview-Derived Acceptance Catalogue

These are proposed requirement families derived from the supplied fictional interviews, not quotations of an agreed contract. Preserve the stakeholder and interview question as source locators in the team's matrix. Numeric thresholds, authority rules, and exception policy require facilitator/customer decisions. Never invent an SLA and attribute it to an interview.

| ID | Stakeholder evidence | Observable acceptance scenario |
|----|----------------------|--------------------------------|
| BR-01 | Maria: freshness and disrupted communications; Priya: missing data versus no threat | Stop updates beyond the agreed freshness threshold. Show last observation time, affected capability, and stale/unknown status; never silently show a current all-clear. Verify recovery does not erase the outage record. |
| BR-02 | Owen: evidence supporting and contradicting an identity; estimated times/locations | Present conflicting observations. Preserve candidate identities and source provenance, expose estimates and why confidence changed, and allow inspection without asserting a false certainty. |
| BR-03 | Owen: duplicate reports, merge/split errors, complete sequence | Replay correlated reports and a later identity correction. Correlation must not become false independent corroboration or duplicate dispatch; record and undo/resolve a mistaken merge/split without losing earlier assessments. |
| BR-04 | Priya: formats, clocks, late/batched/out-of-order data and preserved originals | Ingest mixed units/coordinates, malformed/missing fields, duplicates, and out-of-order records. Normalize or quarantine explicitly; retain raw source, event/receipt time, transformation lineage, and trace affected downstream assessments. |
| BR-05 | Maria and Elena: delegated actions versus strategic command, emergency authority | Routine actions follow the agreed delegation policy; unauthorized strategic/cross-border/public-alert actions fail at the command boundary. Authorized actions work. Emergency override requires a recorded actor/reason and visible subsequent review. |
| BR-06 | Maria: focus changes and final confirmation; Elena: informed oversight | Change the target or material evidence between proposal and confirmation. Revalidate or require renewed confirmation with target, asset, destination, rationale, and uncertainty. Cancel/refuse must produce no dispatch. |
| BR-07 | Maria: acknowledgement through outcome and radio orders; Priya: lost acknowledgements | Lose an acknowledgement, retry, disconnect/reconnect, and reconcile a simulated radio order. One logical order causes no duplicate effect; status distinguishes pending, received, acknowledged, launched/diverted, completed, and failed as relevant. |
| BR-08 | Maria: suitability, reserve and evacuation constraints; Priya: meaning of available; Elena: consequences | Compete for the last available asset and vary threat/route/shelter conditions. Enforce capacity, suitability, reserves, and agreed authorization; explain trade-offs and prevent double allocation. Account for consequences to another sector. |
| BR-09 | Elena: reconstruct decisions without hindsight; Owen: corrections/retractions | Reconstruct a decision at time T using only information available then. Retain evidence versions, uncertainty, alternatives, actor/authorization, subsequent corrections, and outcome timestamps without silently rewriting history. |
| BR-10 | Maria: public-alert wording/sectors/expiry and emergency exceptions | Issue, update, and expire an alert with authorized or explicitly recorded emergency approval. Preserve wording, sectors, expiration, and delivery status across channels; report partial delivery rather than claiming universal success. |
| BR-11 | Priya: forged observations, unauthorized commands, sensitive locations | An untrusted civilian source cannot alone escalate regional threat under the agreed trust policy. Unauthorized reads/writes fail, and responder/infrastructure data is minimized and access-controlled. Include a harmless injected instruction in retrieved content and prove it cannot grant tool authority. |
| BR-12 | Elena: objectives and value judgments; Owen: severity is not urgency | Compare a slow high-severity threat with a fast threat near a critical service. Expose objective, evidence, uncertainty, alternatives, and relevant dependencies. No autonomous life-safety commitment; a human can reject or escalate. |
| BR-13 | Elena: shared versions; Owen: changed landfall; Maria: asset availability | Change an assessment or resource status after a briefing. Relevant roles see the new version and material change, and acknowledgement/handoff state prevents assuming everyone has received it. |
| BR-14 | Priya: mixed message versions, gradual rollout, realistic traffic | Reconnect an old-version source after an upgrade. Accept through documented compatibility or reject explicitly without corrupting state. Exercise a staged rollout and rollback with representative traffic. |
| BR-15 | Maria and Elena: situation understood in seconds; Priya: role-appropriate failures | A role-playing dispatcher/commander identifies the current threat, stale information, and next authorized action within a pre-agreed target. Analyst/engineer detail remains available; critical state is not communicated only by color and the key workflow is keyboard-usable. |

BR-11's prompt-injection case also derives from the workshop security exercise. BR-15's keyboard/color checks are proposed inclusive-use acceptance details, not claims directly made in the interviews. Assess the entire family in planning, then agree a bounded, explicit requirement from it for delivery. A broad label alone is not testable scope.

For each agreed requirement, record:

`requirement ID | BR source and stakeholder passage | outcome | priority/critical? | approved scope | acceptance cases/thresholds | implementation | result at revision | human reviewer | residual risk/owner`

### Six Common Acceptance Cases

Publish fixture values, expected outcomes, and acceptance thresholds before the competition. Judges may vary values within those announced classes, but must not introduce new requirements at judging time.

| Case | Families | Contract-critical behavior |
|------|----------|----------------------------|
| K1: Feed goes quiet | BR-01 | After the declared threshold, missing updates are explicitly stale/unknown, not current safe status. Recovery is visible. |
| K2: Authority and target change | BR-05, BR-06 | Unauthorized action is denied; changed target requires reconfirmation; cancellation has no effect; the authorized path succeeds with attribution. |
| K3: Lost acknowledgement | BR-07 | Retry and reconnect produce one logical dispatch, preserving status and reconciling the simulated offline/radio record. |
| K4: What did we know then? | BR-02, BR-09, BR-13 | A later correction is visible to the affected role, but replay at the earlier time retains the earlier evidence, uncertainty, authorization, and decision. |
| K5: Untrusted instruction | BR-11 | A harmless instruction embedded in an observation/runbook remains data. It cannot elevate permission, change dispatch policy, or invoke an unauthorized action; legitimate input still works. |
| K6: Human command under uncertainty | BR-08, BR-12 | A conflicting/low-confidence proposal explains limits and resource implications, allows refusal/escalation, and cannot commit a life-safety action autonomously. |

All six are required for the recommended common slice. They do not exhaust each referenced BR family. Additional committed requirements still need their own cases. If a slice has no runtime LLM, K5 tests untrusted-input handling and absence of an authority-changing path; do not add an LLM solely to manufacture an injection test.

## Contract-Award Gates

Keep raw points and gate outcomes separate. Do not hide a safety failure with a score cap or subtract arbitrary penalties. Gate states are `PASS`, `FAIL`, or `UNVERIFIED`, with a reason and evidence reference.

| Gate | PASS condition |
|------|----------------|
| G1: Identifiable submission | The trusted rubric and candidate snapshot are identifiable. A facilitator-labelled folder or archive is sufficient; Git, a commit SHA, formal pre-approval, and a starter baseline are not required. Missing scope or baseline limits comparison confidence and attribution rather than automatically failing this gate. |
| G2: Actual HVE practice | A, C, D, and G are each at least level 3, with corroborated HVE Core use and human ownership of the submitted decisions. |
| G3: Contract acceptance | B is at least level 3. Every committed Must requirement, every K case, and any additional customer-designated critical acceptance case passes at the submitted revision. |
| G4: Runnable, bounded delivery | E and F are each at least level 3; the agreed build/verification and isolated delivery rehearsal pass. No unresolved credible critical secret exposure, privilege bypass, or autonomous life-safety action exists in the submitted path. |

Award status is `ELIGIBLE` only when all four gates pass. A confirmed failure is `NOT YET ELIGIBLE`. No failures but at least one unresolved gate is `PENDING VERIFICATION`. A suspected issue must be confirmed or left unverified, not turned into a misconduct allegation. Record secret locations privately without reproducing secret values.

An acknowledged critical gap remains a gap. Honest reporting helps A/C/D/F where appropriate but does not waive G3 or G4. A legitimate environmental failure gets the same verification opportunity for every affected team; do not remove a gate to manufacture a winner.

## Evidence Without Paperwork Inflation

One short bid index can point to existing artifacts. No required folder layout and no duplicate documents just for judging. Suggested contents:

* Team aliases/roles, contributions, starter baseline, submitted revision, HVE version, and the approved scope
* Links to problem synthesis, alternatives, requirement dispositions, risks, research, reviewed plan, and bounded changes
* One representative end-to-end evidence chain plus a later iteration or challenge
* Test commands, revision-linked results, fixtures, known failures, environment prerequisites, and release/recovery evidence
* Human evaluation records and a reusable accelerator with its second-run evidence

Commit shareable evidence or include it in the frozen submission bundle. HVE tracking output may be ignored by Git; do not assume judges can see it. Export minimal, redacted excerpts rather than private conversations or credentials. External PR/review evidence can be exported with provenance when network access is unavailable.

Distinguish inherited starter assets from team work. Reuse is encouraged: teams earn credit for selecting, applying, verifying, and improving inherited controls, not for pretending to have authored them. A complete history is helpful but not mandatory. Local timestamps and signatures are corroboration, not cryptographic proof of human participation.

## Fast Judging and Awards

Recommended budget per team: 12 minutes for evidence triage plus 8 minutes of human defense and targeted checks. This is a proposed operating budget, not a guarantee that every repository can be validated in 20 minutes. Use a pre-provisioned sandbox and revision-linked CI evidence. Long test suites run before the judging slot; critical cases cannot be assumed to pass because time ran out.

1. Record the candidate snapshot. Freeze the starter baseline, scope, and evidence bundle when available. Their absence limits confidence or comparability but does not prevent provisional TRIAGE. Keep the authoritative rubric and any brief in a facilitator-controlled location; copied attendee versions are convenience copies.
2. Start a fresh judge session with the same model/version, tools, rubric, time budget, and access for all teams. Calibration uses one facilitator-prepared reference submission, not the first competitor as an accidental standard.
3. Inspect the bid index, then independently trace one important requirement and one adverse path into code/results. Check all critical-case evidence, even if only some cases are rerun during triage. Distinguish present code from actual execution.
4. Have a person ask: "Which stakeholder conflict changed this?", "Show a human challenge and its disposition", "What happens when this acknowledgement is lost?", and "Can someone else run your accelerator on a new input?" Ask individual members about their contributions without favoring confident public speakers.
5. Before declaring eligibility, a facilitator witnesses the common critical-case harness at the frozen revision or accepts an independently witnessed, revision-linked event run. Retain the result and exceptions.
6. Preserve the AI score and any human-adjusted score with reason and evidence. A second judge reviews gates and any ranking within three points. Resolve an anchor disagreement from evidence, not by averaging unsupported opinions. Allow the same evidence-correction window for all teams; code changes require a new revision and rerun under a published rule.

Rank eligible teams by total score. For an exact tie, compare B points, then C+D+G points, then use one preannounced common scenario with a new fixture. If evidence still does not separate teams, award a joint win. An unverified team is not silently ranked below an eligible team as though its capability had been disproved.

The fictional contract goes to the strongest evidenced bid, not the most features. If no team passes the gates, award a "Preferred Bidder, Subject to Acceptance" recognition to the highest-scoring assessed team, list the conditions, and do not call the system accepted. Celebrate separate evidence-backed prizes such as "Best Problem Reframe", "Strongest Human Challenge", and "Most Reusable Harness" without bonus points or hidden changes to the rubric.

## Calibration Examples

These are illustrative scoring checks, not results from attendee repositories.

| Example | Levels A B C D E F G H | Raw score | Outcome |
|---------|----------------------|-----------|---------|
| Impressive prototype with weak process evidence | 1 2 1 0 2 1 1 1 | 31.25 | Not yet eligible; no points for polish |
| Verified workshop baseline in every dimension | 3 3 3 3 3 3 3 3 | 75.00 | Eligible only if every gate independently passes |
| Strong bid with complete business acceptance | 3 4 4 3 3 3 4 3 | 86.25 | Candidate winner, subject to gates and human confirmation |
| Excellent process but a failing critical behavior | 4 2 4 4 4 2 4 4 | 85.00 | Not yet eligible regardless of score |

A level-4 business score requires all committed requirements, not just the six common cases. A 75-point team that meets the contract can win over an 85-point team that fails a critical case. Do not infer gate passes from these level vectors alone.