## Tombstone — plate meld

<span class="tag impl">Archived design.</span> Do not build new features on this path.

### What v1 built

`field-plate-meld.py` motto: flock + fsync + chain-hash + triple mirror.

Thirty-ish plate sources (iron_plate, gatekeeper, combinatorics, hostess7_brain, spatial, firmware, …) refreshed into one generation-linked JSON. Diagnostic mode gated which sources could refresh. Compiler sense read meld to pick profiles. Compatibility layers and launch seals trusted meld first.

### What was right

- Monotonic generation
- Durability under power loss (fsync + bak)
- Fault isolation impulse (stop refreshing fault-adjacent work)
- Single place for greppable truth

### What was wrong

1. **Fork storms** — subprocess per plate on full meld.
2. **False unity** — “single truth” that re-fused stale peers into multi-MB panels.
3. **Security latency** — keylog/capture policy should not wait on hostess7 + spatial + firmware plates.
4. **Speed** — post-meld hot ratio ~0.986 was a receipt that meld is almost free *after* work; the refresh path was not free.
5. **Depth culture** — every new idea became another plate source.

### What replaces it

Chapter 6 sealed generation: one posture artifact, one bak, generation + mask + profile_id.

Diagnostic mode becomes **mask collapse**, not `_refresh_if_allowed` plate lists.

### Historical files (look-only)

- `lib/field-plate-meld.py` (~1.7k LOC)
- `lib/field-plate-meld-orchestrator.py`
- `data/field-plate-meld-doctrine.json`
- `plate-meld-redundant/`
- FR v1 Chapter 8

### Research conclusion

Meld taught us generation and durability. It must not remain the nervous system of the field stack.

**Next:** Chapter 9 — static layers and launch seals.
