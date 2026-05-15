# 23 — Data and Run Manifest Specification

**Author:** GTCode Editorial
**Published:** May 15, 2026
**Canonical URL:** https://gtcode.com/guides/cns/data-and-run-manifest/
**Section:** Guides
**License:** [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/)

---

# 23 — Data and Run Manifest Specification

## Why manifests matter

CNS 8.0 experiment records track oracle separation and reproducibility.

## Dataset manifest

```json
{
  "dataset_id": "scifact_dev_v1",
  "source": "local_or_remote",
  "split": "dev",
  "hash": "...",
  "label_fields_available_offline": ["label", "rationale"],
  "label_fields_available_runtime": [],
  "created_at": "2026-05-15"
}
```

## Run manifest

```json
{
  "run_id": "cns8_run_001",
  "config_hash": "...",
  "dataset_manifest": "dataset_manifest.json",
  "oracle_policy": {
    "training_oracles": true,
    "runtime_oracles": false,
    "leakage_scan": "passed"
  },
  "models": {
    "proposer": "...",
    "entailment": "...",
    "synthesizer": "..."
  },
  "rule_bank_version": "rules_v0",
  "schemas": {
    "sno": "sno8.schema.json",
    "proof": "proof_trace.schema.json"
  },
  "metrics": {},
  "artifacts": {}
}
```

## Artifact map

```text
runs/{run_id}/
  evidence_atoms.jsonl
  proposed_snos.jsonl
  critic_reports.jsonl
  selected_pairs.jsonl
  proof_closure.jsonl
  residual_tensors/
  latent_predicates.jsonl
  synthesized_snos.jsonl
  orthesis_reports.jsonl
  final_report.md
  run_manifest.json
```

## Required hashes

- evidence atom hashes;
- prompt template hashes;
- config hash;
- rule bank hash;
- schema hash;
- dataset split hash;
- proof trace checksum.

## Oracle leakage fields

Runtime input schemas exclude:

- label;
- gold rationale;
- correct answer;
- hidden context;
- generator seed;
- ground-truth world ID.

---

## How to Cite

**BibTeX:**

    @misc{gtcodeeditorial2026datarunmanifest,
      author  = {GTCode Editorial, },
      title   = {23 — Data and Run Manifest Specification},
      institution = {GTCode.com Guides},
      year    = {2026},
      month   = may,
      url     = {https://gtcode.com/guides/cns/data-and-run-manifest/},
      note    = {Archived at \url{https://github.com/GTCode-Press/publications/tree/main/guides/cns/data-and-run-manifest}}
    }

**APA:**
GTCode Editorial (2026, May 15). 23 — Data and Run Manifest Specification. *GTCode.com Guides*. https://gtcode.com/guides/cns/data-and-run-manifest/ (Archived at https://github.com/GTCode-Press/publications/tree/main/guides/cns/data-and-run-manifest)

**Chicago:**
GTCode Editorial. "23 — Data and Run Manifest Specification." *GTCode.com Guides*, May 15, 2026. https://gtcode.com/guides/cns/data-and-run-manifest/. Archived at https://github.com/GTCode-Press/publications/tree/main/guides/cns/data-and-run-manifest.
