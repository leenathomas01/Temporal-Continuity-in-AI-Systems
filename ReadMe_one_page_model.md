> AI systems are no longer stopping. This repo explores what that changes.

---

# One-Page Model
### *The whole thing, compressed*

---

## The premise

AI is moving from stateless (each query is isolated) to **continuous** (persistent, agentic, always-on).

This is not just a capability change. It's a control systems problem.

---

## Three timelines

| | Speed | Examples |
|---|---|---|
| **t₁** Human/institutional | Slow | ~200ms cognition, years of regulation, seconds of grid response |
| **t₂** Machine execution | Fast | Millisecond inference, MW/second load changes, microsecond switching |
| **t₃** Buffer layer | Mediating | The thing that lets t₁ and t₂ coexist without breaking each other |

t₃ is the missing piece. It doesn't exist yet at the scale the problem requires.

![Three Time Domains](/time-domains.png)

---

## Five mismatches

The same pattern appears at every layer of the system:

```
fast system + slow system + no buffer = instability at the interface
```

| Layer | Fast (t₂) | Slow (t₁) | What breaks |
|---|---|---|---|
| **Cognitive** | AI output rate | Human audit speed | Oversight, independent judgment |
| **Infrastructure** | Compute load changes | Grid response time | Frequency stability, inertia deficit |
| **Control** | Agent state evolution | Human comprehension | Interpretability, accountability |
| **Physical** | Decision-to-action latency | Human intervention window | Irreversible consequences |
| **Geopolitical** | Capability deployment | Governance formation | Safety architecture, coordination |

---

## Five failure modes

**Loop gain runaway** — feedback tightens until the system oscillates or locks in. Corrections stop working because they arrive after the error has already compounded.

**Oversight collapse** — humans remain nominally in the loop but can no longer track system state. Decisions get made without the understanding to contest or correct them.

**Inertia deficit** — the system loses its natural damping. Small disturbances that would have been absorbed now propagate. (Applies to grids and to institutional response alike.)

**Narrative lag** — the pace of change exceeds the pace of explanation. Decisions can no longer be reconstructed, audited, or learned from.

**Capability diffusion** — new compute deployments extend capability into contexts faster than safety architecture and governance can form around them.

---

## The t₃ buffer (what it looks like per layer)

| Layer | t₃ in practice |
|---|---|
| Cognitive | Batched outputs, enforced review windows, async playback, state resets |
| Infrastructure | Synthetic inertia, flexible load management, physically decoupled microgrids |
| Control | Checkpointing, replayable decision traces, human approval gates |
| Physical | Actuation limits, operational design constraints, redundancy |
| Geopolitical | Compute licensing, international red lines, shared safety standards |

---

## The unified principle

> Systems don't fail because they are too powerful.
> They fail because they operate faster than their stabilisers.

This applies to brains, grids, organisations, geopolitics, and AI — simultaneously, in the current moment.

---

## What this repo is

Eight files exploring the above across different domains, in two modes:

**Grounded** - real engineering, real data, testable hypotheses.

**Chaos layer** - speculative metaphors used as intuition tools, preserved intact, explicitly labelled.

Start anywhere. The README has the map.

---

*[README.md](./README.md) → full index*
