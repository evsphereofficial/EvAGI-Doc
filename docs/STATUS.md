<!-- Generated supporting document. -->

# EvAGI â€” Status and Limits

[â† Back to README](./README.md)

---

## Current state

| | |
|---|---|
| **Maturity** | **Experimental** |
| **Version** | research prototype |
| **Public page** | [https://evsphere.vercel.app/research/evagi](https://evsphere.vercel.app/research/evagi) |
| **Machine-readable** | [llms.txt](https://evsphere.vercel.app/llms.txt) |

---

## What the maturity label means

| Label | Meaning |
|---|---|
| **Active** | An operating service or activity, running now. |
| **Available** | Usable by someone outside the team, under the stated conditions. |
| **Experimental** | A research prototype. Results are reported, not settled. |
| **In development** | Actively built. Capabilities can change without notice. |
| **Planned** | Intended direction, not implemented. |

EvAGI is currently **Experimental**.

---

## Known limits

- Catastrophic forgetting is NOT solved by this work
- Zero measured forgetting arises because each task gets disjoint parameters â€” interference is removed by construction, not by improving retention
- Both published runs are single runs â€” no seeds, repeats or error bars
- Neither task set is a standard continual-learning benchmark
- Nothing is released publicly, so results cannot be independently reproduced
- The efficiency comparison is against full fine-tuning, the weakest available baseline

---

## What you need to run it

- Python with a GPU or CPU PyTorch environment
- Sufficient disk for model checkpoints and result logs
- Comfort reading experiment reports and evaluation protocols

---

## What is *not* claimed

- No accuracy, reliability or safety guarantee
- No user count, adoption figure or performance benchmark
- No endorsement, certification or independent review
- No timeline and no promise of a future release

EvAGI is not claimed to be finished, production-ready or commercially supported.

---

ðŸŒ [Website](https://evsphere.vercel.app) Â· [GitHub](https://github.com/evsphereofficial) Â· [npm](https://www.npmjs.com/~evsphere) Â· [LinkedIn](https://www.linkedin.com/company/evsphere) Â· [X](https://x.com/evsphereco)
