# SASA Reference

## Repository references

| Concern | Authoritative location |
|---|---|
| Application behaviour | current source tree |
| Build | Gradle configuration and wrapper |
| Tests | current test tree |
| CI | `.github/workflows/` |
| Dependencies | Gradle dependency declarations and lock/configuration files where present |
| Release | current release/build configuration |
| Legal | LICENSE and repository legal notices |

## Parameters

For any configurable behaviour, document:

- parameter name;
- type/format;
- default;
- allowed values;
- owner;
- validation;
- effect;
- failure behaviour.

## Interfaces

For each externally visible interface, identify:

- caller;
- input;
- validation;
- implementation;
- output;
- errors;
- authentication/privacy implications;
- test coverage.

## Updating this reference

Reference material must describe the current repository. Remove stale instructions rather than accumulating historical procedures that no longer work.
