# Workspace Overview

This folder is a meta-workspace for TestGen ingestion work and the downstream
`test-generator` app.

- `testgen-ingest`: source-oriented ingest workspace, catalogs, quality notes,
  and ingest tools.
- `test-generator`: Browser-based question bank and test builder.

The ingest tool worktrees remain separate git repositories:

- `testgen-ingest/tools/bnk-decoder`: ExamView BNK decoder and exporter.
- `testgen-ingest/tools/ocr-frq`: AP FRQ and Manitoba Pre-Calculus 40S OCR/LaTeX pipeline.
- `testgen-ingest/tools/ocr-mcq`: AP multiple-choice OCR and LaTeX pipeline.

## Current Source Of Truth

- Original PDFs and Mathpix exports are the source of truth for OCR lanes.
- BNK files are the source of truth for ExamView banks.
- `testgen-ingest/sources/*/CATALOG.md` tracks what has been catalogued.
- `testgen-ingest/sources/*/QUALITY.md` tracks known readiness and review gaps.
- Generated LaTeX, Typst, JSON, and PDFs are intermediate or downstream artifacts.
- `test-generator` is the normalization and assembly layer for human use.

## Intended Flow

- `testgen-ingest/sources/*` names the source family and keeps catalog/quality state.
- `testgen-ingest/tools/ocr-frq` and `testgen-ingest/tools/ocr-mcq` ingest PDFs and Mathpix exports.
- `testgen-ingest/tools/bnk-decoder` ingests BNK files and exports a portable question representation, including binary-backed narratives, multi-part questions, assets, and diagnostics.
- `test-generator` accepts manual paste-in content plus best-effort JSON imports from the other tools.
- Test PDFs and generated exports are verification artifacts, not canonical data.

## Operating Rules

- Keep app-level repos independent.
- Keep workspace-wide docs at the root.
- Keep source-family ingest docs in `testgen-ingest/sources`.
- Keep reusable ingest tool worktrees in `testgen-ingest/tools`.
- Keep `test-generator` outside `testgen-ingest` and do not reorganize it as part of ingest cleanup.
- Use `workspace-git` for the root meta-repo because the environment's root `.git` directory is read-only.
- Update the workspace state after meaningful commits or repo changes.
- Prefer a small set of canonical commands over one-off shell invocations.
- When you're ready, add a GitHub remote to the root meta-repo and push `main` like any other repo.
- For any new session, start with `NEW_SESSION.md` and the four root docs listed there.

## Active Focus

- Stabilize `testgen-ingest/tools/ocr-frq` first.
- Improve OCR and BNK decoding quality, especially graphs and figures.
- Preserve shared narratives and question structure in `testgen-ingest/tools/bnk-decoder` so decoded questions still read like the original ExamView prompts.
- Fingerprint all BNK families and split the decoder into safe dialects before broadening heuristics globally.
- Build a best-effort import layer in `test-generator`.
