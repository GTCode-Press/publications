# GCTS Record-Access Ontology

**Author:** GTCode Editorial
**Published:** May 15, 2026
**Canonical URL:** https://gtcode.com/guides/cns-gcts/record-access-ontology/
**Section:** Guides
**License:** [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/)

---

The record-access layer is the strongest differentiating component of GCTS.
Standard verification systems often classify a claim against retrieved evidence.
GCTS also models the records that should exist, might exist, were requested,
were not produced, were produced late, were sealed, were destroyed, or should
never have been expected.

## Record-Access State Object

A record-access state is:

$$
r_k = (id_k, type_k, owner_k, controller_k, duty_k, expected_k, access_k,
production_k, request_k, time_k, q_k)
$$

| Field | Meaning |
| --- | --- |
| `id_k` | Stable record-access identifier |
| `type_k` | Record type, such as report, log, transcript, notification, policy record, metadata, or audit entry |
| `owner_k` | Institution or actor expected to own or retain the record |
| `controller_k` | Actor with practical control over access or production |
| `duty_k` | Legal, policy, role, instrumentation, or ordinary-practice generation duty |
| `expected_k` | Expected observability or generation likelihood |
| `access_k` | Access-state classification |
| `production_k` | Production history or response state |
| `request_k` | Request path, search path, or collection path |
| `time_k` | Time interval in which the record would matter |
| `q_k` | Confidence in the classification |

## Access States

| State | Definition | Ranking effect |
| --- | --- | --- |
| `available` | Record is present and resolvable | Can support, refute, or qualify claims directly |
| `inaccessible` | Record may exist outside the current access path | Creates record contingency and wider uncertainty |
| `sealed` | Record exists or plausibly exists under restricted access | Blocks strict conclusions dependent on the record |
| `withheld` | Non-production is plausibly controlled by an actor with access and incentive | Creates competing missingness worlds and may affect world energy |
| `destroyed` | Record existed or was expected and is no longer available | Creates retention or spoliation hypotheses when duty and control are established |
| `not_generated` | Record should not be expected under the relevant duty or practice | Reduces absence penalty and can refute assumptions about expected records |
| `unknown` | Current evidence cannot classify the access state | Widens uncertainty and prevents strong absence inference |
| `produced_late` | Record appeared after initial non-production | Supports timelines about production behavior and access friction |
| `partial` | Some responsive material exists but expected fields or documents are missing | Creates partial support and unresolved contingencies |
| `contradicted` | Produced record conflicts with other evidence or expected metadata | Increases contradiction residual and alternative-world branching |
| `unavailable_at_time_t` | Record exists now or later but was unavailable at the relevant decision time | Prevents later evidence from being treated as runtime evidence for the original actor |

## Production States

| State | Definition |
| --- | --- |
| `produced` | Responsive record produced |
| `partial_production` | Some responsive material produced |
| `no_response` | No institutional response to request |
| `nonresponsive_response` | Response received but did not answer the record question |
| `refused` | Production denied or refused |
| `claimed_none` | Institution states no responsive record exists |
| `lost` | Record claimed lost |
| `destroyed` | Record claimed destroyed |
| `late_production` | Record produced after delay |
| `metadata_only` | Metadata or administrative material produced without the responsive record |

## Generation Duty

A record expectation is stronger when several duty signals align:

| Duty source | Examples |
| --- | --- |
| Legal duty | reporting law, retention law, mandatory reporting, discovery obligation |
| Policy duty | school policy, HR policy, medical protocol, agency rule |
| Role duty | officer, supervisor, teacher, clinician, custodian, compliance officer |
| Instrumentation duty | logs, cameras, timestamps, access-control systems |
| Ordinary-practice duty | records typically created in comparable cases |
| No duty | record should not be expected |

## Absence Discipline

Absence can affect a claim only after the system has modeled:

1. Whether a record-generation duty existed.
2. Whether the event should have been observable.
3. Who owned or controlled the record.
4. Whether the access path was legitimate or ordinary.
5. What production response occurred.
6. Whether the record's absence is better explained by benign missingness,
   access limits, non-generation, destruction, sealing, withholding, or unknown
   causes.

Only evidence of absence directly penalizes a claim as absent. Other states
usually create uncertainty, record contingency, or competing worlds.

## Output Requirement

Every record-contingent claim should state:

- which records matter;
- why those records were expected or not expected;
- who owned or controlled them;
- what access state is currently assigned;
- how confident the system is in that classification;
- whether strict proof depends on the record;
- whether likely-truth ranking depends on the record;
- what record production would raise, lower, or resolve the claim status.

---

## How to Cite

**BibTeX:**

    @misc{gtcodeeditorial2026recordaccessontology_3a16,
      author  = {GTCode Editorial, },
      title   = {GCTS Record-Access Ontology},
      institution = {GTCode.com Guides},
      year    = {2026},
      month   = may,
      url     = {https://gtcode.com/guides/cns-gcts/record-access-ontology/},
      note    = {Archived at \url{https://github.com/GTCode-Press/publications/tree/main/guides/cns-gcts/record-access-ontology}}
    }

**APA:**
GTCode Editorial (2026, May 15). GCTS Record-Access Ontology. *GTCode.com Guides*. https://gtcode.com/guides/cns-gcts/record-access-ontology/ (Archived at https://github.com/GTCode-Press/publications/tree/main/guides/cns-gcts/record-access-ontology)

**Chicago:**
GTCode Editorial. "GCTS Record-Access Ontology." *GTCode.com Guides*, May 15, 2026. https://gtcode.com/guides/cns-gcts/record-access-ontology/. Archived at https://github.com/GTCode-Press/publications/tree/main/guides/cns-gcts/record-access-ontology.
