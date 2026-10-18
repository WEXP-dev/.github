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
  interoperability records for WEXP and external systems. Interop records test
  cross-system semantic mappings under frozen expectations and explicit claim
  boundaries; an experiment may validly terminate in non-equivalence or an
  explicit bridge requirement.
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
- Public Core `-01` vector sets are published in
  [`wexp-vectors`](https://github.com/WEXP-dev/wexp-vectors), which carries the
  current sets, their exact identities, and their specification binding. They
  are specification-derived: every expected outcome is transcribed from
  published specification text, never from observed implementation behaviour. A
  Core `-00` candidate set remains available. **No set is a conformance
  suite**; passing one means an implementation agreed with expectations derived
  from the specification, and is not certification. A vector count is not a
  maturity measure and is not maintained here.
- Public Core `-01` reference tooling exists in `wexp-ref`. Its Core-01
  conformance is **`PARTIAL` by design** — a deliberate, enumerated partial
  surface with its absences listed, not a claim of complete Core appraisal. It
  consumes the vectors at a pinned commit and does not define protocol
  semantics; where it and a specification disagree, the specification wins.
- Experimental interoperability records, including WEXP × EMILIA and
  WEXP × WIMSE AAR-02, are indexed in the
  [versioned collection](https://github.com/WEXP-dev/wexp-interop#experimental-records).
  Use each package's result, exact carrier and reproduction scope. A collection
  entry is not a conformance, certification or general interoperability claim;
  the catalog, rather than a count copied here, is the navigation source.
- `interop-test-lab` is an **experimental Prototype-000 lab**: disposable test
  infrastructure for running an interoperability exercise between WEXP and a
  synthetic counterparty. It is not a production platform, not a generic
  interoperability framework proven portable, not conformance infrastructure,
  and not a certification system.
- WEXP Native Record is **not published**. No Native Record revision has been
  submitted to or posted by the IETF.

## Preparing a revision

The [publication process](https://github.com/WEXP-dev/wexp-spec/blob/main/PUBLICATION-PROCESS.md)
separates a frozen candidate, exact author approval, submission and verification
of the official archive. [Tooling guidance](https://github.com/WEXP-dev/wexp-spec/blob/main/publication/README.md)
explains the manual default and optional transport. CI and experimental results
do not authorize publication or establish specification conformance.

## What none of this is

Nothing published here is an Internet Standard, a certification, a conformance
programme, or an IETF endorsement.
