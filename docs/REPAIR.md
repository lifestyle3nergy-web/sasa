# SASA Repair

## Repair objective

Restore the repository or application to a known-good state with the smallest justified change.

## Repair sequence

```
OBSERVE
  ↓
REPRODUCE
  ↓
CLASSIFY
  ↓
LOCATE OWNER
  ↓
READ IMPLEMENTATION
  ↓
READ TESTS
  ↓
PLAN
  ↓
REPAIR
  ↓
VALIDATE
  ↓
RESTORE / RELEASE
  ↓
RECORD
```

## Classify the failure

Determine whether the failure is primarily:

- build/toolchain;
- dependency;
- configuration/data;
- UI/application behaviour;
- provider/network integration;
- test/validation;
- packaging/release;
- repository automation.

## Repair rules

- Do not repair symptoms before identifying the owning boundary.
- Do not upgrade unrelated dependencies to solve an unproven problem.
- Preserve working behaviour outside the affected boundary.
- Prefer an existing repository mechanism over a new mechanism.
- Keep the repair isolated and reviewable.
- Add or update a test when behaviour changes.
- Update supporting documentation when the repair changes an established procedure or interface.

## Verification

A repair is not complete because the application builds once.

Verify the relevant build, test, static-analysis, packaging, and repository checks defined by the current project.

## Failed repair

If any required validation fails:

**STOP → preserve evidence → diagnose the failing gate → repair the branch → rerun validation.**

Do not treat a failed gate as acceptable noise.
