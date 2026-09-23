# SASA Operations

## Normal operation

SASA is an Android application. Operational behaviour is therefore observed through the application, build output, tests, logs, and repository automation already present in the project.

## Observe before changing

When behaviour is unexpected:

1. reproduce the behaviour;
2. capture the first meaningful error;
3. identify the component responsible;
4. inspect configuration and inputs;
5. inspect the corresponding implementation;
6. inspect the relevant test;
7. only then plan a change.

## Operational surfaces

Use the repository's existing mechanisms for:

- building;
- testing;
- lint/static analysis;
- packaging;
- release;
- provider/configuration updates;
- tracker/ad-blocking data updates.

The exact commands are maintained in the repository's build scripts and workflow definitions. Do not create undocumented command aliases.

## Healthy state

A healthy change is one where the intended behaviour works and the repository's existing validation gates remain green.
