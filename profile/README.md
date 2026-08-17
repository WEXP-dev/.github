# WEXP

WEXP (Witnessed Execution Protocol) is an IETF-oriented specification effort
for evaluating support for claims about software and AI execution within
explicit evidence and observation boundaries.

The specifications define WEXP. Test vectors and the reference implementation
help developers use the specifications; they do not add or change requirements.

## Repositories

- [wexp-spec](https://github.com/WEXP-dev/wexp-spec) — published WEXP
  specifications and their provenance.
- [wexp-vectors](https://github.com/WEXP-dev/wexp-vectors) —
  schemas and validation tools for implementation-independent WEXP test vectors.
- [wexp-ref](https://github.com/WEXP-dev/wexp-ref) — the reference
  implementation and generic execution tools.

## Current status

- The current specification is
  [`draft-sergeev-wexp-core-01`](https://datatracker.ietf.org/doc/draft-sergeev-wexp-core/01/),
  posted at the IETF on 2026-08-17. It is an Internet-Draft, not an Internet
  Standard. Being posted is not working-group adoption, consensus, or
  standardization.
- [`draft-sergeev-wexp-core-00`](https://datatracker.ietf.org/doc/draft-sergeev-wexp-core/00/)
  is the previous revision and remains available.
- Public Core `-01` test vectors exist: `WEXP-CORE-01-VECTORS-001`, sixteen
  vectors transcribed from the draft's normative fixtures. They are a reference
  corpus, not an IETF conformance suite; passing them is not certification.
- Public Core `-01` reference tooling exists in `wexp-ref`. It consumes the
  vectors at a pinned commit and does not define protocol semantics — where it
  and a specification disagree, the specification wins.
- WEXP Native Record is **not published**. No Native Record revision has been
  submitted to or posted by the IETF.
