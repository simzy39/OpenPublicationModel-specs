# What OPM Is (and Is Not)
## Setting the Boundary Before the Details

**Status:** Non-Normative  
**Authority:** None  
**Purpose:** Boundary-setting and misconception prevention  
**Audience:** Publishers, platform architects, standards bodies, library systems, implementers  
**Author:** Heath Luke Sims  

This document introduces no requirements.  
All normative authority resides exclusively in the OPM Architectural Foundations and the OPM Specification Corpus.

This document exists to ensure that OPM is not misunderstood before any technical reading begins.

---

## How to Read OPM (Important)

OPM is not designed to be discovered by reading isolated specifications.  
It is designed to be understood as a system.

OPM itself consists of a large, explicit corpus of specifications.  
The documents listed here are **non-spec orientation materials** whose sole purpose is to prepare readers to enter that specification corpus correctly.

Before reading the OPM Architectural Foundations or any other OPM specification, readers are expected to read the following orientation documents, in order:

1. **What OPM Is (and Is Not)**
2. **OPM in One Page**
3. **OPM in One Diagram**
4. **Minimum Viable OPM Stack**

These documents:

- introduce no requirements
- carry no normative authority

They exist solely to establish the architectural boundaries, mental models, and expectations required to read the OPM specifications correctly.

The following documents provide worked examples and navigation support and may be read as needed:

- *A Real Book Walkthrough: Moby-Dick*
- *EPUB → Core Text: A Concrete Walkthrough*
- *OPM Specification Map*

Readers who skip the required orientation documents will almost certainly misunderstand the specifications — not because the specifications are unclear, but because OPM intentionally rejects many EPUB-era assumptions.

---

## 1. Why This Document Exists

Most misunderstandings of OPM do not come from reading its specifications incorrectly.

They come from bringing EPUB-era assumptions into OPM before reading anything at all.

If you approach OPM assuming that:

- inference is acceptable
- rendering success implies support
- accessibility can be “figured out” at runtime
- compatibility is approximate or negotiable
- policy can quietly override truth

then you are not misunderstanding a detail —  
you are misunderstanding the system.

This document exists to draw that line before any OPM specification is read.

---

## 2. What OPM Is

OPM is a semantic and architectural model for publications.

It defines:

- what a publication is
- where semantic meaning is allowed to come from
- how compatibility is computed
- how truth is preserved across time
- what systems may truthfully claim

OPM is concerned with **truth**, not behavior.

### Declarative by Design

OPM is strictly declarative.

In OPM:

- meaning exists only if explicitly declared
- structure exists only if explicitly declared
- traversal exists only if explicitly declared
- accessibility exists only if explicitly declared
- capability reliance exists only if explicitly declared

If something is not declared, it does not exist for semantic purposes.

### Deterministic and Auditable

Given:

- the same publication declarations
- the same registry snapshots
- the same system capability declarations

OPM guarantees:

- the same semantic truth
- the same compatibility outcomes
- the same diagnostics

Across platforms.  
Across institutions.  
Across time.

This is not a goal.  
It is a design constraint.

### Designed for Custody and Preservation

OPM assumes that:

- publications outlive software
- platforms change
- ecosystems fragment
- interpretation must remain reproducible

OPM is designed so libraries and archives can preserve meaning, not merely bytes or frozen behavior.

### A Replacement at the Authority Level

OPM replaces EPUB at the **authority level**.

It does not replace EPUB as a ZIP container or packaging convention.

It replaces EPUB where EPUB fails:

- semantic authority
- compatibility truth
- accessibility guarantees
- auditability
- long-term interpretability

---

## 3. What OPM Is Not

### Not a File Format

OPM is not a file format.

It does not define:

- ZIP layouts
- directory structures
- packaging conventions
- transport mechanisms

Those are bindings.

Bindings may carry declared meaning.  
They do not define it.

### Not a Rendering System

OPM does not define:

- layout
- pagination
- styling
- UI behavior
- reading experience

Rendering is downstream behavior.  
Rendering never creates truth.

### Not Heuristic

OPM explicitly forbids:

- inferring structure from markup
- inferring reading order from files
- inferring accessibility from layout
- probing runtime features
- “best-effort” semantic repair

If inference is required, OPM returns **Indeterminate** — not a guess.

### Not Policy

OPM does not decide:

- whether something should open
- whether degraded access is acceptable
- how users are warned
- how institutions apply rules

Policy happens after truth is known.  
Policy may never rewrite truth.

### Not “It Works on My Device”

Rendering success:

- is not compatibility
- is not support
- is not evidence
- is not authority

OPM treats “it rendered” as a non-semantic fact.

### Not Backward-Compatible with Bad Assumptions

OPM does not:

- silently upgrade broken publications
- guess publisher intent
- normalize underspecified content
- pretend missing semantics exist

Silence is failure.  
Failure is information.

---

## 4. What OPM Refuses to Do (On Purpose)

OPM refuses to:

- blur meaning and behavior
- trade correctness for convenience
- hide incompatibility behind UX
- launder policy into claims
- allow partial truth

These are not oversights.  
They are architectural decisions.

---

## 5. “This Sounds Strict” — Correct

OPM is strict because publishing has suffered from:

- decades of implicit semantics
- inaccessible content disguised as accessible
- compatibility claims that cannot be verified
- preservation systems that preserve behavior instead of meaning

OPM chooses:

- honesty over convenience
- determinism over optimism
- declaration over inference
- auditability over folklore

---

## 6. If You Ignore These Boundaries

A system that:

- infers meaning
- repairs semantics heuristically
- treats rendering success as support
- suppresses incompatibility
- overclaims capability

may still function.

It is simply not implementing OPM.

OPM has no central enforcement body.  
Its enforcement mechanism is architectural truth.

---

## 7. How to Enter the OPM Specification Corpus

If you agree with the boundaries established in this document, you are now prepared to read the OPM specifications themselves.

Recommended sequence:

1. **OPM in One Page** — architectural shape
2. **OPM in One Diagram** — authority and truth flow
3. **Minimum Viable OPM Stack** — claim boundaries
4. **Architectural Foundations (Parts A–H)** — constitutional architecture
5. The relevant technical specifications from the full OPM specification corpus, according to your role or use case

If you disagree with the boundaries in this document,  
OPM is not the system you are looking for.

That clarity is intentional.

---

## Final Statement

OPM is not trying to be everything.

OPM is trying to make **truth impossible to fake**.

Everything else follows from that.
