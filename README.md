# Cassandra

**The Adversarial Review Agent**

Cassandra is part of the [Lorae](https://github.com/joshkenitzer-ops/lorae) tool suite. It red-teams a prompt or a spec across seven fixed failure dimensions and tells you exactly where it breaks.

The myth is exact: Cassandra sees what others miss and warns before it is too late. That is the product.

---

## What Cassandra Does Today

Paste in a prompt or a spec. Cassandra evaluates it across seven dimensions, scores each critical, high, medium, low, or pass, and returns a specific finding with a concrete failure scenario, plus a recommended fix for anything that isn't clean:

- **Logic Gaps**
- **Hallucination Risk**
- **Ambiguity Traps**
- **Scope Creep**
- **Edge Case Blindspots**
- **Instruction Conflicts**
- **Output Format Risk**

Input under 30 words returns `INSUFFICIENT_INPUT` rather than fabricated findings. The result also includes a one-sentence summary and an overall 0-100 score.

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
| **Pass** | No meaningful vulnerability detected in this dimension. |

---

## Pipeline Position

Cassandra is designed as the adversarial quality gate in Lorae's spec-driven development pipeline. The handoff below describes the intended workflow; Cassandra does not yet call Vulcan automatically.

| Stage | Tool | Role |
|---|---|---|
| Commission | User | Provides intent and problem context. |
| Forge | Vulcan | Runs FORGE methodology. Produces the spec artifact. |
| Red-Team | **Cassandra** | Adversarial review. Critical and High findings return to Vulcan before user final approval. |
| Approve | User | Final approval. The spec becomes the source of truth. |

---

## What's Coming

- **Document-type awareness.** Today every input runs through the same seven dimensions regardless of whether it's a prompt, a spec, or something else. Planned: inferring the document's purpose and adopting the review persona it needs.
- **A dedicated spec-failure-mode taxonomy**, drawn from IEEE requirements engineering research, for the cases a generic prompt evaluation misses: Absence, Incompleteness, Contradiction, Premature Definition, Silent Constraint Drop, Scope Drift.
- **File upload** (PDF, docx) and downloadable branded report export.
- The Cassandra spec itself, rebuilt through Vulcan using the FORGE methodology before V2 scope is locked. The rest of this roadmap follows from that.

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
