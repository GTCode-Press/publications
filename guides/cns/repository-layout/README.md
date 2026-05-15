# 25 — Repository Layout

**Author:** GTCode Editorial
**Published:** May 15, 2026
**Canonical URL:** https://gtcode.com/guides/cns/repository-layout/
**Section:** Guides
**License:** [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/)

---

# 25 — Repository Layout

## Recommended project structure

```text
cns8/
  pyproject.toml
  README.md
  configs/
    cns8_mvp.yaml
  cns8/
    evidence/
      store.py
      atom.py
      access.py
    sno/
      model.py
      parser.py
      align.py
    agents/
      proposer.py
      antagonist.py
      synthesizer.py
      orthesist.py
      auditor.py
    critics/
      grounding.py
      logic.py
      topology.py
      chirality.py
      access.py
      calibration.py
    tensor/
      rules.py
      closure.py
      proof.py
      residual.py
      predicate_invention.py
    worlds/
      build.py
      rank.py
      calibration.py
    reports/
      audit.py
      markdown.py
    runtime/
      manifest.py
      oracle_boundary.py
  tests/
    test_evidence_store.py
    test_sno_schema.py
    test_citation_validation.py
    test_zero_temp_closure.py
    test_chirality_entanglement.py
    test_predicate_invention_synthetic.py
    test_orthesis_loop.py
  experiments/
    synthetic_latent_context/
    scifact_grounding/
    productive_pair_selection/
  docs/
```

## Build sequencing

1. schema and evidence store;
2. SNO parser and validator;
3. critics;
4. pair selector;
5. proof closure;
6. predicate invention;
7. Synthesizer;
8. orthesis loop;
9. audit report;
10. dashboard.

## Test-first rule

Each new CNS mechanism gets a toy deterministic test before LLM integration.

## LLM isolation

The package should run in deterministic toy mode without any LLM API calls. LLM modules are adapters, not core proof machinery.

---

## How to Cite

**BibTeX:**

    @misc{gtcodeeditorial2026repositorylayout,
      author  = {GTCode Editorial, },
      title   = {25 — Repository Layout},
      institution = {GTCode.com Guides},
      year    = {2026},
      month   = may,
      url     = {https://gtcode.com/guides/cns/repository-layout/},
      note    = {Archived at \url{https://github.com/GTCode-Press/publications/tree/main/guides/cns/repository-layout}}
    }

**APA:**
GTCode Editorial (2026, May 15). 25 — Repository Layout. *GTCode.com Guides*. https://gtcode.com/guides/cns/repository-layout/ (Archived at https://github.com/GTCode-Press/publications/tree/main/guides/cns/repository-layout)

**Chicago:**
GTCode Editorial. "25 — Repository Layout." *GTCode.com Guides*, May 15, 2026. https://gtcode.com/guides/cns/repository-layout/. Archived at https://github.com/GTCode-Press/publications/tree/main/guides/cns/repository-layout.
