# Ingest Architecture

## Layers

1. Source material: PDFs, Mathpix exports, BNK files, recovered legacy bank files, or already-normalized question JSON.
2. Extractor tool: OCR, parser, decoder, or converter that understands one source family.
3. Review artifacts: generated LaTeX, PDFs, JSON packages, image folders, diagnostics, and audit reports.
4. Source catalog: Markdown state files in `sources/*` that say what is catalogued and how trustworthy it is.
5. Downstream import: best-effort JSON, package exports, or manual paste/import into `test-generator`.

## Source Families

- Pre-Calculus 40S provincial exams use the shared `ocr-frq` pipeline because the source shape is exam-style free response with marking-guide solutions.
- Pre-Calculus 40S cumulative exercises are already catalogued as a file-backed question bank.
- ExamView test banks use `bnk-decoder` because the canonical input is binary BNK files and the hard part is structural recovery.
- AP Exam MCQs use `ocr-mcq` because the source is page-image multiple choice with marked answers.
- AP Exam FRQs use `ocr-frq` because the source pairs exam booklets with scoring guides.

## Quality Gates

Use source-specific gates before treating output as import-ready:

- OCR lanes need image presence, math rendering, answer/solution review, and compile checks.
- ExamView lanes need decoder diagnostics, PDF or source-render comparison, graph/image review, and answer-key validation.
- Already-normalized banks need schema validity, image reference checks, curriculum alignment, and semantic spot checks.

The `CATALOG.md` files track coverage. The `QUALITY.md` files track whether that coverage is good enough to trust.
