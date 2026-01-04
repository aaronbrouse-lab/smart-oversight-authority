# Doctrine

This directory contains the **canonical doctrine blocks** for the Smart Oversight system.

## What “Doctrine” Means in Smart Oversight

In this system, **doctrine is not guidance, advice, or policy text**.

Doctrine defines the **structural rules** that govern:
- How authority is interpreted
- When continuation is allowed or denied
- What conditions invalidate an execution state
- How ambiguity, absence, or conflict is handled

Doctrine operates **before** automation, analysis, or optimization.
It establishes the non-negotiable boundaries within which all other system components must operate.

## What Doctrine Is Used For

Doctrine blocks are used by the system to:
- Enforce refusal or stand-down when required conditions are unmet
- Prevent silent normalization of deviation or ambiguity
- Ensure consistent interpretation across time, teams, and tools
- Support audit replay by making refusal logic explicit and reproducible

Doctrine is treated as an **authoritative input** to gate evaluation and replay generation.

## What Doctrine Is Not

Doctrine is **not**:
- Procedural instructions
- User training material
- Implementation code
- Configuration settings
- Human judgment or discretionary analysis

Those elements may reference doctrine, but they do not replace it.

## Change Discipline

All doctrine content in this directory:
- Is version-controlled
- Is subject to deliberate change control
- May only be modified through explicit commits
- Is assumed to have system-wide impact

Changes to doctrine are treated as changes to the system’s governing logic.

## Relationship to Other Directories

- `requirements/` define **what must be satisfied**
- `schemas/` define **how objects are structured**
- `doctrine/` defines **how satisfaction is evaluated and enforced**

Doctrine sits above execution and below authority sources.

---

This directory contains **definitions of how the system refuses**, not why a particular refusal occurred.
