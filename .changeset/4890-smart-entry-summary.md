---
type: Fixed
pr: 4890
---
**`smart-entry` summaries no longer mix the project-global phase index with the milestone-scoped phase count** — in a multi-milestone project the `planning` summary and the shared `executing` / `verify-pending` progress line render the milestone-relative position (e.g. `Phase 3 of 5 (v1.3)` instead of `Phase 13 of 5`). Single-milestone rendering is unchanged. (#4890)
