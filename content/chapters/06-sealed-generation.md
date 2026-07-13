## Truth without plates

v1 iron plate + truth blocks + uncompiled default optimized **dev velocity** while a plate meld bus published “single JSON truth.” That bus grew to thirty sources, subprocess refresh, triple mirrors, and multi-MB panels.

v2 keeps the **intent** (fail-closed trust, uncompiled when appropriate, monotonic generation) and deletes the bus.

## Sealed generation — the one number that matters

| Field | Role |
|-------|------|
| `generation` | Monotonic u64 / integer — bumps on explicit sync or fault collapse |
| `layout_hash` | Digest of die/fabric/capability schema |
| `profile_id` | Fixed string: `belt_2_0`, `field_opt`, … |
| `capability_mask` | GuardChip bits (Chapter 11) |
| `launch_seal.generation` | Must match for `.launch` chamber refresh |

Write path (rare): flock optional · fsync · single `.bak` sibling.  
Read path (hot): compare generation word — **zero allocations when calm**.

Content seal for this book edition (manuscript identity, not runtime posture):

```
SHA256:aVYElqiNin1Q/gcaqa6CGGbJ/gjjG9KXP5ZsXg8uMD8
```

## What happened to truth blocks

Truth blocks remain a **compile / mandate gate** (“may we ship this binary / chamber?”). They no longer **condense plate groups** or prune combinatoric leaves.

Uncompiled default for chambers stays valid: secured `.launch` files refresh only when seal generation matches — Chapter 9.

## Zero-cost 4-slot alignment

Queen `queen-zero-cost-4slot.json` already defines:

| Slot | Guards |
|------|--------|
| TIME | sealed epoch · genesis · entropy verify |
| MEMORY | regions · mmap · foreign write denied |
| THERMO | accountant · budget · FCC scale |
| CONTEXT | syscall generation · layout · seal hash |

Runtime tax: **0**. Tamper: **abort**.

v2 posture seal is the host/panel twin of that engine idea. Same religion: compile-time / boot-time seal, hot path is a compare.

## No fork tax

Forbidden on calm path:

- `subprocess` per plate source
- tree walk scoring
- multi-panel “fuse then read bridge”

Allowed:

- in-process import once
- mmap / atomic read of posture
- explicit operator or CI `sync` command

## Research conclusion

Iron plate language becomes **sealed generation**. Durability stays (one file + bak). Multi-source fuse religion leaves the architecture.

**Next:** Chapter 7 — tombstone of combinatorics.
