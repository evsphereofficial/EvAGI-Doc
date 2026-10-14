<!-- Generated supporting document. -->

# EvAGI â€” Conceptual Architecture

<p align="center"><a href="https://evsphere.vercel.app/research/evagi"><img src="https://img.shields.io/badge/EvSphere-EvAGI-0b0c0d?style=for-the-badge&logo=github&logoColor=white" alt="EvAGI" /></a></p>

> **Scope note.** This describes what each subsystem is *for* and how responsibility is divided. It is not an implementation specification, and internal design detail is deliberately not published. Nothing here is sufficient to reconstruct the system.

---

## One-line model

An experimental architecture where learned domains are held in disjoint parameters and a live router decides which participate in a given task.

---

## Subsystems

| Subsystem | Responsibility |
|---|---|
| **Router** | Decides which experts participate, from a support set rather than a task label. |
| **Experts** | A row of disjoint specialist blocks, separated so their parameters never overlap. |
| **Parameter Pools** | Each expert owns its own pool. This is what makes isolation structural. |
| **Register** | Predicts required active capacity for a task. |
| **Capacity Law** | A measured relationship between active parameters and accuracy. |
| **Merge** | Collects expert outputs into a single result. |

---

## Design principles

1. **Explicit boundaries.** Each subsystem has one job. Overlap between them is a defect, not a convenience.
2. **Composition over configuration.** Capabilities are assembled at runtime rather than hard-wired at build time.
3. **Observability before optimisation.** A subsystem that cannot be inspected cannot be trusted or improved.
4. **Local first.** Execution and data stay under the operator's control wherever that is possible.
5. **Honest failure.** If something does not work, it says so rather than degrading silently.

---

## What is deliberately not here

- Source code, prompts, configuration or infrastructure
- Endpoint, credential, key or connection detail of any kind
- Dataset contents or identifiers
- Anything about a specific client or engagement
- Internal design rationale that would assist copying or attack

If you need any of the above, [ask directly](https://evsphere.vercel.app/start).

---

## Further reading

| | |
|---|---|
| [README](./README.md) | Overview |
| [docs/HOW-IT-WORKS.md](./docs/HOW-IT-WORKS.md) | Stage by stage |
| [docs/STATUS.md](./docs/STATUS.md) | Maturity and limits |
| [docs/FAQ.md](./docs/FAQ.md) | Questions and honest answers |

---

ðŸŒ [Website](https://evsphere.vercel.app) Â· [GitHub](https://github.com/evsphereofficial) Â· [npm](https://www.npmjs.com/~evsphere) Â· [LinkedIn](https://www.linkedin.com/company/evsphere) Â· [X](https://x.com/evsphereco)
