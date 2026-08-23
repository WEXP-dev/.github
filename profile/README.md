# WEXP

WEXP (Witnessed Execution Protocol) is an IETF-oriented specification effort
for evaluating support for claims about software and AI execution within
explicit evidence and observation boundaries.

The specifications define WEXP. Test vectors and the reference implementation
help developers use the specifications; they do not add or change requirements.

## Repositories

- [wexp-spec](https://github.com/WEXP-dev/wexp-spec) — published WEXP
  specifications and their provenance. **Authoritative.**
- [wexp-vectors](https://github.com/WEXP-dev/wexp-vectors) —
  schemas and validation tools for implementation-independent WEXP test vectors.
- [wexp-ref](https://github.com/WEXP-dev/wexp-ref) — the reference
  implementation and generic execution tools.
- [wexp-interop](https://github.com/WEXP-dev/wexp-interop) — experimental
  interoperability records for WEXP and external systems.
- [interop-test-lab](https://github.com/WEXP-dev/interop-test-lab) and
  [interop-test-subject](https://github.com/WEXP-dev/interop-test-subject) —
  experimental interoperability test infrastructure for the Prototype-000 lab,
  and the synthetic counterparty it exercises.

## Current status

- The current specification is
  [`draft-sergeev-wexp-core-01`](https://datatracker.ietf.org/doc/draft-sergeev-wexp-core/01/),
  posted at the IETF on 2026-08-17. It is an Internet-Draft, not an Internet
  Standard. Being posted is not working-group adoption, consensus, or
  standardization.
- [`draft-sergeev-wexp-core-00`](https://datatracker.ietf.org/doc/draft-sergeev-wexp-core/00/)
  is the previous revision and remains available.
- Two public Core `-01` vector sets exist: `WEXP-CORE-01-VECTORS-001`, sixteen
  vectors transcribed from the draft's normative fixtures C01–C16, and
  `WEXP-CORE-01-VECTORS-002`, nine further vectors that widen coverage. Both
  are specification-derived. Seven Core `-00` vectors remain available as a
  candidate set. **No set is a conformance suite**; passing one means an
  implementation agreed with expectations derived from the specification, and
  is not certification.
- Public Core `-01` reference tooling exists in `wexp-ref`. Its Core-01
  conformance is **`PARTIAL` by design** — a deliberate, enumerated partial
  surface with its absences listed, not a claim of complete Core appraisal. It
  consumes the vectors at a pinned commit and does not define protocol
  semantics; where it and a specification disagree, the specification wins.
- One experimental interoperability record is published:
  [**INTEROP-001**](https://github.com/WEXP-dev/wexp-interop) (WEXP × EMILIA,
  DOI [`10.5281/zenodo.22056151`](https://doi.org/10.5281/zenodo.22056151)).
  It is bounded evidence from a controlled experiment with independently frozen
  readings and expectations. Its terminal result is *Explicit Bridge Required*.
  It establishes no semantic equivalence, no mutual validation, no conformance,
  no certification, no adopted mapping, and no general interoperability claim.
- `interop-test-lab` is an **experimental Prototype-000 lab**: disposable test
  infrastructure for running an interoperability exercise between WEXP and a
  synthetic counterparty. It is not a production platform, not a generic
  interoperability framework proven portable, not conformance infrastructure,
  and not a certification system.
- WEXP Native Record is **not published**. No Native Record revision has been
  submitted to or posted by the IETF.

## What none of this is

Nothing published here is an Internet Standard, a certification, a conformance
programme, or an IETF endorsement.
