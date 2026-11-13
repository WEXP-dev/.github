# WEXP

WEXP (Witnessed Execution Protocol) is an IETF-oriented specification effort
for evaluating support for claims about software and AI execution within
explicit evidence and observation boundaries.

Appraisal Core and Coverage are separate specifications: Core evaluates support
for execution-related claims about exact targets; Coverage evaluates bounded
population and record-correspondence claims. Neither replaces a recipient's
application decision.

The specifications define WEXP. Test vectors and the reference implementation
help developers use the specifications; they do not add or change requirements.

## Repositories

- [wexp-appraisal-core-spec](https://github.com/WEXP-dev/wexp-appraisal-core-spec) —
  published WEXP Core revisions and their provenance. **Core specification authority.**
- [wexp-coverage-spec](https://github.com/WEXP-dev/wexp-coverage-spec) — published Coverage specification and artifact provenance. **Coverage specification authority.**
- [wexp-vectors](https://github.com/WEXP-dev/wexp-vectors) —
  schemas and validation tools for implementation-independent WEXP test vectors.
- [wexp-ref](https://github.com/WEXP-dev/wexp-ref) — the reference
  implementation and generic execution tools.
- [wexp-check](https://github.com/WEXP-dev/wexp-check) — a second Core-02
  appraiser, written in a separate AI-assisted session operated by the same
  person as `wexp-ref`. That the session did not consult `wexp-ref` or any WEXP
  corpus expectations is an operator declaration and has not been independently
  verified; the `wexp-ref` Core-02 module was public before `wexp-check` started.
  Its initial version was frozen before the first recorded corpus comparison;
  later changes are documented.
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

- The current Core specification is
  [`draft-sergeev-wexp-core-02`](https://datatracker.ietf.org/doc/draft-sergeev-wexp-core/02/),
  dated 23 October 2026 and published at the IETF. It is an Internet-Draft, not an Internet
  Standard. Being posted is not working-group adoption, consensus, or
  standardization.
- [`draft-sergeev-wexp-core-00`](https://datatracker.ietf.org/doc/draft-sergeev-wexp-core/00/)
  remains available, as does [`draft-sergeev-wexp-core-01`](https://datatracker.ietf.org/doc/draft-sergeev-wexp-core/01/), the immediately preceding Core revision.
- [`draft-sergeev-wexp-coverage-00`](https://datatracker.ietf.org/doc/draft-sergeev-wexp-coverage/00/) (Coverage-00) is also published. Its bounded coverage claims and outcomes are separate from Core appraisals.
- The historical vector sets and the Core `-01` reference tooling below remain bound to Core-01; publication of Core-02 does not establish their conformance to Core-02.
- Separately, two bounded Core-02 corpora are published in `wexp-vectors` at commit `edd67056`:
  [`WEXP-CORE-02-VECTORS-001`](https://github.com/WEXP-dev/wexp-vectors/tree/edd67056873502a2c3cecf5dd2b8db71271c2f57/vectors/WEXP-CORE-02-VECTORS-001)
  (89 complete cases with frozen `corpus.json`, package revision 2) and
  [`WEXP-CORE-02-VECTORS-002`](https://github.com/WEXP-dev/wexp-vectors/tree/edd67056873502a2c3cecf5dd2b8db71271c2f57/vectors/WEXP-CORE-02-VECTORS-002)
  (35 cases: the 32 section 7 Boundary Ceiling matrix cells that set 001 leaves empty, two
  section 12 scope controls and one acceptance probe). Two Core-02 appraisers under one operator
  are published: the version-scoped module in `wexp-ref` at commit `56289024`
  ([surface and limits](https://github.com/WEXP-dev/wexp-ref/blob/56289024c9ee748111f1f1d4f42728ffe04d8d69/CORE02-CONFORMANCE.md))
  and [`wexp-check`](https://github.com/WEXP-dev/wexp-check), appraiser code `a2fd1ffd`. The
  initial `wexp-check` version was frozen before the first corpus comparison, where it agreed
  with the expectations on 122 of 124 cases; the two interpretation differences were aligned
  toward the corpus reading, and these alignments and later fixes are documented, so the pinned
  code is not the code as frozen. At these revisions `wexp-check` agrees with the frozen
  expectations and with the `wexp-ref` output on 124/124 cases (89/89 and 35/35). These
  original comparison runs were performed under the same operator and do not establish
  independent implementation provenance. On 10 November 2026 Laurent Lemonnier replayed the
  unit tests and both comparisons in GitHub Actions in his own repository at the same pinned
  revisions
  ([record](https://github.com/WEXP-dev/wexp-check/blob/4af1e69d5f9b3e28ed8efffba07e188a26a25828/reproductions/2026-11-10-lemonnier/README.md));
  this is a real repetition of the comparison by a third-party operator on pinned revisions of
  code and inputs, with the same code and public expectations, not an independent
  implementation. Agreement with these corpora is bounded author-side qualification,
  not full Core-02 conformance, carrier or AAC/WIMSE interoperability, or a new interop result.
  A bounded Coverage-00 logical test package,
  [`WEXP-COVERAGE-00-LOGIC-001`](https://github.com/WEXP-dev/wexp-vectors/tree/edd67056873502a2c3cecf5dd2b8db71271c2f57/vectors/WEXP-COVERAGE-00-LOGIC-001),
  is published in `wexp-vectors`; it is not a full Coverage evaluator, not a conformance suite and
  not validation of the optional `pg-ledger/0.2.0` deployment profile. No full Coverage evaluator
  or `pg-ledger/0.2.0` implementation is published.
- Public Core `-01` vector sets are published in
  [`wexp-vectors`](https://github.com/WEXP-dev/wexp-vectors), which carries the
  current sets, their exact identities, and their specification binding. They
  are specification-derived: each expected outcome is transcribed from a fixture
  the specification states or derived from its normative text, never from
  observed implementation behaviour. A
  Core `-00` candidate set remains available. **No set is a conformance
  suite**; passing one means an implementation agreed with expectations derived
  from the specification, and is not certification. A vector count is not a
  maturity measure and is not maintained here.
- Public Core `-01` reference tooling exists in `wexp-ref`. Its Core-01
  conformance is **`PARTIAL` by design** — a deliberate, enumerated partial
  surface with its absences listed, not a claim of complete Core appraisal. It
  consumes the vectors at a pinned commit and does not define protocol
  semantics; where it and a specification disagree, the specification wins.
- Experimental interoperability records, including WEXP × EMILIA (INTEROP-001 and
  INTEROP-002; the historical INTEROP-002 result was published on Zenodo on 12 November 2026,
  [version DOI 10.5281/zenodo.24180793](https://doi.org/10.5281/zenodo.24180793)),
  WEXP × WIMSE AAR-02, and the SCITT Receipt as the Core-02 boundary finding, are indexed in the
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

The [publication process](https://github.com/WEXP-dev/wexp-appraisal-core-spec/blob/main/PUBLICATION-PROCESS.md)
separates a frozen candidate, exact author approval, submission and verification
of the official archive. [Tooling guidance](https://github.com/WEXP-dev/wexp-appraisal-core-spec/blob/main/publication/README.md)
explains the release-triggered GitHub submission procedure and manual alternative. CI and experimental results
do not authorize publication or establish specification conformance.

## What none of this is

Nothing published here is an Internet Standard, a certification, a conformance
programme, or an IETF endorsement.
