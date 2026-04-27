> AI systems are no longer stopping. This repo explores what that changes.

---
# GII: The Hardware Buffer
### *A pointer to the infrastructure t₃ prototype*

---

This file is a bridge, not a full document. The Grid Inertial Interface (GII) is a separate body of work — a protocol specification for synthetic inertia provision by converter-dominated loads, with data centres as the primary deployment context.

It's documented here because it independently arrived at the same structural conclusion as the temporal mismatch model: **stability requires a translation layer between fast and slow systems, and that layer has to be designed, not assumed.**

---

## What GII is (briefly)

GII defines how an inertia-providing device must behave at the grid boundary — a behavioural protocol, not a product. The one-line version:

> *GII makes renewables and data centres behave like turbines to the legacy grid.*

It's closer to TCP/IP than to a router. Any hardware with a controllable energy reservoir and a grid-forming inverter can be GII-compliant.

---

## The dual-layer architecture

The data centre implementation uses two layers that don't directly communicate with each other:

**Buffer layer (compute-facing)**
- Absorbs millisecond-scale GPU load spikes using fast-response storage
- Hides compute chaos from the grid
- Knows nothing about grid frequency

**Inertia layer (grid-facing)**
- Responds to frequency, RoCoF, and voltage
- Behaves like a turbine: inject energy when frequency drops, absorb when it rises
- Knows nothing about what the GPUs are doing

The two layers interact only through power flow on a shared DC bus. No control signals cross the boundary.

This single constraint — **asymmetric sensing** — eliminates the control-loop instability that plagues systems where grid-side and load-side controllers can interact.

---

## Priority resolution via physics

When both layers need energy simultaneously (a training job kicks off while the solar farm is clouded over), DC bus voltage drops.

Priority resolves itself without a scheduler or coordinator: bus voltage below threshold triggers compute throttling.

*A training run can pause for 500 milliseconds. Grid frequency cannot.*

This is policy encoded in physics. It doesn't require negotiation, communication, or governance. The buffer mediates through energy, not signals.

---

## The connection to this module

GII is the infrastructure equivalent of t₃. It doesn't try to make data centres slower or grids faster. It inserts a buffer that allows them to coexist without their dynamics coupling directly.

The same pattern applies at every layer of the temporal mismatch stack:
- Don't make the fast system slower
- Don't expect the slow system to keep up
- Build the buffer that lets them coexist

GII just happens to be the version of that buffer you can specify, simulate, and eventually build.

---

## Current status

The GII protocol specification is at v0.1 — conceptual framework, simulation-ready, not production-complete. The repo is private. The full architecture (state machine, droop curves, degradation logic, island detection, validation suite, regional grid code mapping) is available on request.

A public concept note was published March 2026: [The Grid Doesn't Need More Energy. It Needs More Inertia.](https://medium.com/@leenathomas01/the-grid-doesnt-need-more-energy-it-needs-more-inertia-633c77992552)

---

## The five open questions (briefly)

1. **Droop density scaling law** — R as a function of node density, with stability envelope boundaries. Needs eigenvalue analysis.
2. **RoCoF threshold derivation** — generalised framework that works across grid types.
3. **Flywheel MTBF under real duty cycles** — published data assumes calmer operation than a volatile grid actually provides.
4. **Who owns the interface?** — the dual-layer topology spans data centre power engineers, utility operators, and inverter vendors. No one currently owns the boundary where GII lives. This is probably the biggest practical barrier.
5. **Inertia market immaturity** — in most U.S. markets, inertia isn't yet a compensated ancillary service. The ROI case currently depends on behind-the-meter benefits.

---

*Back to: [04_infrastructure_layer.md](./04_infrastructure_layer.md)*  
*Next: [06_geopolitical_layer.md](./06_geopolitical_layer.md)*
