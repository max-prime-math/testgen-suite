# Outputs

This directory contains generated ExamView decoder outputs.

Current outputs:

- `reports/`: full `bnk-decoder` reports tree.
- `reports/corpus-dialects/`: corpus fingerprint and dialect inventory reports.
- `reports/dialect-regression/`: representative decoder regression reports.
- `reports/mathpix-pqp/precalculus-12/`: Typst PQP files generated from Mathpix PDF exports, with copied assets, raw LaTeX, and Typst audit output.
- `reports/testgen-safe/`: TestGen-safe export and render-check outputs.

The ExamView decoder scripts now write into `reports/` by default.
The Mathpix converter writes into `reports/mathpix-pqp/` by default. The Typst audit writes into `reports/mathpix-pqp/precalculus-12/typst-audit/`.
