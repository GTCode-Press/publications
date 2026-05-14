# GCTS Architecture

**Author:** GTCode Editorial
**Published:** May 13, 2026
**Canonical URL:** https://gtcode.com/guides/cns-gcts/architecture/
**Section:** Guides
**License:** [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/)

---

GCTS is an evidence-first pipeline. LLMs may propose extractions or render
reports, but truth ranking is produced by structured evidence, access modeling,
rule closure, and world scoring.

```mermaid
flowchart TD
  A[Raw corpus / documents /<br/>observations] --> B[Evidence Ingestor]
  B --> C[Evidence Atom Store]
  C --> D[Claim Proposer]
  C --> RA[Record Access<br/>Modeler]
  D --> E[Grounding Verifier]
  RA --> IM[Institutional<br/>Incentive Modeler]
  E --> F[Rule Compiler]
  IM --> F
  F --> G[Tensor Logic Closure]
  G --> H[World Builder]
  RA --> H
  IM --> H
  H --> I[Chirality +<br/>Residual Analyzer]
  I --> J[Latent Context +<br/>Access Orthesist]
  J --> H
  H --> K[World Ranker]
  K --> L[Synthesizer /<br/>Renderer]
  L --> M[Audit + Report]
```

## Core Modules

### Evidence Ingestor

Parses the corpus, assigns stable evidence IDs, segments spans, computes source
quality priors, and stores provenance, temporal metadata, and access path.

Output: `EvidenceAtom[]`.

### Record Access Modeler

Identifies records expected by procedure, role, instrumentation, policy, or
ordinary practice. It classifies access states, distinguishes absence of
evidence from evidence of absence, and emits record-contingency notes.

Output: `RecordAccessState[]`.

### Institutional Incentive Modeler

Models actor roles and evidence-control asymmetries. It estimates incentives to
disclose, conceal, delay, narrow, or frame evidence. It adjusts source
reliability and missingness likelihood while leaving claim proof to evidence and
rules.

Output: `InstitutionalIncentiveProfile[]`.

### Claim Proposer

Extracts candidate claims, attaches evidence references, proposes typed
relations, preserves extraction confidence, and marks claims that depend on
unavailable or expected records.

LLMs may be used here, but proposed claims are untrusted until verified.

### Grounding Verifier

Resolves citations, runs claim-evidence entailment, detects invalid references,
rejects unsupported strict promotion, and emits grounding reports.

### Rule Compiler And Tensor Logic Closure

The compiler converts verified claims, relations, and access states into strict
and soft rules. The closure engine computes zero-temperature closure for strict
rules, soft closure for hypotheses, proof traces, and contradiction structure.

### World Builder And Ranker

The world builder enumerates or searches possible worlds with alternative
assumptions, contexts, and missingness hypotheses. The ranker computes:

- world posterior mass;
- claim likely-truth rankings;
- strict support mass;
- confidence;
- uncertainty decomposition.

### Synthesizer / Renderer

The renderer produces top-K worlds and natural-language reports with proof
links, evidence links, access-contingency notes, and calibrated hedging. It must
refuse unsupported strict claims.

## Data Flow

1. Evidence enters as immutable atoms.
2. Expected records and access states are modeled separately from available
   evidence.
3. Claims are proposed and linked to evidence, access states, or record
   contingencies.
4. Verification rejects non-resolving references and low-entailment strict
   links.
5. Rules compile verified claims, relations, and access states into a proof
   substrate.
6. Worlds are generated from alternative assumptions, contexts, and missingness
   hypotheses.
7. Worlds are ranked by evidence support, contradiction energy, parsimony,
   source reliability, and access coherence.
8. The renderer outputs ranked alternatives and collapses to a single answer
   only when uncertainty is low.

## Audit Artifacts

Every run emits an input corpus manifest, evidence atom manifest,
record-access manifest, institutional-incentive manifest, claim extraction
manifest, grounding report, rule compilation manifest, world distribution
report, proof trace file, access-contingency report, rendered synthesis, and
metrics report.

If any strict gate fails, no strict promoted truth claim is produced. The report
uses statuses such as `unsupported`, `record_contingent`, `conflicted`, or
`insufficient evidence` and lists missing records, access constraints, and next
collection actions.

---

## How to Cite

**BibTeX:**

    @misc{gtcodeeditorial2026architecture,
      author  = {GTCode Editorial, },
      title   = {GCTS Architecture},
      institution = {GTCode.com Guides},
      year    = {2026},
      month   = may,
      url     = {https://gtcode.com/guides/cns-gcts/architecture/},
      note    = {Archived at \url{https://github.com/GTCode-Press/publications/tree/main/guides/cns-gcts/architecture}}
    }

**APA:**
GTCode Editorial (2026, May 13). GCTS Architecture. *GTCode.com Guides*. https://gtcode.com/guides/cns-gcts/architecture/ (Archived at https://github.com/GTCode-Press/publications/tree/main/guides/cns-gcts/architecture)

**Chicago:**
GTCode Editorial. "GCTS Architecture." *GTCode.com Guides*, May 13, 2026. https://gtcode.com/guides/cns-gcts/architecture/. Archived at https://github.com/GTCode-Press/publications/tree/main/guides/cns-gcts/architecture.
