# OPM in One Diagram
## Architecture, Authority, and Truth Flow

**Status:** Non-Normative  
**Authority:** None  
**Role:** Architectural overview (illustrative; no enforcement authority)  
**Author:** Heath Luke Sims  

This document introduces no requirements.  
All normative authority resides exclusively in the OPM Architectural Foundations and the OPM Specification Corpus.

---

```text
┌──────────────────────────────────────────────────────────────────────────┐
│                        PUBLICATION (declares)                            │
│                                                                          │
│   • Stable publication identity                                          │
│   • Explicit semantic entities and declared structure                    │
│   • Declared reading order (if any)                                      │
│   • Selectors (exclusive semantic attachment; no inference)              │
│   • Declared capability reliance                                         │
│   • Binding identity only (no semantic authority)                        │
│                                                                          │
└──────────────────────────────────────────────────────────────────────────┘
                                   │
                                   │  (declared inputs only)
                                   ▼
┌──────────────────────────────────────────────────────────────────────────┐
│  LAYER 1 -- SEMANTIC INTERPRETATION                                      │
│            (Truth of meaning)                                            │
│                                                                          │
│  Specifications:                                                         │
│   • Core Semantic Model                                                  │
│   • Selectors & Structural Addressing                                    │
│                                                                          │
│  Authoritative inputs:                                                   │
│   • Publication declarations                                             │
│   • Registry snapshots                                                   │
│     (semantic terms, media types, structural models)                     │
│                                                                          │
│  Output:                                                                 │
│   • CSIR -- Canonical Semantic Interpretation Record                     │
│                                                                          │
│  Hard boundaries:                                                        │
│   • No inference                                                         │
│   • No heuristics                                                        │
│   • No runtime probing                                                   │
│   • Selector resolution is deterministic or fails                        │
│   • Interpretation is computed once and closed in the CSIR               │
│                                                                          │
└──────────────────────────────────────────────────────────────────────────┘
                                   │
                                   │  (semantic truth is now immutable)
                                   ▼




┌──────────────────────────────────────────────────────────────────────────┐
│  LAYER 4 -- OUTCOME HANDLING (POLICY)                                    │
│            (Behavior after truth)                                        │
│                                                                          │
│  Specification:                                                          │
│   • Outcome Handling & Degraded Open                                     │
│                                                                          │
│  Permitted actions:                                                      │
│   • Refuse access                                                        │
│   • Open with full support                                               │
│   • Open under Degraded Open                                             │
│                                                                          │
│  Hard constraints:                                                       │
│   • Compatibility outcomes are preserved verbatim                        │
│   • Reason identifiers are preserved verbatim                            │
│   • Degradation is disclosed durably                                     │
│   • Unmet support is never claimed                                       │
│   • Indeterminate remains unknown                                        │
│                                                                          │
└──────────────────────────────────────────────────────────────────────────┘
                                   │
                                   │  (downstream behavior only)
                                   ▼
┌──────────────────────────────────────────────────────────────────────────┐
│                     RENDERING / UX / DELIVERY                            │
│                                                                          │
│   • UI choices, warnings, and workflows                                  │
│   • Marketplace and institutional rules                                  │
│   • Accessibility heuristics (behavior, not truth)                       │
│   • MAY be generous with access                                          │
│   • MUST NOT rewrite semantic or compatibility truth                     │
│                                                                          │
└──────────────────────────────────────────────────────────────────────────┘


Key Architectural Boundary (Read Once)
Semantic meaning is fixed here ───────────────┐
                                              │
Compatibility is computed here ───────────────┤  Truth is immutable
                                              │
Validation records facts ─────────────────────┤
                                              │
Policy decides behavior ──────────────────────┘
           (policy never decides truth)

Everything above the policy line is audit-grade truth.
