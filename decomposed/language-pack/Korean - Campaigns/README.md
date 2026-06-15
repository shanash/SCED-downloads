# Korean - Campaigns (decomposed)

**Source of truth.** Do not edit combined JSON (`downloadable/korean_campaigns.json`)
directly. Edit the decomposed per-card files here instead, then regenerate the
combined artifact via `SCED-tools/scripts/build-korean-campaigns-combined.py`.

## Why decomposed is authoritative

- `library.json` has `decomposed: true` for Korean - Campaigns, so the combined
  JSON is composed from the decomposed source in this directory at build time.
  The combined JSON is a generated build artifact, not a tracked source file.
- Maintainers MUST make Korean - Campaigns changes in the decomposed files here
  and rebuild the combined JSON in the same PR. A change applied only to a
  generated combined JSON is overwritten on the next build, so PRs that modify
  the combined JSON without a corresponding decomposed change are rejected in
  review.

## Build flow

```
decomposed/language-pack/Korean - Campaigns/Korean-Campaigns.KoreanC/**
    ↓  (SCED-tools/scripts/build-korean-campaigns-combined.py)
downloadable/korean_campaigns.json   (build artifact; do not hand-edit)
```
