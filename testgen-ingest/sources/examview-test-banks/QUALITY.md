# Quality

## Current Assessment

The ExamView corpus is catalogued at the file/family level. Question-level
quality depends on decoder maturity and varies by bank family.

## Current Strengths

- The BNK corpus is organized by curriculum family.
- `bnk-decoder` has corpus reports, dialect regression reports, and TestGen-ready export paths.
- Pre-Calculus 11/12 work has active diagnostics for narratives, graphs, algorithms, and assets.
- The Mathpix PDF-export path now generates Typst PQP for Pre-Calculus 12 with real copied image assets and compile-audited review PDFs.

## Known Risks

- Some decoder paths are still alpha-quality for semantic parity.
- Graph objects may be preserved as data before they render natively downstream.
- OLE/MathType and WMF-style embedded objects still need deeper decoding or documented fallback handling.
- Answer-key recovery and record boundary handling need bank-family validation.
- Internal "clean" scores are not enough; PDF/source comparison remains the readiness gate.
- Graph-heavy multiple-choice questions in Chapters 01-03 still have incomplete choice parsing diagnostics.
- Mathpix and BNK-derived chapter counts do not yet agree; some matching groups are intentionally grouped and some OCR sections need manual audit.
- A small number of solution formulas fall back to Typst-safe text strings where Mathpix mixed prose labels into complex math/table notation; raw LaTeX is preserved for manual repair.

## Mathpix PQP Snapshot

Generated 2026-06-26 from `../../tools/bnk-decoder/ignore/examples` into
`outputs/reports/mathpix-pqp/precalculus-12`.

- Questions: 696
- Referenced image assets: 400
- Content format: Typst
- Curriculum metadata/tags: full Manitoba Pre-Calculus 40S outcome labels on all questions
- Source metadata/tags: ExamView, Mathpix, McGraw Hill, Pre-Calculus 40S, with canonical lowercase source tags in PQP
- Typst audit: 11/11 chapter review PDFs compile
- Quality flags: 683 clean, 13 suspect, 0 garbage
- Structural validation issues: 10 graph-choice MCQs with incomplete A-D choice recovery
- Symlinks: none

## Ready Criteria

- Each BNK file has question count, decoder dialect, and export status.
- Each exported bank has diagnostics reviewed and classified.
- Graphs, images, algorithms, and answer keys have source-parity evidence.
- A bank is marked import-ready only after a representative render or PDF audit.
