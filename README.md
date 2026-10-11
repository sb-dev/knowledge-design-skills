# Knowledge Design Skills

Skills for explaining topics clearly, from a short answer to a complex technical account. Adapt explanations to the audience, purpose and medium while preserving their meaning.

**Status:** Bootstrap workspace. Research, production skills and evaluation are planned.

The selected design is a toolkit for producing, adapting and reviewing explanations. It supports text, video content and interface content. Audience, depth, length, tone and examples are adjustable. Meaning preservation, clarity, factual support and human comprehension are assessed separately.

## Start

Follow the [bootstrap guide](docs/bootstrap-guide.md). In Claude Code, run:

```text
/bootstrap
```

The command reads repository progress, finds local books and executes the next incomplete stage. Run the same command to resume.

## Repository contents

- [Domain bootstrap specification](docs/research-logs/2026-10-11-knowledge-design-skills-new-project-bootstrap-process.md): research, domain rules, corrected examples and acceptance gates.
- [Execution contract](docs/research-logs/2026-10-11-bootstrap-execution-contract.md): stage execution, verification and commits.
- [Research tooling](docs/research-logs/2026-10-11-bootstrap-research-tooling.md): source access and research methods.
- [Research logs](docs/research-logs/README.md): durable decisions and evidence.
- [Source provenance](docs/bootstrap-provenance.md): reference revision, adaptations and notices.

The four skills under `.claude/skills/` conduct the bootstrap. The candidate production skills `explain-topic`, `adapt-explanation` and `review-explanation` remain subject to research. Production packages, examples, Extension Packs, benchmarks and CI are created at their specified stages.
