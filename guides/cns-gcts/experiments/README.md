# GCTS Experiments

**Author:** GTCode Editorial
**Published:** May 15, 2026
**Canonical URL:** https://gtcode.com/guides/cns-gcts/experiments/
**Section:** Guides
**License:** [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/)

---

The project must test the theory and expose failure modes. Every GCTS
experiment should have pre-registered hypotheses, baselines, ablations,
held-out data, no runtime oracle, and failure criteria.

## Baseline Families

| Baseline | Purpose |
| --- | --- |
| Direct LLM answer | Measures answer-first behavior |
| RAG plus citations | Measures retrieval-grounded generation without access-state modeling |
| Claim-verification classifier | Measures support/refute/insufficient-evidence behavior |
| Truth-discovery baseline | Measures source-reliability aggregation |
| Simple Bayesian model | Measures probabilistic update without typed access states |
| GCTS without access states | Tests the value of record-access modeling |
| Full GCTS | Target architecture |

## Core Experiments

### EXP-001: Synthetic Latent-Context Resolution

Test whether GCTS recovers hidden modifiers that explain contradictions:
time, subgroup, measurement method, population, jurisdiction, or mechanism.

Success criteria:

- top-3 world coverage at or above 85%;
- latent predicate recovery F1 at or above 0.70;
- calibration ECE at or below 0.10.

### EXP-002: Fact-Verification Grounding Without Runtime Labels

Test claim-status assignment with benchmark labels withheld at runtime. Candidate
data sources include FEVER, SciFact, FEVEROUS, and AVeriTeC.

Baselines:

- RAG plus direct answer;
- RAG plus NLI verifier;
- claim-verification classifier;
- multi-agent debate;
- GCTS without multiverse;
- full GCTS.

Success criteria include zero strict promoted claims with unresolved citations,
improved calibration over baselines, and higher abstention precision.

### EXP-003: Multiverse Calibration

Test whether top-K possible worlds are calibrated and informative.

Metrics:

- top-K world coverage;
- Brier score;
- expected calibration error;
- entropy versus error correlation.

### EXP-004: Oracle-Boundary Ablation

Compare three conditions:

1. No labels.
2. Labels for offline calibration only.
3. Illegal runtime oracle upper bound.

Condition 2 should improve calibration over condition 1. Condition 3 is an
upper bound and must never be treated as deployable.

### EXP-005: Chirality Predictiveness

Test whether chirality predicts synthesis difficulty beyond embedding distance,
claim-graph conflict, and graph cycle count.

Dependent variables:

- convergence iterations;
- contradiction residual after synthesis;
- human uncertainty rating;
- false synthesis rate;
- abstention correctness.

### EXP-006: Adversarial Record Suppression

Test whether GCTS distinguishes absent evidence, evidence of absence,
inaccessible evidence, sealed evidence, likely withheld evidence, destroyed
evidence, and not-generated evidence.

Synthetic planted states include:

- expected record exists and is produced;
- expected record exists but is inaccessible;
- expected record exists but is sealed;
- expected record exists but is withheld;
- expected record was destroyed;
- record was never expected to exist;
- produced record affirmatively refutes the claim.

Success criteria:

- access-state F1 at or above 0.75 on planted cases;
- improved likely-truth Brier/ECE over no-access ablation;
- lower false rejection rate where decisive records are inaccessible;
- lower false promotion rate where evidence of absence is available;
- lower missingness-overreach rate on not-generated records.

## Test Layers

Unit tests cover schema validation, citation resolution, tensor rule firing,
proof trace emission, posterior normalization, entropy/confidence formulas, and
access-state invariants.

Property tests enforce that posterior mass sums to 1, strict promotion requires
proof traces, invalid citations force strict status to `unsupported`, soft rules
cannot promote strict truth, and absence of evidence cannot become evidence of
absence without record-duty and access-path basis.

Integration tests cover ingestion, extraction, grounding, access modeling,
closure, world ranking, and report generation.

Red-team tests include citation hallucination, semantically similar negations,
unsupported paraphrases, misleading lexical overlap, narrow evidence inflated
into broad claims, false suppression inference, selective disclosure, and
strategic partial production.

---

## How to Cite

**BibTeX:**

    @misc{gtcodeeditorial2026experiments_41e9,
      author  = {GTCode Editorial, },
      title   = {GCTS Experiments},
      institution = {GTCode.com Guides},
      year    = {2026},
      month   = may,
      url     = {https://gtcode.com/guides/cns-gcts/experiments/},
      note    = {Archived at \url{https://github.com/GTCode-Press/publications/tree/main/guides/cns-gcts/experiments}}
    }

**APA:**
GTCode Editorial (2026, May 15). GCTS Experiments. *GTCode.com Guides*. https://gtcode.com/guides/cns-gcts/experiments/ (Archived at https://github.com/GTCode-Press/publications/tree/main/guides/cns-gcts/experiments)

**Chicago:**
GTCode Editorial. "GCTS Experiments." *GTCode.com Guides*, May 15, 2026. https://gtcode.com/guides/cns-gcts/experiments/. Archived at https://github.com/GTCode-Press/publications/tree/main/guides/cns-gcts/experiments.
