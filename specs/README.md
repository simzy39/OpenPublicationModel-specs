# Open Publication Model (OPM) — Technical Specifications

This directory contains the **normative technical specifications** of the Open Publication Model (OPM).

These specifications define the detailed rules, data models, and processing requirements required to implement OPM. All specifications in this directory are **normative** unless explicitly stated otherwise.

---

## Authority

All technical specifications in this directory are governed by the **OPM Architectural Foundations**.

The Architectural Foundations define:
- architectural boundaries
- authority flow
- interpretation constraints
- rules for extension and evolution

No technical specification may contradict or override the Architectural Foundations.

---

## Structure

Specifications are grouped by primary concern:

- **`core/`**  
  Core semantic concepts, publication identity, declared meaning, and foundational models.

- **`selectors/`**  
  Structural addressing, selector semantics, attachment rules, and resolution behavior.

- **`capabilities/`**  
  Capability profiles, negotiation rules, degradation semantics, and compatibility computation.

- **`validation/`**  
  Validation, conformance, reporting, and diagnostic requirements (including OPMCheck).

- **`bindings/`**  
  Container and transport bindings (e.g., EPUB, ZIP), defining how OPM declarations are carried without defining semantic authority.

- **`registries/`**  
  Registry definitions, snapshot rules, identifier governance, and authority flow for shared vocabularies.

This structure is organizational only.  
Normative relationships are defined by specification text, not directory layout.

---

## Normative Language

Specifications use normative requirement keywords such as **MUST**, **MUST NOT**, **SHOULD**, and **MAY** as defined in the relevant specifications.

---

## Scope and Intent

These specifications are intended to:

- enable deterministic interpretation of publications
- make compatibility and support claims computable
- preserve semantic truth across time and systems
- support auditability, custody, and long-term preservation

They are not intended to:
- prescribe user interfaces or UX behavior
- mandate business or institutional policy
- define product features or workflows

---

## Reading Guidance

Readers new to OPM are strongly encouraged to read the **orientation documents** and **Architectural Foundations** before engaging with the technical specifications.

The specifications assume familiarity with the architectural constraints established elsewhere in this repository.

---

## Status

Specifications may evolve over time as edge cases are explored and implementation feedback is incorporated. Changes are made deliberately and with respect to architectural stability.

No claim of completeness or adoption is implied.
