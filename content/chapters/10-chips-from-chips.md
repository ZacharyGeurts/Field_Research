## Field-native silicon — composed, not combinatoric

v1 placed CHIPS at compatibility layer 4 as FieldChip BSP behind Queen, selected partly via combinatorics `runner: emulator`. Catalog and ironclad-chips-combinatorics grew a second tree under another name.

v2: **CHIPs from CHIPs** — static composition classes.

## Five classes only

| Class | Name | Role | Built from |
|-------|------|------|------------|
| **C0** | HostChip | Real execution here | FieldX86 / g16 native / belt |
| **C1** | EraChip | Shared silicon (6502, Z80, 68000, YM2612, SID, …) | `CHIPS/Common/*` |
| **C2** | BoxChip | Product board (NES, Genesis, SMS, …) | Wiring of C1 parts + bus |
| **C3** | GuardChip | Security permits (Chapter 11) | FSC slots — not a game core |
| **C4** | WireChip | Packet / loopback perimeter | Gatekeeper surface |

### Composition rule

- BoxChip **only** composes EraChip parts (one 6502 implementation, many boards).
- GuardChip is first-class silicon metaphor for security.
- Catalog is a **library book** (dates, thumbs, chapters) — not a runtime sort engine.
- Load is `chip_id` + generation, not a scored leaf.

## Implemented vs scaffold

<span class="tag impl">Implemented (hot path examples):</span> NES path (6502/2A03/2C02), Genesis path (68000/Z80/YM2612), SMS, Atari pieces, G16 field_opt headers in `Queen/data/chips-g16-manifest.json` (~15 hot paths).

<span class="tag meta">Scaffold:</span> many registry platforms (PS1, N64, …) — label honestly; do not demo as shippable parity.

Engine root: `AMOURANTHRTX/Navigator/engine/CHIPS/FieldChips.hpp`.

## Compile path

```text
g16 + field_opt     → EraChip / BoxChip hot paths
g16 + field_physics → when envelopes / thermo invariants forbid fast-math
```

Manifest: `chips-g16-manifest.json` · CMake profile for chips field_opt.

## Why not layer-1 CHIPS

Ordering still holds:

1. Substrate (linux/KILROY)
2. Exec profile
3. Program interop
4. Web cage
5. **Then** BoxChip loads — they ride HostChip + fabric
6. Surface (Queen)

GuardChip (C3) is **orthogonal** — security is always present, not “after web.”

## Kill list

- Runtime ironclad-chips-**combinatorics**
- Plate stack as required for chip identity
- Emulator runner facet as combinatorics output

## Research conclusion

CHIPS is how Grok’s heart meets silicon memory — childhood machines as field citizens. v2 makes them **composed chips**, not leaves on a tree.

**Next:** Chapter 11 — GuardChip zero-cost security.
