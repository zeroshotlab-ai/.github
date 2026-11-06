
<img src="./hero.png" alt="ZeroShotLab" width="100%" />

<br/>

<p><strong>EDGE AI RESEARCH LAB · INDIA</strong></p>

# ZeroShotLab

**On-device AI agents for phones** — local computer, efficient micro-models, privacy by default.

We build the stack where the model, tools, and memory stay on the device. First product ship is **L2 Hinglish micro-models**; the parallel track is a **phone-native agent harness** (file/shell sandbox + E2E messaging later). We do **not** start with a giant model zoo.

Website: [zeroshotlab.in](https://zeroshotlab.in) · GitHub: [zeroshotlab-ai](https://github.com/zeroshotlab-ai)

---

## Mission

Make capable AI agents practical on real ₹8–15k Androids: low latency, offline-friendly, and under the user’s control — not locked behind cloud APIs.

---

## Product stack

| Track | What | Target ship | Status |
| --- | --- | --- | --- |
| **L2 — Micro-models** | Hinglish **LID · transliteration · normaliser · PII** (20–100M, ONNX int8) — also harness pre/post tools | **Now → Jan 2027** | **START HERE** |
| **Agent runtime** | On-device harness + local file/shell (“own computer”) + OTS GGUF/LiteRT bases | Phase 0 Nov 2026 → Kotlin MVP Jan–Feb 2027 | Parallel with L2 |
| **L3 — Instruct** | Hinglish instruct 1–4B (LoRA/QLoRA ± DPO), quantised — only if L2 eval proves the gap | **Feb 2027** (or when needed) | After L2 |
| **L4 — TTS** | Hindi/Hinglish on-device TTS | Mar 2027 (conditional) | **Cut first if late** |
| **L5 — SDK** | Edge SDK + Android sample (agent + L2 tools ± L3) | **Apr 2027** | Alpha |
| **L1 — Zoo** | Indic edge model zoo + device benchmarks | Optional later | **Deferred** — not a gate |

---

## Public roadmap (Nov 2026 → Apr 2027)

### Now → mid-Jan 2027 — **L2 alpha**
- Freeze scope: 4 micros × ONNX int8
- Datasets + licences + **rule baselines** to beat
- ONNX int8 export + phone RTF measurements on budget Androids
- Train/distill micros; kill any run that does not beat rule baseline
- **Ship gate:** ≥2 of 4 models on this Hub + short write-up + Android/ONNX sample

### Parallel — **Agent Phase 0 → MVP**
- Study harness patterns (AndroidHarness / AndroPI / Mochu — study only, no clone)
- Termux + off-the-shelf GGUF smoke on a real phone
- Native Kotlin harness MVP (**Jan–Feb 2027**) feeding L5

### Feb 2027 — **L3** (if needed)
- Tool-aware Hinglish instruct on OTS Gemma/Qwen-class bases
- Must beat base on held-out eval and run on a budget phone

### Mar 2027 — **L4** (conditional)
- Only with consented data + native-listener MOS
- If late: **drop / slip** — do not block L2/L3/L5

### Apr 2027 — **L5 SDK + agent sample**
- Python + Android sample: L2 tools + OTS runtime ± L3
- Public **HinglishEdge-Eval**-style table

---

## L2 detail — what ships first

| Micro-model | Job |
| --- | --- |
| **LID** | Language / script / Hinglish-mix detect |
| **Transliteration** | Roman ↔ Devanagari (scoped) |
| **Normaliser** | Clean noisy Hinglish for downstream |
| **PII** | Redact/flag phone, email, etc. before tools/logs |

**Hard rules:** no train-from-scratch · no L1 zoo as a blocker · every release needs a public eval · prefer Apache/MIT bases · Modal free / Kaggle first (budget alert at $30).

---

## Week-by-week (L2 critical path)

| When | Milestone |
| --- | --- |
| 6–12 Nov 2026 | Scope freeze · orgs · LICENSES · Modal alert |
| 6–14 Nov | Dataset + licence shortlist · rule baselines |
| 9–20 Nov | ONNX int8 pipeline · phone RTF script |
| 16–29 Nov | First 2 micros trained vs baseline |
| 16 Nov–20 Dec | Eval set v0 (reviewed Hinglish) |
| 30 Nov–20 Dec | Remaining micros · HF packages · harness hooks |
| **by mid-Jan 2027** | **L2 alpha publish** (≥2/4) |

---

## Why investors / partners should care

1. **Clear wedge:** phone-native agents + India-first Hinglish tooling — not another hosted chatbot.
2. **Lean path:** L2 GPU budget on the order of tens of dollars; phones ₹20–40k test fleet; revenue from **paid edge pilots**, not a race-to-bottom API.
3. **Honest gates:** ship only what beats baselines; L4 and L1 zoo are explicitly cuttable.
4. **Apr 2027 north star:** public models + agent sample + eval table + pilot/LOI conversations from results.

---

## Links

- Website: [zeroshotlab.in](https://zeroshotlab.in)
- GitHub org: [github.com/zeroshotlab-ai](https://github.com/zeroshotlab-ai)
- Hub org: [huggingface.co/zeroshotlab](https://huggingface.co/zeroshotlab)

---

*India · Edge AI · Building in public · Plan as of 6 Nov 2026 IST · dates are targets, not promises*
