# TestGen Ingest

This folder groups the ingestion sources and tooling that feed `test-generator`.
`test-generator` itself intentionally remains outside this folder.

## Layout

- `sources/pre-calculus-40s-provincial-exams`: Manitoba Pre-Calculus 40S provincial exam OCR and import tracking.
- `sources/pre-calculus-40s-cumulative-exercises`: Catalogued Pre-Calculus 40S cumulative exercise bank.
- `sources/examview-test-banks`: ExamView BNK source corpus, curriculum indexes, and legacy Math Power material.
- `sources/ap-exam-mcqs`: AP multiple-choice PDF/OCR tracking.
- `sources/ap-exam-frqs`: AP free-response PDF/OCR tracking.
- `tools/bnk-decoder`: ExamView decoder worktree.
- `tools/ocr-frq`: AP FRQ and Manitoba Pre-Calculus 40S OCR/LaTeX worktree.
- `tools/ocr-mcq`: AP MCQ OCR/LaTeX worktree.

## Source Tracking

Each source directory has the same documentation pattern:

- `README.md`: what the source is and where canonical inputs/tooling live.
- `CATALOG.md`: what has been catalogued so far.
- `QUALITY.md`: known review state, readiness, and quality gaps.
- `outputs/`: source-local generated artifacts, reports, and importable packages.

Keep canonical source files in their source or tool location. Keep generated
exports under the owning source's `outputs/` directory when they are useful for
verification or hand review.

## Import Boundary

The ingest side prepares source-specific outputs and quality evidence.
`test-generator` remains the downstream app that normalizes, stores, assembles,
and renders questions for human use.
