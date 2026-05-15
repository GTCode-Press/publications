# 15 — Risk Register and Failure Modes

**Author:** GTCode Editorial
**Published:** May 15, 2026
**Canonical URL:** https://gtcode.com/guides/cns/adversarial-evidence/
**Section:** Guides
**License:** [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/)

---

# 15 — Risk Register and Failure Modes

## Risk 1 — Reverting to verification/ranking

Symptom: final output is top worlds or claim labels but no synthesized SNO.

Mitigation: every run must emit SNO lineage and synthesis status.

## Risk 2 — LLM judgments

Symptom: an LLM judge decides which narrative is true.

Mitigation: LLMs can propose or render; proof gates and calibrated models decide promotion categories.

## Risk 3 — Predicate overfit

Symptom: latent predicates explain training contradictions but fail held-out examples.

Mitigation: MDL penalty, held-out synthetic contexts, grounding gates, false predicate rate.

## Risk 4 — Access-state misuse

Symptom: missing records are treated as evidence.

Mitigation: access-state critic; separate absence-of-evidence from evidence-of-absence.

## Risk 5 — Round-trip drift

Symptom: synthesized text re-grounds into a different logic state.

Mitigation: orthesis loop; $\chi_{LL}$ threshold.

## Risk 6 — Topology theater

Symptom: topology terms appear but metrics are not used in decisions.

Mitigation: make beta-1, holonomy residual, and topology diagnostics part of acceptance criteria or remove them.

## Risk 7 — Grounding destroys synthesis

Symptom: system becomes conservative fact checking and never creates new SNOs.

Mitigation: preserve Synthesizer and predicate invention; classify hypotheses separately instead of blocking all novelty.

## Risk 8 — Synthesis hides contradiction

Symptom: fluent narrative erases unresolved conflict.

Mitigation: residual contradiction section required in audit report.

## Risk 9 — Prior-art soup

Symptom: doc reads like a collection of known systems.

Mitigation: keep the SNO synthesis flow visible and evaluate module interactions/ablations.

## Risk 10 — Dataset leakage

Symptom: labels or synthetic generator parameters appear in runtime.

Mitigation: oracle-boundary audit, split hashes, prompt scans.

## Risk 11 — Citation hallucination

Symptom: evidence IDs do not resolve.

Mitigation: reject invalid inputs; citation validity required check.

## Risk 12 — Calibration laundering

Symptom: likely claims are written as strict claims.

Mitigation: output category enforcement and confidence language table.

---

## How to Cite

**BibTeX:**

    @misc{gtcodeeditorial2026adversarialevidence_c425,
      author  = {GTCode Editorial, },
      title   = {15 — Risk Register and Failure Modes},
      institution = {GTCode.com Guides},
      year    = {2026},
      month   = may,
      url     = {https://gtcode.com/guides/cns/adversarial-evidence/},
      note    = {Archived at \url{https://github.com/GTCode-Press/publications/tree/main/guides/cns/adversarial-evidence}}
    }

**APA:**
GTCode Editorial (2026, May 15). 15 — Risk Register and Failure Modes. *GTCode.com Guides*. https://gtcode.com/guides/cns/adversarial-evidence/ (Archived at https://github.com/GTCode-Press/publications/tree/main/guides/cns/adversarial-evidence)

**Chicago:**
GTCode Editorial. "15 — Risk Register and Failure Modes." *GTCode.com Guides*, May 15, 2026. https://gtcode.com/guides/cns/adversarial-evidence/. Archived at https://github.com/GTCode-Press/publications/tree/main/guides/cns/adversarial-evidence.
