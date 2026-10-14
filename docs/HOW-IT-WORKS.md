<!-- Generated supporting document. -->

# EvAGI â€” How It Works

[â† Back to README](./README.md)

---

- Routes each input to the expert set that should handle it
- Keeps experts and their parameter pools disjoint, so no weights are shared
- Predicts how much capacity a task needs rather than activating everything
- Learns facts live and re-checks them in a fresh session
- Reports measured accuracy, forgetting and capacity alongside every run

---

## Stage by stage

| # | Stage | What happens |
|---|---|---|
| **1. Input** | A task arrives. |
| **2. Route** | The router selects experts from a live support set. |
| **3. Activate** | Only the selected experts and their pools participate. |
| **4. Execute** | The active subset processes the input. |
| **5. Merge** | Outputs combine into a result. |
| **6. Measure** | Accuracy, forgetting and capacity are recorded. |

---

## Where the boundaries are

Each stage above hands something to the next one. Those hand-offs are the interesting part: they are where correctness is decided, and they are the first place to look when something misbehaves.

What is deliberately not documented: internal data structures, specific algorithms, thresholds, or the contents of any configuration. That is not an oversight â€” publishing them would make the system easier to copy or interfere with.

---

## Verifying behaviour yourself

The only honest way to judge EvAGI is to run it and observe. Claims in this repository are consistent with what the published artefacts show, but the artefacts are captures and schematics, not proofs.

- Maturity: **Experimental**
- Reference: [https://evsphere.vercel.app/research/evagi](https://evsphere.vercel.app/research/evagi)

---

ðŸŒ [Website](https://evsphere.vercel.app) Â· [GitHub](https://github.com/evsphereofficial) Â· [npm](https://www.npmjs.com/~evsphere) Â· [LinkedIn](https://www.linkedin.com/company/evsphere) Â· [X](https://x.com/evsphereco)
