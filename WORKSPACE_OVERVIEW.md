# Workspace Overview

This folder is a meta-workspace that contains four separate git repositories:

- `bnk-decoder`: ExamView BNK decoder and exporter.
- `ocr-frq`: AP Calculus BC free-response OCR and LaTeX/PDF pipeline.
- `ocr-mcq`: AP Calculus BC multiple-choice OCR and LaTeX pipeline.
- `test-generator`: Browser-based question bank and test builder.

## Current Source Of Truth

- Original PDFs are the source of truth for the OCR apps.
- BNK files are the source of truth for `bnk-decoder`.
- Generated LaTeX, Typst, JSON, and PDFs are intermediate or downstream artifacts.
- `test-generator` is the normalization and assembly layer for human use.

## Intended Flow

- `ocr-frq` and `ocr-mcq` ingest PDFs and produce usable question data.
- `bnk-decoder` ingests BNK files and exports a portable question representation.
- `test-generator` accepts manual paste-in content plus best-effort JSON imports from the other tools.
- Test PDFs and generated exports are verification artifacts, not canonical data.

## Operating Rules

- Keep app-level repos independent.
- Keep workspace-wide docs at the root.
- Use `workspace-git` for the root meta-repo because the environment's root `.git` directory is read-only.
- Update the workspace state after meaningful commits or repo changes.
- Prefer a small set of canonical commands over one-off shell invocations.

## Active Focus

- Stabilize `ocr-frq` first.
- Improve OCR and BNK decoding quality, especially graphs and figures.
- Build a best-effort import layer in `test-generator`.
