# AP Exam MCQs

This source covers AP exam multiple-choice pages. The OCR pipeline lives in
`../../tools/ocr-mcq`.

## Canonical Inputs

- Current source PDF: `../../tools/ocr-mcq/PDFs/ap_multiple_choice.pdf`
- Current combined LaTeX output: `outputs/latex/output_exam.tex`
- Current review PDF: `outputs/latex/output_exam.pdf`

## Tooling

- CLI entry point: `../../tools/ocr-mcq/src/main.py`
- OCR implementation: `../../tools/ocr-mcq/src/ocr.py`
- Answer detection: `../../tools/ocr-mcq/src/detection.py`
- Web app: `../../tools/ocr-mcq/app.py`

## Tracking Files

- `CATALOG.md` tracks processed pages/questions.
- `QUALITY.md` tracks OCR confidence, answer detection, and review status.
- `outputs/` exposes generated LaTeX/PDF artifacts.
