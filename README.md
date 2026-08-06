[README.md](https://github.com/user-attachments/files/29409424/README.md)
# Cassandra

**The Adversarial Review Agent**

Cassandra is part of the [Lorae](https://github.com/joshkenitzer-ops/lorae) tool suite. Cassandra reads any document, infers its intent, and adopts the critical persona the document needs to hear. The warnings are the point.

The myth is exact: Cassandra sees what others miss and warns before it is too late. That is the product.

---

## What Cassandra Does Today

The live app accepts any text input: a prompt, a spec, a cover letter, a product brief. Cassandra infers the document's purpose, adopts the adversarial persona it needs, and returns a structured review with findings categorized by severity.

The review is not gentle. It is honest, specific, and direct.

**Live at:** [cassandra-app-theta.vercel.app](https://cassandra-app-theta.vercel.app)

---

## Severity Levels

| Severity | Definition |
|---|---|
| **Critical** | Fundamental flaw. Must be resolved before the document is used. |
| **High** | Significant weakness. Likely to reduce effectiveness or credibility. |
| **Medium** | Improvement opportunity. Does not block use but reduces quality. |
| **Low** | Minor observation. Polish and edge case handling. |

---

## Spec Failure Mode Checks

When reviewing a spec, Cassandra checks against six known failure modes drawn from IEEE requirements engineering research:

- **Absence:** A required behavior is not specified at all.
- **Incompleteness:** A requirement exists but only partially specifies the behavior. Edge cases, error states, or boundary conditions are missing.
- **Contradiction:** Two or more requirements conflict. Both cannot be true simultaneously.
- **Premature Definition:** A need is specified before the problem is bounded.
- **Silent Constraint Drop:** A constraint exists in the problem context but does not appear in the requirements.
- **Scope Drift:** Requirements reference behavior outside the defined version scope.

---

## Pipeline Position

Cassandra is the adversarial quality gate in Lorae's spec-driven development pipeline.

| Stage | Tool | Role |
|---|---|---|
| Commission | User | Provides intent and problem context. |
| Forge | Vulcan | Runs FORGE methodology. Produces the spec artifact. |
| Red-Team | **Cassandra** | Adversarial review. Critical and High findings return to Vulcan before user final approval. |
| Approve | User | Final approval. The spec becomes the source of truth. |

---

## What's Coming

File upload (PDF, docx) and downloadable branded report export are the next planned additions. The Cassandra spec will be rebuilt through Vulcan using the FORGE methodology before V2 scope is locked. The roadmap follows from that.

---

## Part of the Lorae Suite

| Tool | Role |
|---|---|
| Cassandra | Adversarial review agent |
| Vulcan | Spec forge (FORGE methodology) |
| Janus | Session handoff and context persistence |
| Ma'at | Automated quality review |
| Chiron | Upskilling and tutoring agent |

---

*Ancient patterns. Modern intelligence.*
