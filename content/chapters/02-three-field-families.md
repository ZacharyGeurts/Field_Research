## Three families, one literacy

Field Research assumes you have met the three families from Field Primer Chapter 2. We repeat them because **every GuardChip permit and every BoxChip load ultimately serves one of these**.

## Family 1 — GPU fabric (AMOURANTHRTX)

Addressable field state: texels as memory, shaders as operators, SSBO strips as thermodynamic ledgers. Phi · Thermo · Flow on bindings 8–10. CANVAS and Field Die share the same dispatch plane.

<span class="tag impl">Implemented:</span> `AMOURANTHRTX/Navigator/`, fabric map in `amouranthrtx-field-fabric-map.json`.

v2 note: fabric does **not** consult a combinatorics runner facet. Fabric runs; HostChip / BoxChip load is explicit.

## Family 2 — Field Die

The die is silicon metaphor made executable: guest RAM (~64 MiB), `data_bus[64]`, x86 console path (`x86.comp` / FieldX86Core).

Hard limits remain physics boxes:

- 8³ dots per box (512)
- four scale nets — `body` → `room` → `field` → `planetary`
- **`max_field_depth: 0`**

Belt profiles (`belt_1_0` 256 slots, `belt_2_0` 512 slots) are **fixed compile/exec choices**, not leaves on a scored tree.

## Family 3 — Packet field (NEXUS)

Perimeter: gatekeeper, packet-field ring, threat panel `:9477`. Sockets become operator-readable state. Diagnostic mode collapses capability mask under fault.

v2: perimeter posture is a **bitmask + generation**, not a meld plate skip list.

## How families couple (v2)

```
GPU fabric  ←→  Field Die  ←→  Packet field
   C1/C2 chips     C0 HostChip      C4 WireChip
                   C3 GuardChip (INPUT/VIEW/CONTEXT)
```

No middle bus of 30 JSON plates. Coupling is:

1. Shared **sealed generation** (Chapter 6)
2. Shared **capability mask** (Chapter 11)
3. Explicit chip load IDs (Chapter 10)

## Stack roles

| Piece | Role |
|-------|------|
| Grok16 | Unified `g16` driver, belt / field_opt / field_physics profiles |
| NewLatest / NEXUS | Install root, panel, packet field |
| Queen | Browser gate, launch chambers, CHIPS registry |
| AMOURANTHRTX | Fabric + die engine |
| Amouranth Shield | Host install-time hardening (nft, screen baseline) — not the hot-path truth bus |

**Next:** Chapter 3 — thermodynamics as accounting, not heat religion for trees.
