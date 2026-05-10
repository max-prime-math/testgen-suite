# Decisions

## Workspace Structure

- The four apps remain separate git repositories.
- The root folder acts as a meta-workspace, not a monorepo.
- Cross-app coordination happens through shared docs and generated state files.

## Import Strategy

- `test-generator` should accept pasted commented LaTeX.
- `test-generator` should accept pasted Typst.
- `test-generator` should accept best-effort JSON from OCR and BNK tools.
- Metadata comments should carry `class`, `unit`, and `section`.

## Data Ownership

- Original PDFs and BNK files remain the canonical inputs.
- Generated outputs may be kept for verification during development.
- Generated PDFs are disposable once the pipeline is trusted.

