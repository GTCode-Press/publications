# CNS 8.0 Test Plan

**Author:** GTCode Editorial
**Published:** May 15, 2026
**Canonical URL:** https://gtcode.com/guides/cns/test-plan/
**Section:** Guides
**License:** [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/)

---

# CNS 8.0 Test Plan

## Unit tests

- EvidenceAtom hashing and lookup.
- SNO schema validation.
- citation-validity rejection behavior.
- evidence entanglement calculation.
- graph chirality proxy.
- zero-temperature closure.
- proof trace recording.
- ZTHR calculation.
- residual tensor construction.
- predicate-invention utility.
- world posterior normalization.
- orthesis loop convergence.

## Integration tests

- evidence → Proposer → critic → SNO.
- SNO pair → pair selector → proof closure.
- proof closure → residual tensor → latent predicate.
- Synthesizer → re-grounding → orthesis report.
- final audit report.

## Property tests

- no strict claim without proof trace;
- no missing evidence ID can pass citation validator;
- adding unrelated evidence should not increase entanglement;
- possible-world posterior sums to 1;
- predicate complexity penalty lowers PIU.

## Regression tests

- citation hallucination case;
- unrelated disagreement case;
- true unresolved contradiction case;
- hidden subgroup synthetic case;
- round-trip drift case.

## Acceptance tests

- synthetic latent-context recovery above threshold;
- strict ZTHR equals 0;
- final report separates strict/likely/hypothesis/unresolved/rejected.

---

## How to Cite

**BibTeX:**

    @misc{gtcodeeditorial2026testplan,
      author  = {GTCode Editorial, },
      title   = {CNS 8.0 Test Plan},
      institution = {GTCode.com Guides},
      year    = {2026},
      month   = may,
      url     = {https://gtcode.com/guides/cns/test-plan/},
      note    = {Archived at \url{https://github.com/GTCode-Press/publications/tree/main/guides/cns/test-plan}}
    }

**APA:**
GTCode Editorial (2026, May 15). CNS 8.0 Test Plan. *GTCode.com Guides*. https://gtcode.com/guides/cns/test-plan/ (Archived at https://github.com/GTCode-Press/publications/tree/main/guides/cns/test-plan)

**Chicago:**
GTCode Editorial. "CNS 8.0 Test Plan." *GTCode.com Guides*, May 15, 2026. https://gtcode.com/guides/cns/test-plan/. Archived at https://github.com/GTCode-Press/publications/tree/main/guides/cns/test-plan.
