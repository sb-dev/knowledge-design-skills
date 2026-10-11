---
name: bootstrap-stage-execution
description: Internal execution discipline for staged Production Skills bootstraps. Used by /bootstrap to execute one stage completely, verify it, repair failures, commit it, and continue safely.
allowed-tools:
  - Read
  - Grep
  - Glob
  - Skill
  - Bash
---

# Bootstrap Stage Execution

This skill standardises execution mechanics. It does not define domain work. The governing bootstrap specification remains authoritative.

## Stage loop

For the current stage:

1. Read the complete stage in the governing bootstrap specification.
2. Read accepted prior-stage outputs that the stage depends on.
3. Derive a compact checklist covering required inputs, substantive work, outputs, exact counts/distributions, required execution/tests/evaluation, and exit criteria.
4. Perform the complete substantive work.
5. Persist the stage's durable outputs.
6. Re-read the stage requirements and verify the actual outputs against them.
7. Diagnose and repair every mandatory failure, then re-run affected verification.
8. Commit only the completed stage.
9. Push and verify the remote branch points to the intended commit and files.
10. Return control to `/bootstrap`, which determines and starts the next incomplete stage.

## Evidence rule

Never substitute:

```text
plan for execution
summary for required research
bibliography for direct-source examination
script for required script execution
prompt for required generated output
file existence for substantive validation
single favourable run for a required benchmark/comparison
model memory for required source evidence
```

Never invent research findings, repository behaviour, test passes, benchmark results, installation results, tool executions, or empirical evidence.

## Verification and repair

Verification must check substance, not filenames alone.

If a mandatory requirement fails:

```text
diagnose
→ repair the owning scope
→ re-run affected verification
→ continue
```

Do not weaken acceptance criteria, skip required work, or rewrite validators to make incomplete work pass.

An exhaustive conformance table is optional unless the bootstrap, execution contract, or stage risk requires one.

## Blockers

Stop only when progress genuinely depends on a user decision, including required approval, supplied-source substitution, material scope ambiguity, unavailable mandatory evidence/capability with no allowed alternative, or reopening accepted work without authority.

Failed tests, poor searches, dead URLs, tool failures, implementation defects, extraction problems, and verification failures are execution problems to repair, not user-decision blockers.

## Commit discipline

Follow the Knowledge Design execution contract for commit syntax, verification, model attribution and remote readback. Use one commit per completed stage. At S08, commit each selected pack's P1–P5 separately. At S15, commit P6–P7 separately. Do not batch independent stages.

Use `feature:`, `fix:`, `docs:` or `chore:` with an imperative summary and stage identifier. Inspect current repository guidance and history first. End AI-authored commits with exactly one verified model co-author trailer. Do not guess the execution identity.

A stage record cannot contain its own resulting commit hash. Resolve that commit from Git history; cite stable prior commits in dependent records. After a push failure, inspect both histories before retrying.

## Context

Reconstruct stage context from:

```text
governing bootstrap specification
+
accepted prior-stage repository outputs
+
current bootstrap execution contract under docs/research-logs/
```

Do not depend on conversation memory for accepted state.

## Domain checks

Verify quantities, bounds, uncertainty, causal claims and protected technical spans separately from clarity. Follow the fixture and held-out protocols in domain specification §7. Retain all generated outputs, including failures. Reader-task results remain NOT_RUN until actual readers perform the task.
