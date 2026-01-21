# Open Publication Model (OPM) — Specifications

This repository contains the **architectural foundations and specification corpus** for the **Open Publication Model (OPM)**.

OPM defines a semantic and compatibility architecture for digital publications, with an emphasis on **explicit meaning**, **deterministic interpretation**, **auditability**, and **long-term preservation**.

This repository is **not a product** and does not assume adoption or implementation. It exists to define the problem space and architectural constraints clearly and honestly.

---

## Repository Scope

This repository contains:

- Non-normative orientation documents
- Architectural Foundations
- Normative technical specifications

This repository does **not** contain:

- Product implementations
- Validation tools or QA software
- EPUB readers or platforms
- Commercial services
- Reference code

Those concerns are intentionally out of scope.

---

## How to Read OPM

OPM is not designed to be discovered by reading isolated specifications.

Readers new to OPM should begin with the **orientation documents**, which establish the architectural boundaries and mental models required to read the specifications correctly.

Recommended entry order:

1. *What OPM Is (and Is Not)*
2. *OPM in One Page*
3. *OPM in One Diagram*
4. *Minimum Viable OPM Stack*

The Architectural Foundations and technical specifications assume familiarity with these documents.

---

## Status

OPM is under active development.

- Architectural principles are considered **stable**
- Specifications may evolve as edge cases and implementation feedback are explored

No claim of completeness, adoption, or endorsement is made.

---

## Governance and Contributions

This project follows a **single-maintainer / central editorial authority** model to preserve architectural coherence.

Contributions, feedback, and critique are welcome, but final decisions on specification content rest with the maintainer.

See `CONTRIBUTING.md` for details.

---

## License and Patent Policy

The contents of this repository are governed by:

- the **Open Publication Model Specification License** (see `LICENSE`)
- the **Open Publication Model Patent Policy** (see `PATENT-POLICY`)

Together, these are intended to encourage broad scrutiny, implementation, and use of the specifications while preserving clear attribution and reducing patent uncertainty.

---

## Maintainer

OPM is authored and maintained by **Heath Luke Sims**.

---

## Related Work

OPM is independent of, but related to, other efforts in digital publishing and library infrastructure.

For example, the **Library Catalog Access Protocol (LCAP)** defines a discovery and access protocol for library catalogs. LCAP does not depend on OPM, but may benefit from OPM-modeled digital publications.

---

## Intent

OPM is not trying to be everything.

OPM exists to make **truth about digital publications explicit and impossible to fake**.

Everything else follows from that.
