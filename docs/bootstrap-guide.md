# Bootstrap guide

## 1. Set up the repository once

Create an empty GitHub repository for `knowledge-design-skills` and clone it. Copy this archive's contents into the clone, including `.claude/` and `.gitignore`. The archive contains no Git history.

Use a dedicated working branch. The recommended name is `feat/bootstrap`. If your clone already has history, create that branch from your intended base. Preserve unrelated changes.

Before `/bootstrap`, check that `origin` points to your intended knowledge-design repository and that the working branch is the one you want to update. The command commits and pushes completed stages there.

The extraction itself does not complete S00. The first run verifies the durable repository, records its location and branch, and completes S00 against the specification.

## 2. Add supplied books, if available

Put book PDFs under `books/`. Subdirectories are supported.

`/bootstrap` discovers `books/**/*.pdf` automatically. The directory is gitignored. Supplied books stay local and are not uploaded to external services without your explicit approval.

Books are not required to start S00. The selected five-book corpus must be directly accessible for the S03 extraction gate. Relevant excerpts can qualify when they cover the intended contribution. Selection and source-access decisions are recorded separately.

## 3. Start or resume

Open Claude Code from the repository root:

```bash
claude
```

Then run:

```text
/bootstrap
```

It reconstructs progress from repository evidence, executes each remaining stage, checks its outputs, repairs failures, commits and pushes it, verifies the remote state, then continues.

No stage numbers or book paths are required. To limit execution, state the required stage or range with your request.

The workflow stops for a required decision or an unresolved mandatory blocker. It does not treat generated text or internal review as evidence of human understanding. A reader study needs actual participants.

## Optional retrieval fallback

Native web search, web fetching and local reading are the defaults. Firecrawl is optional. If a concrete retrieval problem requires it, use its current official installation and authentication instructions. Keep large retrieval outputs under `.firecrawl/`.

The workflow reports missing tools or source access precisely. It never reports an unexecuted benchmark, installation or reader study as passed.
