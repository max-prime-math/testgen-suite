# Catalog

Last counted from `../../tools/bnk-decoder/ignore/ExamView/Banks`: 2026-06-25.

| Curriculum | BNK files | Index folder | Source folder |
| --- | ---: | --- | --- |
| Calculus | 1 | `by-curriculum/calculus` | `../../tools/bnk-decoder/ignore/ExamView/Banks/Calculus` |
| Foundations of Math 10 | 72 | `by-curriculum/foundations-of-math-10` | `../../tools/bnk-decoder/ignore/ExamView/Banks/Foundations of Math 10` |
| Foundations of Math 11 | 9 | `by-curriculum/foundations-of-math-11` | `../../tools/bnk-decoder/ignore/ExamView/Banks/Foundations of Math 11` |
| Foundations of Math 12 | 8 | `by-curriculum/foundations-of-math-12` | `../../tools/bnk-decoder/ignore/ExamView/Banks/Foundations of Math 12` |
| Math Apprenticeship 10 | 10 | `by-curriculum/math-apprenticeship-10` | `../../tools/bnk-decoder/ignore/ExamView/Banks/Math Apprenticeship 10` |
| Math Apprenticeship 11 | 10 | `by-curriculum/math-apprenticeship-11` | `../../tools/bnk-decoder/ignore/ExamView/Banks/Math Apprenticeship 11` |
| Math Makes Sense 9 | 67 | `by-curriculum/math-makes-sense-9` | `../../tools/bnk-decoder/ignore/ExamView/Banks/Math Makes Sense 9` |
| MathWorks 10 | 37 | `by-curriculum/mathworks-10` | `../../tools/bnk-decoder/ignore/ExamView/Banks/MathWorks 10` |
| MathWorks 11 | 30 | `by-curriculum/mathworks-11` | `../../tools/bnk-decoder/ignore/ExamView/Banks/MathWorks 11` |
| MathWorks 12 | 29 | `by-curriculum/mathworks-12` | `../../tools/bnk-decoder/ignore/ExamView/Banks/MathWorks 12` |
| Pre-Calculus 11 | 9 | `by-curriculum/pre-calculus-11` | `../../tools/bnk-decoder/ignore/ExamView/Banks/Pre-Calculus 11` |
| Pre-Calculus 11 (Mickelson) | 45 | `by-curriculum/pre-calculus-11-mickelson` | `../../tools/bnk-decoder/ignore/ExamView/Banks/Pre-Calculus 11 (Mickelson)` |
| Pre-Calculus 12 | 11 | `by-curriculum/pre-calculus-12` | `../../tools/bnk-decoder/ignore/ExamView/Banks/Pre-Calculus 12` |
| Pre-Calculus 12 (Mickelson) | 35 | `by-curriculum/pre-calculus-12-mickelson` | `../../tools/bnk-decoder/ignore/ExamView/Banks/Pre-Calculus 12 (Mickelson)` |

## Totals

- Top-level curriculum families: 14
- BNK files: 373
- Question-level catalog: partial, currently represented by decoder reports and exported packages rather than a consolidated source-level index.

## Mathpix PDF Export Conversion

Last generated from `../../tools/bnk-decoder/ignore/examples`: 2026-06-26.

| Source set | Input zips | PQP questions | Referenced assets | Output folder | Status |
| --- | ---: | ---: | ---: | --- | --- |
| Pre-Calculus 12 Chapters 01-11 | 11 | 696 | 400 | `outputs/reports/mathpix-pqp/precalculus-12` | Typst PQP generated; all 11 audit PDFs compile; graph-choice diagnostics remain |

The output folder includes one `.pqp.json` and one `.summary.json` per chapter,
plus `conversion-summary.json`, copied image assets, raw Mathpix LaTeX, and
`typst-audit/` review PDFs. PQP content is emitted as Typst while raw LaTeX is
preserved under `extensions.mathpix`.

## Backlog

- Promote decoder corpus reports into a stable source-level file index.
- Add per-bank question counts and per-bank quality status.
- Separate generated diagnostics from manually reviewed import readiness.
- Reconcile the Mathpix PQP chapter counts against the PDF exports and existing BNK-derived PQP.
