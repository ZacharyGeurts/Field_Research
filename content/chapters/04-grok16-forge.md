## From GCC to one driver named g16

Grok16 began as a question: *Can we own the full compile chain for field-native execution without forking reality?*

Answer shipped: unified ELF **`g16`** (auto C/C++ and more), `g++16` compat symlink, distro track 5.x, engine stamp **16.2.0**, default **gnu++26** where mandated.

```bash
export G16_PREFIX=/path/to/Grok16
export GROK16_ROOT="$G16_PREFIX"
./scripts/grok16-toolchain.sh verify
./bin/g16 -dumpversion   # 16.2.0
```

## Fixed profiles — no sense plate ladder on hot path

| Profile | Use |
|---------|-----|
| `belt_1_0` | Baseline belt |
| `belt_2_0` | Default single-fabric belt (512 die slots) |
| `field_opt` | Throughput field kernels (may use fast-math) |
| `field_physics` | Physics-safe — belt spirit without `-ffast-math` |
| `ai` / `vulkan_rtx` | Specialized consumers |

v1 used `g16-compiler-sense-plate.py` + meld to pick expert ladders (−413 ms compile on one host). That was a real receipt — and a **runtime dependency** we reject for v2 architecture.

v2: operator or CI **selects a profile once**. Optional offline `g16 sense` may exist as a bench tool; it must not gate every boot through plate fuse.

## Field CMake

Canonical consumer path:

- `cmake/grok16-toolchain.cmake`
- `cmake/grok16-profile-field-opt.cmake` or `field-physics`
- `scripts/field-cmake.sh` for Queen RTX-style builds

AMOURANTHRTX CMake already detects `g16` / `GROK16_ROOT`. Prefer that over silent g++-14 fallback for field builds.

## Gates that remain

- Ironclad / field sanity on release binaries
- Launch seal generation for `.launch` chambers
- Honesty: scaffold CHIPS vs implemented cores

No gate requires combinatorics `walk_tree_to_end()`.

## Research conclusion

The forge produces **one driver** that speaks field dialects. v2 chooses dialect with a **fixed profile name**, not a scored leaf on a four-facet tree.

**Next:** Chapter 5 — single fabric and belt, depth zero forever.
