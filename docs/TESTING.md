# SASA Testing & Validation

## Purpose

Tests are executable evidence of intended behaviour. Read the relevant tests before modifying the implementation.

## Change validation

Use the repository's existing Gradle tasks and GitHub Actions as the authoritative validation mechanism.

At minimum, identify the applicable:

- build task;
- unit/instrumentation tests;
- lint/static analysis;
- packaging/release checks;
- workflow checks.

Do not assume a task exists merely because another repository uses it.

## Test-first investigation

For a defect:

1. locate the existing test for the behaviour;
2. reproduce the failure;
3. determine whether the test is missing, incorrect, or exposing an implementation defect;
4. make the smallest repair;
5. run the narrow test;
6. run the repository-wide applicable validation.

## Evidence

Record the exact commit/branch and validation results when reporting a repair. A result from an older commit is not evidence for the current change.
