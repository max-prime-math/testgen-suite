# Pre-Calculus 40S Provincial Exams

This source covers Manitoba Pre-Calculus 40S provincial exams and marking-guide
content. The current pipeline lives in `../../tools/ocr-frq` because these exams
are free-response style and share most of the AP FRQ extraction architecture.

## Canonical Inputs

- Current Mathpix sample: `../../tools/ocr-frq/mathpix/pre-calc-40s_jan_13_mg-only_cleaned_aggressive.zip`
- Current processed JSON: `outputs/january-2013/processed.json`
- Current formatted review output: `outputs/january-2013/formatted.pdf`

## Tooling

- Manitoba entry point: `../../tools/ocr-frq/process_manitoba_exam.py`
- Parser: `../../tools/ocr-frq/src/manitoba_precalc_parser.py`
- Bulk-import converter: `../../tools/ocr-frq/src/extract_to_bulk_import.py`
- Existing docs: `../../tools/ocr-frq/MANITOBA_PROCESSING_README.md`

## Tracking Files

- `CATALOG.md` tracks which provincial exams have extracted/catalogued questions.
- `QUALITY.md` tracks Mathpix/OCR quality and review readiness.
- `outputs/` exposes generated JSON, LaTeX, and PDF artifacts for this source.
