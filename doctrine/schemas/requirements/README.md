# Requirements

This directory contains the **canonical requirement and control node definitions** used by the Smart Oversight system.

## What “Requirement” Means in Smart Oversight

In this system, a **requirement** is a versioned, uniquely identified node that expresses:
- A condition that must be satisfied, evidenced, or explicitly unresolved
- The authority source it derives from (or is mapped to)
- The evidence expectation (what would demonstrate satisfaction)
- The frequency, scope, and applicability boundaries
- The authority level (e.g., authoritative vs local/derived)

Requirements are represented as **nodes** so they can be referenced, evaluated, compared over time, and replayed.

## What Requirements Are Used For

Requirements are used to:
- Define the system’s evaluable surface (“what must be true”)
- Provide stable targets for drift detection (what changed, when, and why)
- Enable consistent gate evaluation and refusal decisions
- Support audit replay by linking outcomes to explicit requirement nodes
- Prevent ambiguous interpretations from substituting for explicit conditions

A gate decision should be explainable as:  
**Which requirement nodes were satisfied, unresolved, missing, or conflicting — and why.**

## What Requirements Are Not

Requirements are **not**:
- Implementation tasks or engineering backlog items
- User procedures or checklists (those may reference requirements)
- Gate rules or refusal logic (that belongs in `doctrine/`)
- Data structure definitions (that belongs in `schemas/`)
- Unversioned notes or “tribal knowledge”

Requirements define “what,” not “how.”

## Node Identity and Traceability

Each requirement/control node should have:
- A stable, unique identifier
- A title and concise statement
- Authority/source references (as applicable)
- Applicability boundaries (scope, domain, conditions)
- Evidence expectations (what counts as support)
- Status and version metadata

Nodes must remain referenceable across time, even when updated (via versioning and supersession).

## Change Discipline

All requirement nodes in this directory:
- Are version-controlled and treated as authoritative inputs
- Must be updated through deliberate, reviewable commits
- Should be superseded rather than silently rewritten when meaning changes
- Must preserve traceability to prior versions and sources

Changes to requirements change what the system can evaluate.

## Relationship to Other Directories

- `schemas/` define **how requirement nodes are structured**
- `doctrine/` defines **how nodes are evaluated and how refusal operates**
- `requirements/` define **the conditions and controls to be evaluated**

Requirements are the system’s “what must be satisfied” layer.
