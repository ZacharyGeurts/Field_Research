## Zero-cost security — Heaven passes free

Motto: **Heaven passes at zero cost. Hell pays.**

Calm path: one compare of sealed generation + capability mask. No proc walk, no plate fuse, no tree.

```
if (generation == sealed && (mask & NEED) == NEED) return ALLOW;
else deny or diagnostic_collapse();
```

## GuardChip (C3) slots

Extend Queen’s zero-cost 4-slot (TIME · MEMORY · THERMO · CONTEXT) with host-critical permits:

| Slot | Seals | Default |
|------|-------|---------|
| TIME | epoch · monotonic generation | sealed |
| MEMORY | die/canvas region policy | no foreign write |
| THERMO | entropy budget | budgeted |
| CONTEXT | layout hash · launch seal | sealed |
| **INPUT** | who may read keys / inject | **deny hooks** |
| **VIEW** | who may sample pixels | **deny capture** |

Optional: CLIP lane for paste channel (ghost clipboard patterns already in host-desktop).

## Keylogging

v1 inventory: name denylists in `admin-window-shield.py`, `hardware_wire_registry.py`, `NEXUS_NO_KEYBOARD_HOOK`, Amouranth Shield anti-surveillance.

**Gap:** renamed binaries, in-process hooks, kernel modules slip past polls.

**v2 design:**

- INPUT slot grants only seat owner + field keybinding service
- Synthetic inject tools (xdotool class) never receive grant near admin surfaces
- Polling scanners become **dirty-mask only** (pay when generation dirty), not 30s forever storms
- Browser admin portals keep CSP: no unexpected keyboard capture APIs

<span class="tag impl">Partial today:</span> denylists + env flags.  
<span class="tag phil">Target:</span> capability seat model with zero calm tax.

## Screenshots and screen capture

v1: block spectacle/grim/obs-class procs; Amouranth Shield screen_guard; OBS PipeWire whitelist as intentional hole; AmmoCode collab **element-only**, no `getDisplayMedia`, host grant, max 2 fps.

**v2 design:**

| VIEW mode | Meaning |
|-----------|---------|
| `0` | No capture |
| `obs_pipewire:<fingerprint>` | Explicit OBS permit |
| `collab_element` | AmmoCode-style element share |
| `operator_grant` | Time-boxed screenshot grant |

Full desktop scrape without VIEW bit = deny. Engine framebuffer reads bound to MEMORY + VIEW.

## Diagnostic mode (bitmask, not plate list)

v1 fault signals stay meaningful: ironclad sanity, g1id, io-packet, filesystem critical, thermal crit, brain corruption.

engage():

1. detect_problems
2. `mask &= BASELINE`
3. `generation++`
4. baseline-only modules
5. clear only after `debug_self` passes

No meld `_refresh_if_allowed`. No combinatorics skip.

## Beyond-DARPA doctrine — honesty

`beyond-darpa-security-doctrine.json` states high ambition (human channels situational, machine hostile, fail-closed). Label claims:

- Doctrine file + assess API: **Implemented** scaffolding
- “Exceeds DARPA/Lockheed”: **Philosophy** until gates are seat-level and compile-sealed

v2 prefers **working zero-cost mask** over slogan tier names.

## Host install vs field hot path

| Layer | Role |
|-------|------|
| Amouranth Shield (`ammo.sh`) | Host nft, screen baseline, OBS whitelist install |
| GuardChip FSC | Runtime field permits for NEXUS/Queen/engine |
| AmmoCode security | Collab tunnel + screenshare session proofs |

One permit **ledger schema**; three surfaces may enforce.

## Research conclusion

Perimeter is not only firewall rules. It is **which capabilities exist when generation is calm**. Keylog and screenshot defense graduate from name lists to **GuardChip slots** without paying for Hell when Heaven is quiet.

**Next:** Chapter 12 — Queen desktop wires VIEW/INPUT.
