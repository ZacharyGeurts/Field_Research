## Tombstone — the combinatorics tree

<span class="tag impl">Archived design.</span> Do not build new features on this path.

### What v1 built

`Grok16/lib/field_combinatorics.py` was the authoritative engine for facet math:

1. **launch_mode**
2. **belt_profile**
3. **truth_tier**
4. **runner** (native BSP / emulator / belt)

`combinatoric_tree()` → `walk_tree_to_end()` → `condense_plates()` → panel JSON → bridge `exec_posture`.

UX evolution:

| Phase | UX |
|-------|-----|
| 1 | Operator combinatorics studio |
| 2 | Grok16 engine |
| 3 | Plate combinatorics bridge |
| 4 | Compatibility layers auto-cycle (v1 current) |
| **5 (v2)** | **Tree deleted from hot path** |

### Why it died

1. **Field speed** — scoring leaves and condensing groups on refresh is not free.
2. **Security** — posture for keylog/capture must not wait on a tree.
3. **Honesty** — “auto combinatorics” still meant forks, panels, and drift.
4. **CHIPS** — `runner: emulator` inverted chip identity; chips should be **loaded by ID**, not selected as a scored facet.
5. **Single fabric** — the tree re-encoded fixed physics (depth 0, 512 dots) as explorable options. Physics is not a menu.

### What replaces it

| Old | New |
|-----|-----|
| Facet tree | Fixed profile table |
| Terminal leaf score | Explicit `profile_id` |
| Speed cap walk | Bench JSON offline + documented headroom |
| `runner: emulator` | BoxChip / EraChip load (Chapter 10) |
| `/api/combinatorics` | Gone or 410 → layers / posture |

### Historical files (look-only)

- `Grok16/lib/field_combinatorics.py`
- `lib/field-combinatorics-studio.py`
- `lib/field-plate-combinatorics-bridge.py`
- `data/*combinatorics*` panels
- FR v1 Chapter 7

Keep benches under `docs/` if useful. Do not wire panel boot to them.

### Research conclusion

Combinatorics answered “don’t make the operator crank.” v2 answers “don’t make the machine crank either.”

**Next:** Chapter 8 — tombstone of plate meld.
