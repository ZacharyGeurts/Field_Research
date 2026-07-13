## Layers as map — not as auto-cycle machine

v1 motto: *Pre-baked profiles stack upward — combinatorics runs itself; you ride the layers.*

v2 motto: *Layers name dependencies. Seals name trust. Nothing cycles a tree.*

## Six layers (names kept)

| Index | ID | Role |
|-------|-----|------|
| 0 | substrate | KILROY / linux compat pin |
| 1 | exec | Fixed profile → belt / die / BSP |
| 2 | program | Queen↔NEXUS, toolchain |
| 3 | web | HTML/JS/CSS cage |
| 4 | chips | FieldChip composition (Chapter 10) |
| 5 | surface | NEXUS shell, Queen browser only |

## refresh() without combinatorics

Allowed sequence:

1. Probe layer presence (cheap existence checks)
2. Read or write **sealed generation**
3. Bump `launch_seal.generation` only on explicit sync
4. Publish small panel: live layer flags + `profile_id` + seal

Forbidden:

- `truth_publish → combinatorics cycle → bridge`
- subprocess plate refresh storms
- requiring meld before seal bump

## Launch seals — still the right key

`queen-launch-chamber.py` patterns remain:

- `write_launch_file()` locks by default
- `launch_refresh_allowed(seal_generation)` must match panel generation
- Stale seal fails closed
- `verify_launch_integrity()` on chamber run

Research conclusion **kept from v1**: compatibility sync (now **posture sync**) is the refresh key for launch manifests. Tamper without sync fails closed.

## Operator view

Show:

- L0–L5 on/off
- `profile_id`, die slots
- `launch_seal.generation`
- capability mask summary (GuardChip)

Do **not** show four-level combinatoric trees or thirty plate chain hashes.

## Design alternatives still rejected

| Alternative | Why rejected |
|-------------|--------------|
| Operator runs full tree each boot | Cognitive + heat load |
| Launch refresh without seal | Tampered `.launch` |
| Nested compatibility stacks | Violates depth zero |
| **Layers that secretly cycle combinatorics** | **v2 tombstone** |

## Research conclusion

Layers are literacy. Seals are trust. Profiles are chosen, not scored.

**Next:** Chapter 10 — CHIPs from CHIPs.
