# Quality

## Current Assessment

The AP FRQ lane is the most complete OCR lane by coverage: 192 generated
questions across 32 year/form sections. It still has known content-quality gaps.

## Known Limitations

- 2000 BC Q2-Q6 have no solutions in the current scoring-guide extraction.
- 2000 BC Q1 has scoring-guide content that appears to belong to another question.
- Some part solutions are missing or truncated where OCR was incomplete.
- 1998 BC Q2 has an `e^{2z}` typo that should be reviewed as `e^{2x}`.
- Some rubric criterion lines may still appear in solution sections.

## Ready Criteria

- Every question has reviewed body text, solution text, rubric text, and figure references.
- Known year-specific issues are either fixed or explicitly marked blocked.
- Generated LaTeX compiles after edits.
- Export format for downstream `test-generator` import is selected and documented.
