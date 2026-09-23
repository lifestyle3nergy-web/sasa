# SASA Installation

## Goal

Establish a clean, reproducible development environment using the repository's existing Android/Gradle build configuration.

## Principle

Use the versions and configuration already declared by the repository. Do not introduce a second build system or substitute package-management conventions without an explicit engineering reason.

## Procedure

1. Clone the repository.
2. Open the project in Android Studio or use the repository's Gradle wrapper from a terminal.
3. Inspect the declared Android/Gradle/Kotlin configuration before changing versions.
4. Allow the existing wrapper to resolve the declared dependencies.
5. Build the existing application target.
6. Run the existing test suites.
7. Confirm the resulting state before beginning development.

## Clean-environment check

A successful installation must demonstrate:

- dependencies resolve;
- the project configures;
- the application builds;
- the existing tests execute;
- no unrelated repository files are modified.

## If installation fails

Do not immediately upgrade dependencies.

Record:

- command executed;
- Gradle/JDK/Android tool versions;
- first meaningful error;
- affected module;
- dependency or configuration involved.

Then follow [Repair](REPAIR.md).
