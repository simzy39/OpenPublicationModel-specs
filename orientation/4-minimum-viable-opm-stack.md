# Minimum Viable OPM Stack
## What you actually need to implement OPM — and nothing you don’t

**Status:** Non-Normative  
**Authority:** None  
**Purpose:** Practical architectural guidance  
**Audience:** Platform architects, implementers, validators, libraries  
**Author:** Heath Luke Sims  

This document introduces no requirements.  
All normative authority resides exclusively in the OPM Architectural Foundations and Normative Technical Specifications.

---

## What This Document Is For

This document answers one question only:

> **What is the smallest, honest architecture required to say  
> “we support OPM publications”?**

It does not describe:

- what you might implement later
- what improves UX
- what helps onboarding or sales
- what “works in practice”

It describes only the irreducible minimum required to:

- compute OPM semantic truth
- compute compatibility truth
- report facts honestly
- preserve those facts across time

Anything less is not partial support.  
It is **non-support**.

---

## One Critical Clarification (Read This First)

**Rendering is not support.**

A system that:

- opens files
- displays text
- scrolls pages
- plays audio

—but cannot compute semantic truth and compatibility truth—

does **not** support OPM, even if the content “works”.

This stack defines what **support actually means**.

---

## The Minimum Viable OPM Stack (Overview)

To support a real OPM publication — from a flyer to *Moby-Dick* — a system must be able to do four things:

- interpret declared meaning deterministically
- compute compatibility deterministically
- record and report facts honestly
- preserve truth across time

Everything else is optional.

---

## Layer 1 — Semantic Interpretation (Required)

This layer answers:

> **What does this publication mean?**

You must implement:

- Core Semantic Model
- Selectors & Structural Addressing

You must be able to:

- recognize a publication as a semantic entity
- resolve declared structure (or fail deterministically)
- resolve selectors deterministically (or fail)
- produce a Canonical Semantic Interpretation Record (CSIR)

You must also have, locally and offline:

- Media Type Registry snapshots (for structural models)
- Semantic Terms Registry snapshots

You must **not**:

- infer structure from markup
- infer reading order
- infer navigation
- repair missing declarations

If you cannot produce a stable CSIR,  
**OPM support stops here**.

---

## Layer 2 — Compatibility Evaluation (Required)

This layer answers:

> **Does this system support what the publication relies on?**

You must implement:

- Capability Profiles
- Profile Registry (via offline snapshots)
- Profile Negotiation
- Capability Degradation Semantics

You must be able to:

- read declared publication capability reliance
- declare your system’s supported capabilities
- compute **exactly one** outcome:
  - Compatible
  - Incompatible
  - Indeterminate

You must:

- emit stable, machine-readable reason codes
- treat missing authority as **Indeterminate**

You must **not**:

- infer support from rendering success
- probe features at runtime
- soften outcomes
- collapse incompatibility into warnings

If you cannot compute compatibility deterministically,  
**you cannot claim support**.

---

## Layer 3 — Validation & Reporting (Required)

This layer answers:

> **What facts were observed, and how were they computed?**

You must implement:

- Validation & Conformance (OPMCheck)

You must be able to:

- verify semantic interpretation against the CSIR
- verify compatibility computation correctness
- record registry snapshot identifiers
- emit deterministic diagnostics

You must **not**:

- repair publications
- enforce policy
- decide access
- hide failures

Validation reports facts.  
It does **not** decide outcomes.

---

## Layer 4 — Outcome Handling  
### (Policy Layer — Optional)

This layer answers:

> **What do we choose to do now that we know the truth?**

Governed by:

- Outcome Handling & Degraded Open

You may choose to:

- refuse access
- open with full support
- open under Degraded Open

You must:

- preserve compatibility outcomes verbatim
- preserve reason codes verbatim
- disclose degradation durably

You must **not**:

- claim support under Degraded Open
- rewrite incompatibility
- treat access as evidence

Policy is allowed.  
Policy is **not truth**.

---

## Bindings (Conditionally Required)

Bindings are required only if your system:

- emits exchange artifacts, or
- ingests artifacts for custody or distribution

Bindings:

- carry declared meaning
- do not define meaning
- do not affect compatibility

You may support:

- ZIP
- TAR
- directories
- content-addressed bindings

Bindings are **never** part of the semantic minimum.

---

## What Is Explicitly Not Required

The following are **not** part of the minimum viable stack:

- UI or UX work
- rendering engines
- EPUB compatibility layers
- OPDS or catalog protocols
- DRM systems
- recommendation logic
- accessibility heuristics
- metadata enrichment
- completeness or readiness classification

You may implement all of these —  
but **none of them create OPM support**.

---

## What “Minimum” Really Means

Minimum does **not** mean:

- trivial
- simplistic
- weak
- toy-grade

It means:

- no inference
- no ambiguity
- no hidden authority
- no deceptive claims

A system that meets this minimum can honestly support:

- a flyer
- a novel
- *Moby-Dick*

Anything less cannot.

---

## Claim Boundary (Read Carefully)

You may claim:

> **“We support OPM publications”**

**if and only if** you implement this stack.

If you only render content, you may claim:

- viewer
- renderer
- consumer

Those are legitimate roles.  
They are **not OPM support**.

---

## Why This Stack Exists

This minimum exists to ensure that:

- accessibility claims are structural
- compatibility claims are auditable
- preservation is real
- generosity does not become deception

It is intentionally boring.

That is the point.
