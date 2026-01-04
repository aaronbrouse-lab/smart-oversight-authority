# Schemas

This directory contains the **canonical object schemas** used by the Smart Oversight system.

## What “Schema” Means in Smart Oversight

In this system, a **schema** is a strict, versioned contract that defines:
- What an object is allowed to contain
- What fields are required vs optional
- Valid types, formats, and constraints
- How objects reference other objects (identifiers, hashes, versions)

Schemas exist to prevent ambiguity, silent drift, and “it kind of works” data shapes.

## What Schemas Are Used For

Schemas are used to:
- Validate ingested inputs and produced artifacts
- Enforce consistency across modules and tools
- Enable deterministic audit replay and comparison
- Prevent accidental introduction of new fields or meanings without review
- Support interoperability (future tools can read the same objects)

A schema is how the system ensures that “an object” remains the same thing over time.

## What Schemas Are Not

Schemas are **not**:
- Business logic or gate rules (that belongs in `doctrine/`)
- Requirements or control intent (that belongs in `requirements/`)
- UI configuration
- Storage layout rules
- Free-form documentation

Schemas describe structure and constraints, not meaning or judgment.

## Change Discipline

All schemas in this directory:
- Are version-controlled and treated as authoritative inputs
- Must remain backward-compatible unless explicitly version-bumped
- Should change only when a new object type is introduced or a formal contract must evolve
- Require explicit commit messages that state what changed and why

Schema changes are system-wide interface changes.

## Relationship to Other Directories

- `requirements/` define **what must be represented**
- `doctrine/` defines **how evaluation and refusal operate**
- `schemas/` define **how artifacts are structured so they can be validated and replayed**

Schemas make the system inspectable and reproducible.
