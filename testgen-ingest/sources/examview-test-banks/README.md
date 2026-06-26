# ExamView Test Banks

This source covers binary ExamView BNK files and related recovered legacy bank
material. The decoder tool worktree lives in `../../tools/bnk-decoder`.

## Canonical Inputs

- BNK corpus: `../../tools/bnk-decoder/ignore/ExamView/Banks`
- Mathpix PDF exports: `../../tools/bnk-decoder/ignore/examples`
- Decoder reports: `outputs/reports`
- Legacy Math Power material: `legacy-math-power`

## Curriculum Index

`by-curriculum/` contains one directory per top-level curriculum family. These
folders are lightweight indexes for navigation and review tracking; the BNK
files remain in the decoder worktree so existing decoder scripts keep their
relative paths.

## Tooling

- Decoder app and packages: `../../tools/bnk-decoder`
- Corpus report command from the decoder worktree: `npm run report:corpus -- "ignore/ExamView/Banks"`
- Regression command from the decoder worktree: `npm run dialect:regression`
- Mathpix PDF export conversion from the decoder worktree: `npm run convert:mathpix-examview`
- Mathpix Typst compile audit from the decoder worktree: `npm run audit:mathpix-typst`

## Tracking Files

- `CATALOG.md` tracks file-level corpus coverage by curriculum.
- `QUALITY.md` tracks decoder and question-quality readiness.
- `outputs/` contains generated decoder reports, Mathpix PQP exports, Typst audit PDFs, and TestGen-safe exports.
