# Unified repository merge notes

This repository combines:

- `ahmedmokireldindevelopers/Startup-Funding-2025`: the React founder operating system and business-building resource library.
- `ahmedmokireldinonline/startup-programs-2026-2027`: the source-first startup credits, grants, accelerators, discounts, and ecosystem directory.

The first repository is the canonical destination because it contains the application and the larger learning library. The second repository's folders (`categories/`, `china/`, `communities/`, `global/`, `imports/`, `open-source/`, `ukraine/`, `archive/`, and `.github/`) were copied without path conflicts.

`data/catalog.csv` was not copied because it is byte-for-byte identical to the retained root `programs.csv` (38 records). `data/README.md` documents the canonical location. The old `public/index.html` was removed because the Vite application now has a single canonical root `index.html` entry point.

The source directory remains the primary reference for program eligibility and application links. Verify official program pages before applying because benefits, deadlines, and eligibility can change.

The two SaaS files `Companies-Grid view (1).csv` and `Companies-Grid view (2).csv` were also byte-for-byte identical. The `(1)` file is the retained canonical copy.
