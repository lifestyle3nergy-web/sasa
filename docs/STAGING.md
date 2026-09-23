# SASA Staging

## Staging model

SASA changes progress through controlled evidence gates:

```
CHANGE
  ↓
LOCAL DEVELOPMENT
  ↓
TARGETED VALIDATION
  ↓
FULL VALIDATION
  ↓
PULL REQUEST
  ↓
INDEPENDENT CI
  ↓
HUMAN REVIEW
  ↓
PROMOTION
  ↓
POST-CHANGE OBSERVATION
```

## Gate rule

A failed required gate stops progression.

Do not bypass a failed check merely to reach the next stage.

## Branch discipline

Work on an isolated branch. Keep unrelated repairs separate so reviewers can identify exactly what changed and why.

## Promotion evidence

A promotion decision should be based on current-head evidence:

- exact commit;
- relevant tests;
- applicable CI;
- review;
- release/package evidence where applicable.

## Learning

When a recurring failure reveals a missing tool, test, guardrail, or explanation, improve the repository so the next engineer can detect it earlier.
