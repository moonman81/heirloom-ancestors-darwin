# Comparison note: heirloom-doctools-darwin vs DWB 1.0 (AT&T 1988)

## Status

Skeleton note — waiting for a local DWB 1.0 extraction.

## Framework

DWB 1.0 → OpenSolaris ~ 2005 → Heirloom (2001-2008) → moonman81 Darwin port (2026).

## Diff dimensions to catalogue

- `troff/`: additions in Heirloom for OpenType font handling, hyphenation
  library integration (libhnj), postscript output improvements.
- `tbl/`, `eqn/`, `pic/`: syntactic additions post-DWB.
- `refer/`: bibliographic database format compatibility.
- `mm/ms/me` macros: any additions beyond the DWB 1.0 baseline.

## References

- Ossanna 1977 (CSTR #54) — troff user's manual;
  in `heirloom-citations-darwin/tech-reports/bell-labs-cstr/54.pdf`.
