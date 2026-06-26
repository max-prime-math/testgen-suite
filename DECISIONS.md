# Decisions

## Workspace Structure

- Ingest work is grouped under `testgen-ingest`.
- Reusable ingest tool worktrees remain separate git repositories under `testgen-ingest/tools`.
- Source-family tracking lives under `testgen-ingest/sources`.
- `test-generator` remains a separate top-level repository and is not reorganized with ingest material.
- The root folder acts as a meta-workspace, not a monorepo.
- Cross-app coordination happens through shared docs and generated state files.
- The root meta-repo lives in `~/.codex/memories/testgen-suite-root-repo` and is operated through `workspace-git`.

## Import Strategy

- `test-generator` should accept pasted commented LaTeX.
- `test-generator` should accept pasted Typst.
- `test-generator` should accept best-effort JSON from OCR and BNK tools.
- Metadata comments should carry `class`, `unit`, and `section`.

## Data Ownership

- Original PDFs and BNK files remain the canonical inputs.
- Source-level Markdown catalogs record what has been catalogued and the review quality.
- Generated outputs may be kept for verification during development.
- Generated PDFs are disposable once the pipeline is trusted.
