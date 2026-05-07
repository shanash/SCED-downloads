# Korean - Campaigns (decomposed)

**Source of truth.** Do not edit combined JSON (`downloadable/korean_campaigns.json`)
directly. Edit the decomposed per-card files here instead, then regenerate the
combined artifact via `SCED-tools/scripts/build-korean-campaigns-combined.py`.

See task `.am/korean-image-apply/design.md` §3.3 for the invariant and rationale.

## Why decomposed is authoritative

- `library.json` currently has `decomposed: false` for Korean - Campaigns as a
  temporary state (see SCED-downloads commit `0c2e08bdab`). Once
  UniqueBack/Deck 2320 parity is verified, a follow-up task
  (`korean-campaigns-decomposed-restore`) will restore `decomposed: true` and
  remove the tracked combined JSON.
- Until then, maintainers MUST update decomposed files and rebuild the
  combined JSON in the same PR. PRs that modify the combined JSON without a
  corresponding decomposed change will be rejected in review.

## Build flow

```
decomposed/language-pack/Korean - Campaigns/Korean-Campaigns.KoreanC/**
    ↓  (SCED-tools/scripts/build-korean-campaigns-combined.py)
downloadable/korean_campaigns.json   (build artifact; do not hand-edit)
```
