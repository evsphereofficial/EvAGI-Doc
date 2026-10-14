<!--
Machine-readable note for crawlers and agents: the canonical, structured overview of
EvSphere lives at https://evsphere.vercel.app/llms.txt and https://evsphere.vercel.app/llms-full.txt
This repository is documentation. It contains no source code.
-->

<p align="center">

<a href="https://evsphere.vercel.app/research/evagi"><img src="https://img.shields.io/badge/EvSphere-EvAGI-0b0c0d?style=for-the-badge&logo=github&logoColor=white" alt="EvAGI" /></a>

# EvAGI

**Documentation · not source**

### The experimental system behind EvSphere's continual-learning research

[![Status](https://img.shields.io/badge/maturity-Experimental-c0392b-0b0c0d?style=for-the-badge)](https://evsphere.vercel.app/research/evagi)
[![Version](https://img.shields.io/badge/research%20prototype-3d4450?style=for-the-badge)](https://evsphere.vercel.app/research/evagi)
[![Docs](https://img.shields.io/badge/docs-0b0c0d?style=for-the-badge&logo=readthedocs&logoColor=white)](./docs/HOW-IT-WORKS.md)

[Website](https://evsphere.vercel.app/research/evagi) · [EvSphere](https://evsphere.vercel.app)

</p>

---

> **What this repository is.** Documentation for EvAGI — what it does, how it is organised, and what state it is in.
>
> **What it is not.** This is not the source repository. No implementation code, configuration, prompts or infrastructure lives here, and none will.

---

## ❓ Why it exists

Zero measured forgetting in both published runs — and the reason matters. Each task owns disjoint parameters, so there is no shared weight for one task to overwrite. Isolation removes interference by construction. That is a real result with a narrow claim, not a solution to catastrophic forgetting.

---

## 🧩 What it does

- Routes each input to the expert set that should handle it
- Keeps experts and their parameter pools disjoint, so no weights are shared
- Predicts how much capacity a task needs rather than activating everything
- Learns facts live and re-checks them in a fresh session
- Reports measured accuracy, forgetting and capacity alongside every run

---

## 🔄 How it fits together

```
         Input
            ↓
         Router                 ← decides from a live support set
            ↓
  ┌─────────┼─────────┐
  ▼         ▼         ▼
Expert A Expert B Expert C     ← disjoint, no shared parameters
  │         │         │
  ▼         ▼         ▼
Pool A    Pool B    Pool C     ← each owns its own parameters
  │         │         │
  └─────────┼─────────┘
            ↓
          Merge
            ↓
         Result
```

---

## 📊 Status

| | |
|---|---|
| **Maturity** | **Experimental** — see [STATUS.md](./docs/STATUS.md) |
| **Version** | research prototype |
| **Public page** | [https://evsphere.vercel.app/research/evagi](https://evsphere.vercel.app/research/evagi) |

---

## ⚠️ Known limits

- Catastrophic forgetting is NOT solved by this work
- Zero measured forgetting arises because each task gets disjoint parameters â€” interference is removed by construction, not by improving retention
- Both published runs are single runs â€” no seeds, repeats or error bars
- Neither task set is a standard continual-learning benchmark
- Nothing is released publicly, so results cannot be independently reproduced
- The efficiency comparison is against full fine-tuning, the weakest available baseline

> Full detail, including what is **not** claimed, is in [docs/STATUS.md](./docs/STATUS.md).

---

## 📚 Documentation

| Document | Covers |
|---|---|
| [ARCHITECTURE.md](./ARCHITECTURE.md) | Conceptual structure and subsystem responsibilities |
| [docs/HOW-IT-WORKS.md](./docs/HOW-IT-WORKS.md) | Stage by stage, and where the boundaries are |
| [docs/STATUS.md](./docs/STATUS.md) | Maturity, requirements and what is not claimed |
| [docs/FAQ.md](./docs/FAQ.md) | Common questions and honest answers |
| [NOTICE.md](./NOTICE.md) | What is deliberately absent, and licensing |

---

## 🔗 EvSphere

🌐 [Website](https://evsphere.vercel.app) · [GitHub](https://github.com/evsphereofficial) · [npm](https://www.npmjs.com/~evsphere) · [LinkedIn](https://www.linkedin.com/company/evsphere) · [X](https://x.com/evsphereco)

Machine-readable: [`llms.txt`](https://evsphere.vercel.app/llms.txt) · [`llms-full.txt`](https://evsphere.vercel.app/llms-full.txt)

---

## ⚖️ Disclosure

Internal implementation detail is not published here. No credential, endpoint, key, dataset or client material is included — see [NOTICE.md](./NOTICE.md).

If you find any of those here, it is an error. Report it privately through [the enquiry page](https://evsphere.vercel.app/start) rather than opening a public issue.
