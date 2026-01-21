# OPM in One Page
## The Open Publication Model at a Glance

**Status:** Non-Normative  
**Authority:** None  
**Purpose:** Ultra-concise architectural summary  
**Audience:** Architects, implementers, decision-makers  
**Author:** Heath Luke Sims  

This document introduces no requirements.  
All normative authority resides exclusively in the OPM Architectural Foundations and OPM Technical Specifications.

---

## What OPM Is

OPM is a publication architecture that makes:

- meaning explicit
- compatibility computable
- truth preservable

It separates — and prevents the collapse of:

- meaning and rendering
- compatibility and runtime success
- truth and policy

This separation is architectural, not optional.

---

## The One Rule Everything Follows

Truth is computed from declared inputs.  
Policy happens after truth.

Nothing below truth computation may influence what is true.

---

## The Five Layers (Strictly One-Way)

Declared Publication Semantics  
↓  
Deterministic Interpretation  
↓  
Compatibility Negotiation  
↓  
Validation & Reporting  
↓  
Policy / UX / Rendering  

Authority flows downward only.  
Rendering never creates truth.

---

## What a Publication Is (Architecturally)

A publication is not a file.

A publication is:

- a stable identity
- explicit structure (or none)
- declared reading order (or none)
- selector-addressable attachment surfaces
- declared capability reliance

If it is not declared, it does not exist.

---

## How Meaning Works

- Meaning is declared, never inferred
- Structure exists only if explicitly declared
- Attachments exist only via selectors
- Registries interpret identifiers; they never invent meaning

No heuristics.  
No repair.  
No guessing.

---

## How Compatibility Works

Compatibility is a computed fact, not an observation.

Computed from:

- declared publication capability reliance
- declared system capability support
- registry snapshots
- deterministic negotiation rules

Possible outcomes (exhaustive):

- **Compatible**
- **Incompatible**
- **Indeterminate**

There is no such thing as “mostly compatible.”

---

## What Validation Does (and Does Not Do)

Validation:

- verifies deterministic interpretation
- verifies compatibility computation
- records facts
- emits diagnostics
- discloses the Evaluation Context

Validation does **not**:

- repair content
- infer meaning
- enforce policy
- decide access
- soften outcomes

Validation records truth.  
It does not create it.

---

## What Policy Is Allowed to Do

Policy may:

- refuse to open
- open fully
- open under Degraded Open

Policy may never:

- change truth
- hide incompatibility
- rewrite outcomes
- claim support it does not have

Access is behavior.  
Truth is architectural.

---

## What OPM Never Does

OPM never:

- infers structure from markup
- infers accessibility from layout
- probes runtime features
- treats rendering success as support
- silently repairs meaning
- upgrades broken publications

If it’s not declared, it’s not true.

---

## The Minimum to Support a Real Book

To support a real publication (e.g. *Moby-Dick*), a system must be able to:

- compute semantic meaning deterministically
- resolve selectors deterministically
- compute compatibility truth honestly
- report outcomes reproducibly

Rendering alone is insufficient.

---

## EPUB vs OPM (Correctly Framed)

EPUB is a container and distribution format.  
OPM is a semantic and compatibility architecture.

OPM replaces EPUB at the authority level, not the ZIP level.

---

## Final Line

OPM is not about stricter publishing.

OPM is about making **truth impossible to fake**.
