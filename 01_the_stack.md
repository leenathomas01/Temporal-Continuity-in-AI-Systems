> AI systems are no longer stopping. This repo explores what that changes.

---

# The Temporal Mismatch Stack

*Core model. Everything else in this module builds on this.*

---

## The premise

AI is moving from stateless (each prompt is a fresh start) to **temporally continuous** (persistent state, running agents, always-on inference). This is not a small upgrade. It changes the fundamental dynamics of human-machine interaction — and of the electrical infrastructure that runs it.

The risk isn't that systems become smarter than us. The risk is that systems become **faster than we can supervise them**, and we don't notice until the buffers are already gone.

---

## Two time domains

**t₁ — Human/institutional time**

- Cognitive loop: ~100–300ms per decision cycle
- Sequential reasoning, limited working memory
- Regulatory cycles: months to years
- Grid response timescales: seconds

**t₂ — Machine execution time**

- Sub-millisecond to microsecond operations
- Parallel, recursive, stateful
- Inference: milliseconds
- Training load changes: seconds, at gigawatt scale

> These are abstractions, not literal clocks. "t₂ is faster than t₁" means systems evolve state faster than humans can audit it — not that time dilates.

---

## The mismatches (stacked)

Each layer has its own version of the same problem: **a fast system directly coupled to a slow one, with insufficient buffering between them.**

### 1. Cognitive mismatch

Human cognition cannot track AI outputs at production speed. Decision density compresses. Verification time shrinks. Humans begin deferring to outputs rather than evaluating them.

This is not a failure of intelligence — it's a bandwidth problem. You can't audit a system that updates faster than you can read it.

**Failure modes:** cognitive lock-in, oversight collapse, confirmation loops, loss of independent judgment.

### 2. Infrastructure mismatch

Modern AI workloads don't pull power like traditional industrial loads. They pull in bursts, ramp at hundreds of megawatts per second, and increasingly — as persistent agents replace batch training — they pull *continuously* at gigawatt scale.

Power grids are engineered around the assumption of distributed, variable, self-damping load. A concentration of always-on compute that acts as a single coherent demand signal breaks those assumptions.

**Failure modes:** sympathetic tripping, frequency excursions, grid instability under load concentration.

### 3. Control mismatch

Human-in-the-loop oversight assumes the loop has a manageable cycle time. As AI systems become persistent agents — acting, observing, adapting in continuous cycles — the human's ability to meaningfully audit degrades.

The system doesn't stop being supervised. It starts being supervised too slowly to catch errors before they compound.

**Failure modes:** narrative lag (can't explain why decisions were made), epistemic gap (can't verify intermediate reasoning), institutional lag (governance structures designed for discrete deployments).

### 4. Physical mismatch

When AI leaves the screen and enters the world — robotics, autonomous vehicles, real-time infrastructure control — the latency between decision and consequence shrinks to below the human intervention threshold.

A text hallucination is correctable. A physical action may not be.

**Failure modes:** irreversible consequence, loss of intervention window, control handoff without readiness.

### 5. Geopolitical mismatch

Advanced AI capability is scaling faster in infrastructure terms than global coordination mechanisms can match. Each new compute cluster — a "portal" in informal shorthand — extends capability into a new context without synchronised governance.

**Failure modes:** uneven safety standards, competitive race dynamics, capability diffusion outpacing alignment work.

---

## The missing layer: t₃

Each mismatch above has the same structural solution: **a buffer that rate-matches the fast system to the slow one.**

**t₃** is the name for whatever performs that function at a given layer:

| Layer | t₃ equivalent |
|---|---|
| Cognitive | Batched outputs, enforced review windows, async playback |
| Infrastructure | Synthetic inertia, flexible load management, DC-isolated microgrids |
| Control | Checkpointing, replayable decision traces, human approval gates |
| Physical | Operational design constraints, actuation limits, redundancy |
| Geopolitical | International compute registries, capability governance, shared red lines |

t₃ is not a single thing. It's a design principle: **don't couple fast systems directly to slow ones without a translation layer.**

---

## Testable hypotheses

These are what a grounded version of this model would eventually validate:

**H1:** Lower interaction latency increases reliance on AI outputs and reduces critical evaluation.

**H2:** Continuous AI sessions reduce the diversity of hypotheses a user considers over time.

**H3:** Introducing structured delays (t₃ mechanisms) at the interface improves decision quality relative to real-time interaction.

**H4:** Concentrated, continuous AI load clusters exhibit measurable instability signatures in regional grid data that differ from equivalent-magnitude traditional industrial loads.

---

## What this is not

This model does not claim:
- AI cognition leaks into electromagnetic fields
- Human attention creates physical feedback effects
- External intelligences are responding to compute infrastructure

The "temporal mismatch" is a control systems problem. The solution space is engineering, governance, and interface design — not shielding.

---

*Next: [02_continuity_pandora.md](./02_continuity_pandora.md) — why continuity specifically is the hinge*
