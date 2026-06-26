# Quality

## Current Assessment

The AP MCQ source has a generated combined output, but it should be treated as
OCR-derived draft material until answer choices and marked answers are reviewed.

## Known Risks

- OCR depends on image quality and model behavior.
- Correct-answer detection depends on visible answer marking in the source pages.
- Generated LaTeX can compile while still containing semantic OCR mistakes.
- The current `ocr-mcq` worktree has existing uncommitted local/generated files; they were preserved during the move.

## Ready Criteria

- Every question has body text, five choices when applicable, and one verified answer.
- Flagged pages have been manually corrected.
- Generated LaTeX compiles after corrections.
- A source/year/form identifier is attached before downstream import.
