# GCTS Theory

**Author:** GTCode Editorial
**Published:** May 15, 2026
**Canonical URL:** https://gtcode.com/guides/cns-gcts/theory/
**Section:** Guides
**License:** [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/)

---

GCTS separates three questions that are often collapsed:

1. What is strictly proven?
2. What is likely true across admissible worlds?
3. What uncertainty remains because of evidence quality, missing records,
   access conditions, source incentives, or contradiction structure?

The system emits three distinct quantities:

| Quantity | Meaning |
| --- | --- |
| `P(c | E,A,I)` | likely-truth posterior mass across structured worlds |
| `P0(c | E)` | strict proof support from resolvable evidence and proof traces |
| `Conf(c)` | confidence after uncertainty decomposition |

A claim can be probable while still record-contingent. A claim can be strictly
proven inside a narrow reference set while its broader interpretation remains
low-confidence. A claim can be plausible yet unsuitable for promotion because
access-state uncertainty remains material.

## Evidence Atoms

An evidence atom is:

$$
e_i = (u_i, s_i, t_i, q_i, a_i, m_i)
$$

where `u_i` is a stable source identifier, `s_i` is a span, observation,
record, or structured datum, `t_i` is temporal scope, `q_i` is source/evidence
quality, `a_i` is access path, and `m_i` is metadata.

The available evidence set is:

$$
E = \{e_1,\dots,e_n\}
$$

Evidence atoms are immutable within a run. Later corrections or productions
create new atoms and preserve the earlier state as part of the audit trail.

## Record-Access States

GCTS models missing evidence as structured information. A record-access state is:

$$
r_k = (id_k, type_k, owner_k, controller_k, duty_k, expected_k, access_k,
production_k, request_k, time_k, q_k)
$$

The `access_k` value may be `available`, `inaccessible`, `sealed`, `withheld`,
`destroyed`, `not_generated`, `unknown`, `produced_late`, `partial`,
`contradicted`, or `unavailable_at_time_t`.

This lets the system distinguish:

- absence of evidence;
- evidence of absence;
- inaccessible evidence;
- sealed evidence;
- withheld evidence;
- destroyed evidence;
- not-generated evidence;
- partial or nonresponsive production;
- evidence unavailable at the relevant decision time.

Absence can affect ranking only when record-generation duty, expected
observability, ownership/control, collection path, production state, and access
state justify that effect.

## Claims And Statuses

A claim is:

$$
c_j = (p_j, frame_j, refs_j, contingencies_j, \sigma_j)
$$

where `p_j` is a proposition, `frame_j` is an argument frame, `refs_j` is an
evidence-reference set, `contingencies_j` is a record-contingency set, and
`\sigma_j` is one of `proven`, `probable`, `plausible`, `record_contingent`,
`conflicted`, `unsupported`, `rejected`, or `insufficient_evidence`.

Relations among claims are typed through a relation set `R`, including
`supports`, `refutes`, `implies`, `specializes`, `generalizes`, `qualifies`,
`depends_on`, `undercuts`, and `independent`.

## Language, Logic, And Access

Let `L` be the language/concept manifold, `T` the logic/proof space, and `A`
the access/missingness space. A grounding map extracts proof and access
structure:

$$
G: L \rightarrow \mathcal{T} \times \mathcal{A}
$$

A rendering map turns structured worlds back into language:

$$
S: \mathcal{T} \times \mathcal{A} \rightarrow L
$$

The orthesis is the stable structured state:

$$
(\mathcal{T}^{\ast},\mathcal{A}^{\ast}) =
G(S(\mathcal{T}^{\ast},\mathcal{A}^{\ast}))
$$

The orthesis is the structured state that survives language rendering without
losing proof support, likely-truth support, access-state coherence, or
uncertainty.

## Chirality Residuals

Round-trip chirality measures whether a structured state survives rendering and
re-grounding:

$$
\delta(X) = d_{\mathcal{T},\mathcal{A}}(X, G(S(X)))
$$

A fluent narrative can have high chirality if its logical or access structure
falls apart under grounding. In GCTS, chirality is a diagnostic residual:

- graph chirality, based on edge-incidence differences between claim graphs;
- residual tensor chirality, based on unresolved support/refutation mass;
- access chirality, when structured modeling breaks narrative access
  assumptions;
- rendering chirality, when generated language drops proof or access
  contingencies.

Chirality does not prove falsity. It identifies mismatch that must be resolved
by evidence, rules, access modeling, or explicit uncertainty.

## Possible Worlds

A world view is:

$$
W_k = (F_k, R_k, Z_k, \Pi_k, A_k, M_k, H_k)
$$

where `F_k` contains accepted facts and likely-truth claims, `R_k` is a rule
subset, `Z_k` are latent context predicates, `\Pi_k` are proof traces, `A_k`
are assumptions, `M_k` is a record-access model, and `H_k` is an
institutional-incentive hypothesis set.

Worlds are scored by energy:

$$
\mathcal{E}(W_k;E,A,I) =
\alpha C(W_k) + \beta X(W_k) + \gamma G_w(W_k) + \delta K(W_k)
+ \eta S_r(W_k) - \lambda S_e(W_k)
$$

where `C` is contradiction, `X` is access mismatch, `G_w` is weak grounding,
`K` is unsupported complexity, `S_r` is source risk, and `S_e` is evidence
support.

World posterior mass is:

$$
Q(W_k \mid E,A,I) =
\frac{\exp(-\mathcal{E}(W_k;E,A,I))}
{\sum_\ell \exp(-\mathcal{E}(W_\ell;E,A,I))}
$$

Lower energy worlds are better supported. Contradictions, unsupported
complexity, access mismatch, weak grounding, and source risk raise energy;
evidence support lowers it.

## Likely-Truth Ranking

For a claim `c`:

$$
P(c \mid E,A,I)=
\sum_k Q(W_k\mid E,A,I)\,\mathbf{1}[c \in Cl(W_k)]
$$

The score reports posterior mass across structured worlds. LLM confidence has
no role in the runtime truth value.

Strict proof support is emitted separately:

$$
P_0(c \mid E)=
\sum_k Q(W_k\mid E,A,I)\,\mathbf{1}[c \in Cl_0(W_k)]
$$

Confidence is a function of grounding quality, world entropy, access-state
uncertainty, source risk, and residual conflict:

$$
Conf(c) = f(q_g(c), H(W), u_A(c), r_s(c), \delta(c))
$$

The system must emit `P(c | E,A,I)`, `P0(c | E)`, and `Conf(c)` separately.

---

## How to Cite

**BibTeX:**

    @misc{gtcodeeditorial2026theory_42e5,
      author  = {GTCode Editorial, },
      title   = {GCTS Theory},
      institution = {GTCode.com Guides},
      year    = {2026},
      month   = may,
      url     = {https://gtcode.com/guides/cns-gcts/theory/},
      note    = {Archived at \url{https://github.com/GTCode-Press/publications/tree/main/guides/cns-gcts/theory}}
    }

**APA:**
GTCode Editorial (2026, May 15). GCTS Theory. *GTCode.com Guides*. https://gtcode.com/guides/cns-gcts/theory/ (Archived at https://github.com/GTCode-Press/publications/tree/main/guides/cns-gcts/theory)

**Chicago:**
GTCode Editorial. "GCTS Theory." *GTCode.com Guides*, May 15, 2026. https://gtcode.com/guides/cns-gcts/theory/. Archived at https://github.com/GTCode-Press/publications/tree/main/guides/cns-gcts/theory.
