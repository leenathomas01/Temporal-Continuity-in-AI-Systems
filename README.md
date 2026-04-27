> AI systems are no longer stopping. This repo explores what that changes.

---

# Temporal Continuity in AI Systems

A systems framework for understanding the shift from stateless to continuous AI - and why it creates a control problem across cognitive, infrastructure, and governance layers.

---

## What this is

AI systems are no longer stopping. This repo explores what that changes.

A framework for understanding a specific transition in AI systems: the shift from **stateless** (each query is an isolated event) to **continuous** (persistent, agentic, always-on).

This transition is usually framed as a capability upgrade. It is also a control systems problem — and one that appears simultaneously across cognitive, infrastructure, control, physical, and geopolitical layers.

The central claim is not about intelligence levels. It is about timing:

> Systems don't fail because they are too powerful.
>
> They fail because they operate faster than their stabilisers.

---

## The model

Three time domains:

| | Speed | Examples |
|---|---|---|
| **t₁** Human/institutional | Slow | ~200ms cognition, years of regulation, seconds of grid response |
| **t₂** Machine execution | Fast | Millisecond inference, MW/second load changes, microsecond switching |
| **t₃** Buffer layer | Mediating | The rate-matching mechanism that lets t₁ and t₂ coexist |

t₃ is the design principle, not a specific technology. At each layer of the stack, it takes a different form. At each layer, it is currently underdeveloped relative to the pace of t₂ deployment.

![Three Time Domains](/time-domains.png)

---

## How to read this repo

**Start here:** `ReadMe_one_page_model.md` - the full framework compressed into one page. Tables, failure modes, and t₃ per layer. Read this first.

**Then, by interest:**

| File | What's in it |
|---|---|
| `01_the_stack.md` | Core model: where the mismatches are and why |
| `02_continuity_pandora.md` | Why continuity specifically is the hinge, not capability level |
| `03_cognitive_layer.md` | Bandwidth, semantic drift, and the death of white space |
| `04_infrastructure_layer.md` | Grid inertia, converter-dominated loads, and AI data centre load dynamics |
| `05_gii_bridge.md` | Grid Inertial Interface — a hardware t₃ prototype (pointer to separate repo) |
| `06_geopolitical_layer.md` | Capability diffusion, governance lag, and what "portals" actually mean |
| `appendix_chaos_origin.md` | Original speculative draft, preserved intact — where the framework started |
| `08_metaphor_map.md` | Translation table: chaos-layer constructs → grounded interpretations |

The files are modular. They cross-reference but don't require sequential reading.

---

## Two modes

The repo operates in two modes, explicitly labelled:

**Grounded** - engineering, data, testable hypotheses. Claims are bounded.

**Chaos layer** - speculative metaphors used as intuition scaffolding. Preserved as an honest record of how the framework developed, not as literal models of physical reality.

The appendix is the full chaos-layer origin draft. The metaphor map translates it.

---

## What this is not

- An implementation repo. There is no production code here.
- A claim that AI cognition has physical electromagnetic effects.
- A finished framework. This is v0.1 - conceptual, simulation-ready in parts, not field-validated.

The open questions are documented explicitly in each layer file.

---

## Related work

**Medium** — narrative version of the core argument: [Temporal Continuity of AI Systems: The Real Pandora's Box](https://medium.com/@leenathomas01)

**GII protocol** — the infrastructure t₃ proposal, published separately: [The Grid Doesn't Need More Energy. It Needs More Inertia.](https://medium.com/@leenathomas01/the-grid-doesnt-need-more-energy-it-needs-more-inertia-633c77992552)

---

## Status

`v0.1` — April 2026

Conceptual framework. Grounded in control theory, power systems engineering, and cognitive science analogues. Cross-layer synthesis is the contribution; individual layers draw on existing bodies of work.

The open questions in each file are genuine.

---

---

