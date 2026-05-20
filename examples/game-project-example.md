# Synthetic Game Project Example

This is a synthetic example. Replace names and paths with your own project context.

## Task

```text
T014: Fix mobile HUD overlap
```

## Board Entry

- [ ] T014: Fix mobile HUD overlap
  - Goal: Health, score, and pause controls fit on a small mobile viewport.
  - Done when: HUD elements do not overlap at 375x667 and 430x932.
  - Verification: browser screenshot or playtest report for both viewports.
  - Risk: UI fix could hide controls or reduce touch target size.
  - Recommended intelligence: medium

## Handoff Entry

```text
completed:
- adjusted HUD spacing and responsive layout

verification:
- 375x667 screenshot: pass
- 430x932 screenshot: pass

not tested:
- tablet landscape

next:
- check long localized labels
```

