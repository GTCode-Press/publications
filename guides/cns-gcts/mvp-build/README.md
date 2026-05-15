# GCTS MVP Build

**Author:** GTCode Editorial
**Published:** May 15, 2026
**Canonical URL:** https://gtcode.com/guides/cns-gcts/mvp-build/
**Section:** Guides
**License:** [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/)

---

The GCTS MVP can be built without full custom model training. The first target
is an auditable decision-support prototype that accepts a bounded corpus,
extracts evidence and claims, models access states, enumerates worlds, and emits
ranked reports.

## Product Boundary

The MVP should be an **Evidence Accountability Workbench** focused on auditable
evidence operations. The first useful product should help analysts organize
evidence, identify record contingencies, preserve contradiction, and report what
records would change the analysis.

Initial users:

- investigative researchers;
- legal support teams;
- compliance analysts;
- journalists handling incomplete records;
- internal auditors;
- intelligence-style analytic teams.

## Phase 1: Local Prototype

Use existing models and explicit schemas:

- LLMs for candidate extraction, latent-context suggestions, access-hypothesis
  suggestions, and rendering.
- Retrieval plus citation validation for evidence grounding.
- NLI or entailment models for claim-evidence scoring.
- A small evidence-access model for expected record existence, availability,
  control, and non-production.
- A rule compiler for a monotone tensor-logic core.
- Candidate-world enumeration or beam search.
- Calibration data to map evidence, access, incentive, and contradiction
  signals to probabilities.
- A dashboard to expose world rankings, proof traces, record-access states,
  uncertainty, and next evidence.

Fine-tuning is optional in Phase 1. If used, it should target extraction,
evidence linking, access-state classification, and calibration. Direct runtime
truth judgment stays outside model generation.

## Runtime Data Products

The MVP should persist:

- evidence atoms;
- record-access states;
- institutional incentive profiles;
- claims and relations;
- rules and proof traces;
- world views;
- posterior and confidence reports;
- rendered synthesis reports.

## API Surface

The first API should expose:

- `POST /runs` to create a synthesis run from a corpus manifest;
- `GET /runs/{id}` for run status;
- `GET /runs/{id}/evidence` for evidence atoms;
- `GET /runs/{id}/access` for record-access states;
- `GET /runs/{id}/worlds` for top-K possible worlds;
- `GET /runs/{id}/claims` for claim rankings and statuses;
- `GET /runs/{id}/report` for the rendered report.

## MVP Gates

The first build succeeds only if it reaches:

- 100% resolvable citations for promoted strict claims;
- zero promoted zero-temperature claims without proof traces;
- calibrated claim probabilities with ECE at or below 0.10 on held-out
  verification tasks;
- top-3 world coverage at or above 85% on synthetic latent-context tasks;
- measurable chirality correlation with synthesis difficulty;
- measurable access-state calibration on adversarial record-suppression tasks;
- explicit distinction between `unsupported`, `record_contingent`,
  `conflicted`, and `rejected`;
- ablation evidence that multiverse/proof/access scoring beats simple RAG and
  LLM debate baselines on grounding, uncertainty quality, and likely-truth
  ranking.

## First Repository Shape

```text
gcts-prototype/
  gcts/
    schemas.py
    access_states.py
    rules.py
    worlds.py
    scoring.py
    statuses.py
    audit.py
  examples/
    facility_incident/
      evidence.json
      records.json
      claims.json
  outputs/
  README.md
```

## First Demonstration

The first demo should show the same evidence under different access states:

1. Available record.
2. Inaccessible record.
3. Withheld record.
4. Not-generated record.
5. Evidence of absence.

The expected result is a visible status difference across runs, with strict
proof, likely-truth posterior, and confidence reported separately.

---

## How to Cite

**BibTeX:**

    @misc{gtcodeeditorial2026mvpbuild_d905,
      author  = {GTCode Editorial, },
      title   = {GCTS MVP Build},
      institution = {GTCode.com Guides},
      year    = {2026},
      month   = may,
      url     = {https://gtcode.com/guides/cns-gcts/mvp-build/},
      note    = {Archived at \url{https://github.com/GTCode-Press/publications/tree/main/guides/cns-gcts/mvp-build}}
    }

**APA:**
GTCode Editorial (2026, May 15). GCTS MVP Build. *GTCode.com Guides*. https://gtcode.com/guides/cns-gcts/mvp-build/ (Archived at https://github.com/GTCode-Press/publications/tree/main/guides/cns-gcts/mvp-build)

**Chicago:**
GTCode Editorial. "GCTS MVP Build." *GTCode.com Guides*, May 15, 2026. https://gtcode.com/guides/cns-gcts/mvp-build/. Archived at https://github.com/GTCode-Press/publications/tree/main/guides/cns-gcts/mvp-build.
