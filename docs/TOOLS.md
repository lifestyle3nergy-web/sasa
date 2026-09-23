# SASA Engineering Tools

## Tool discovery

Before adding a tool, locate the existing repository mechanism that performs the required operation.

Useful tool categories include:

| Category | Purpose |
|---|---|
| Build | compile/package the Android application |
| Test | execute automated behaviour checks |
| Lint | detect static/code-quality problems |
| Diagnose | isolate failures |
| Inspect | examine configuration, data, and runtime state |
| Release | package and publish validated versions |
| CI | independently reproduce repository gates |

## Source of truth

The exact executable commands live in the current repository's Gradle files, scripts, and GitHub Actions workflows.

This document intentionally avoids inventing command names that may not exist in the current SASA tree.

## Adding a tool

A new tool should have:

- a clear owner;
- defined inputs and outputs;
- failure behaviour;
- tests;
- a documented purpose;
- a clear reason the existing toolchain cannot already perform the task.
