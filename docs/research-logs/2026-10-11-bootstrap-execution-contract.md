# Knowledge Design Skills — Bootstrap execution contract

**Project:** `knowledge-design-skills`  
**Governing specification:** [Domain bootstrap specification](2026-10-11-knowledge-design-skills-new-project-bootstrap-process.md)  
**Operator command:** `/bootstrap`  
**Initial state:** S00–S19 PLANNED; no accepted stage outputs.

This contract defines execution mechanics. The domain specification controls substantive requirements and exit gates. Explicit user instructions take precedence.

## Repository and branch

This archive has no Git history, configured remote or established branch. The intended repository name is `knowledge-design-skills`; the recommended working branch is `feat/bootstrap`.

At S00, verify the actual repository root, `origin` and current branch. Record those values in `s00-workspace.md`. The reference repository and its branch are provenance only. Never push Knowledge Design work to the software-engineering reference repository.

Use the recorded branch on later runs. Resolve a conflicting repository identity or branch before writing. Preserve unrelated local changes. Do not create, replace or force-update a remote implicitly.

## Execution authority

Invoking `/bootstrap` authorises the remaining stages unless the user narrows the scope. Commit and push verified stage work to the confirmed working branch. Initial archive preparation does not invoke `/bootstrap` or authorise publication elsewhere.

Release publication, a family registry update or changes in another repository require their own applicable authorisation. S18 must distinguish prepared publication evidence from actual publication.

## Supplied sources

Inventory `books/**/*.pdf` at each run. Record bibliographic metadata, edition, access, selection and reading coverage. Use repository-relative paths in durable records.

Never commit, move, rename, delete or modify supplied PDFs. Never upload them to an external service without explicit approval. Do not silently exclude, replace or demote a supplied book. New files do not automatically reopen an accepted corpus.

S02 selects exactly five distinct books. S03 requires meaningful direct examination of all five for their intended contributions. Relevant excerpts may be sufficient when their scope supports that contribution. A local PDF is preferred when supplied; another lawful direct source is valid. Summaries, publisher descriptions and model memory cannot replace reading.

## Stage loop

1. Read the complete stage and governing rules.
2. Inspect accepted dependencies and their evidence.
3. Extract required inputs, outputs, counts, checks and exit criteria.
4. Perform the substantive work and persist its records.
5. Re-read requirements and verify the actual outputs.
6. Repair mandatory failures and rerun affected checks.
7. Commit only that completed stage.
8. Push to the confirmed working branch and read back the remote commit and relevant files.
9. Continue with the next incomplete stage.

Use `bootstrap-stage-execution`, `bootstrap-research` and `direct-source-extraction` as needed. P1–P5 each have separate records and commits for every selected initial pack before S08 passes. P6–P7 each have separate records and commits at S15.

## Evidence and acceptance

Follow domain specification §§6–7 and §11. Preserve separate results for meaning, internal clarity, factual support and human comprehension. A result in one dimension cannot compensate for a failure in another.

The initial seven-fixture gate requires 21 retained outputs under the declared protocol. CL07 and human validation remain NOT_RUN until an actual reader study runs. Negative controls and the additional held-out source-error case are required at their specified stage. Do not present proposed tests or sample rewrites as executed results.

Preserve all failures and inconclusive results. Record actual model identifiers and reviewer types. No fabricated sources, user studies, measurements, tool runs or maturity claims are permitted.

Stage status is PLANNED, IN_PROGRESS, BLOCKED or COMPLETED. Completion requires substantive evidence and a resulting commit. Resolve a record's own commit through Git history; do not insert a self-referential commit hash. Downstream records may cite stable prior commit hashes.

## Commits

Before committing, inspect repository guidance and recent history. Run required verification. Use one commit per completed stage, including each pack substage.

Use `<type>: <imperative summary>` with `feature:`, `fix:`, `docs:` or `chore:`. Include the stage identifier. Examples:

```text
docs: Complete S02 five-book selection
docs: Complete S08 P3 technical-training extraction
feature: Implement S15 P6 technical-training showcase
```

Use short body paragraphs or bullets to explain the change and reason. Cite the owning specification section when relevant. End each AI-authored commit with exactly one `Co-Authored-By: <exact model name> <provider noreply address>` trailer. Verify the actual execution model and provider address. Never guess or copy a reference author's model. Do not add other generated trailers.

If verification or model identity cannot be established, retain the work and report the exact unresolved requirement. Do not claim a verified commit. A failed push is a delivery issue, not proof that the stage needs to be re-executed; inspect local and remote history before retrying.

## Repair and blockers

Repair failed searches, extraction problems, command failures and test failures using an allowed path. Do not weaken the acceptance gate.

Stop only for a decision or mandatory requirement that cannot be resolved within the authorised scope. Examples include inaccessible selected sources, required supplied-book permission, missing human participants for a required study, conflicting accepted decisions or unrelated changes that would have to be overwritten.

State the exact requirement, work completed and what is needed to continue. Routine implementation choices do not need confirmation.

## Final audit

After S19, audit the repository against the domain specification and current family requirements. Verify installation, generated outputs and any claimed comparisons from retained evidence. Keep unavailable downstream video or interface execution explicitly unverified. Report maturity only at the level the evidence supports.
