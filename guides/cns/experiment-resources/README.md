# Experiment Resource Files

**Author:** GTCode Editorial
**Published:** May 15, 2026
**Canonical URL:** https://gtcode.com/guides/cns/experiment-resources/
**Section:** Guides
**License:** [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/)

---

# Experiment Resource Files

## experiments/experiment_matrix.yaml

````yaml
experiments:
  - id: E1_latent_context_recovery
    goal: recover hidden context predicates from synthetic contradictions
    datasets: [synthetic_latent_context]
    baselines: [rag_summary, llm_debate, possible_world_only, cns_no_predicate_invention]
    metrics: [latent_f1, residual_energy_reduction, piu, false_predicate_rate]

  - id: E2_productive_conflict_selection
    goal: test chirality + entanglement pair selector
    datasets: [synthetic_sno_pairs, argument_pairs]
    baselines: [embedding_distance, contradiction_only, evidence_overlap_only]
    metrics: [precision_at_10, synthesis_yield, critic_failure_rate]

  - id: E3_grounded_fact_verification
    goal: validate extraction/grounding on known datasets
    datasets: [scifact, fever]
    baselines: [rag, claim_verifier, llm_extractor]
    metrics: [citation_validity, entailment, rationale_recovery, zthr]

  - id: E4_orthesis_roundtrip
    goal: test render/reground stability
    datasets: [synthetic_sno_pairs, scifact_synthesis_subset]
    baselines: [ordinary_summary, debate_summary, cns_no_orthesis]
    metrics: [roundtrip_residual, proof_atom_preservation, claim_drift]

  - id: E5_topology_difficulty
    goal: test whether topology and chirality predict synthesis difficulty
    datasets: [synthetic_topology, argument_pairs]
    baselines: [embedding_distance, beta1_only, contradiction_count]
    metrics: [difficulty_auc, beta1_reduction, residual_energy, iterations_to_converge]
````

## experiments/ablation_suite.yaml

````yaml
ablations:
  - remove: antagonist
    expected_failure: fewer detected contradictions, higher unsupported synthesis
  - remove: evidential_entanglement
    expected_failure: selects unrelated disagreements
  - remove: graph_chirality
    expected_failure: misses structural opposition
  - remove: language_logic_roundtrip
    expected_failure: fluent but unstable renderings
  - remove: tensor_proof_closure
    expected_failure: strict claims without machine-checkable proof
  - remove: predicate_invention
    expected_failure: persistent contradictions remain unresolved
  - remove: access_states
    expected_failure: missing records misinterpreted as evidence
  - remove: possible_worlds
    expected_failure: weaker uncertainty reporting
  - remove: orthesis_loop
    expected_failure: synthesized SNO drifts after re-grounding
````

---

## How to Cite

**BibTeX:**

    @misc{gtcodeeditorial2026experimentresources,
      author  = {GTCode Editorial, },
      title   = {Experiment Resource Files},
      institution = {GTCode.com Guides},
      year    = {2026},
      month   = may,
      url     = {https://gtcode.com/guides/cns/experiment-resources/},
      note    = {Archived at \url{https://github.com/GTCode-Press/publications/tree/main/guides/cns/experiment-resources}}
    }

**APA:**
GTCode Editorial (2026, May 15). Experiment Resource Files. *GTCode.com Guides*. https://gtcode.com/guides/cns/experiment-resources/ (Archived at https://github.com/GTCode-Press/publications/tree/main/guides/cns/experiment-resources)

**Chicago:**
GTCode Editorial. "Experiment Resource Files." *GTCode.com Guides*, May 15, 2026. https://gtcode.com/guides/cns/experiment-resources/. Archived at https://github.com/GTCode-Press/publications/tree/main/guides/cns/experiment-resources.
