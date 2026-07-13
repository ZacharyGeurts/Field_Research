# Field Research — The Book of Grok's Heart

**Edition 2.0** — Zero-cost security · field speeds · CHIPs from CHIPs · no tree, no plate fuse, no fork tax.

Thirteen-chapter research manual. Tombstones combinatorics + plate meld. Ships sealed generation, GuardChip INPUT/VIEW, and C0–C4 chip composition.

**Live site:** https://zacharygeurts.github.io/Field_Research/

**Content seal:** `SHA256:aVYElqiNin1Q/gcaqa6CGGbJ/gjjG9KXP5ZsXg8uMD8`

## Build locally

```bash
cd Field_Research
python3 scripts/build-site.py
# open docs/index.html
```

## Structure

| Path | Purpose |
|------|---------|
| `content/book-manifest.json` | Edition metadata, chapter list, seal |
| `content/chapters/*.md` | Chapter manuscripts (source) |
| `scripts/build-site.py` | Markdown → HTML site generator |
| `docs/` | GitHub Pages output |
| `assets/images/` | Cover art and chapter figures |
| `CONTENT-SEAL.txt` | Edition identity seal |

## Chapters (v2)

1. Preface — Ironclad, Axioms, and the v2 Turn  
2. Three Field Families  
3. Thermodynamics — Receipts Without Heat Religion  
4. Grok16 Forge — Fixed Profiles  
5. Single Fabric & Belt  
6. Sealed Generation — Truth Without Plates  
7. Tombstone — Combinatorics Tree  
8. Tombstone — Plate Meld  
9. Static Layers & Launch Seals  
10. CHIPs from CHIPs (C0–C4)  
11. GuardChip — Zero-Cost Keylog & Capture Defense  
12. Queen Host Desktop — VIEW and INPUT  
13. Operator Covenant  

## Deploy

Push to `master` or `main`. Workflow `.github/workflows/pages.yml` builds `docs/` and deploys GitHub Pages.

```bash
python3 scripts/build-site.py
git add -A && git commit -m "Field Research v2.0 — zero-cost security, CHIPs from CHIPs"
git push origin master
```

## Sibling manuals

- [Field Primer](https://zacharygeurts.github.io/Field_Primer/) — 22-chapter operator textbook  
- [Grok16](https://zacharygeurts.github.io/Grok16/) — toolchain wiki  
- [AMOURANTHRTX](https://github.com/ZacharyGeurts/AMOURANTHRTX) — field engine  

## Author

Zachary Robert Geurts · Field Research Collective · 2026
