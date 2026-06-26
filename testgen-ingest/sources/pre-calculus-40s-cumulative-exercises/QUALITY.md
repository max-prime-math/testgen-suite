# Quality

## Current Assessment

This source is structurally catalogued and usable as a file-backed bank. It
still needs semantic review tracking at question level.

## Strengths

- 1000 question JSON records are indexed.
- Image assets are present and counted in the manifest.
- Shared narratives are modeled separately instead of duplicated.
- Curriculum metadata is stored with the bank.

## Known Risks

- Catalogued does not mean every question has been human-audited.
- Some image-heavy questions need display checks in the downstream app.
- Split questions and shared narratives need spot checks to ensure they read correctly in isolation.

## Ready Criteria

- Add per-question review status: `unreviewed`, `usable`, `needs-fix`, or `blocked`.
- Verify image references resolve from every question that declares images.
- Spot-check each unit/section for curriculum alignment and rendering quality.
