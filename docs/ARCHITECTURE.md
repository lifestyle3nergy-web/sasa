# SASA Architecture

## Purpose

SASA (AI Hub) is an Android application that brings AI assistant services together in a configurable interface.

The current repository is the source of truth for the implementation. This document describes how an engineer should discover the architecture rather than imposing a new architecture on the project.

## How to read the repository

Start at the repository root and follow the existing source structure:

- application entry points — identify lifecycle and startup behaviour;
- UI/presentation code — identify user-facing behaviour;
- configuration/data — identify service definitions and runtime configuration;
- networking/provider integration — identify external service boundaries;
- tests — identify behaviour that the project already considers important;
- build/release configuration — identify packaging and delivery behaviour.

Use the actual directory and symbol names in the current tree when making changes. Do not create parallel structures merely to match this document.

## Boundary rule

A change belongs at the narrowest existing boundary that owns the behaviour.

Before changing code, answer:

1. What behaviour is changing?
2. Which existing component owns it?
3. What inputs and outputs does it have?
4. Which tests prove the current behaviour?
5. What external dependency or configuration does it rely on?
6. What is the smallest safe change?

## External services

AI services, tracker/ad-blocking data, translation services, distribution channels, and other external systems are integration boundaries. Treat their schemas, URLs, permissions, availability, and failure modes as explicit dependencies.

## Architecture evidence

When implementation changes materially, update this document only when the documented architectural relationship has changed. Do not document every implementation detail here; keep those details close to the source and tests.
