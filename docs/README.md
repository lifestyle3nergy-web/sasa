# SASA Engineering Documentation

This directory is the engineering support layer for SASA (AI Hub).

The repository source, tests, configuration, and existing build tooling remain authoritative. These documents explain how to understand, operate, diagnose, repair, validate, and extend the existing system without replacing its established conventions.

## Start here

1. [Architecture](ARCHITECTURE.md) — identify system boundaries and ownership.
2. [Installation](INSTALL.md) — establish a clean working environment.
3. [Operations](OPERATIONS.md) — run and inspect the existing application.
4. [Repair](REPAIR.md) — diagnose, repair, restore, and verify.
5. [Testing](TESTING.md) — prove a change is safe.
6. [Staging](STAGING.md) — move a validated change through controlled stages.
7. [Tools](TOOLS.md) — find the repository's existing engineering tools.
8. [Reference](REFERENCE.md) — commands, parameters, files, and interfaces.

## Engineering rule

Do not invent a new mechanism when an existing SASA mechanism already works. Read the implementation and tests first, then use the smallest change that preserves established behaviour.

## Change path

**Observe → Understand → Plan → Implement → Validate → Review → Measure → Record**

If a document conflicts with the current implementation, stop and reconcile the documentation with the repository before relying on it.
