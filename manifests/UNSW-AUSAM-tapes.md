# UNSW AUSAM series — 22 site tapes (Sydney, ~1978-1988)

Australian University of New South Wales' extended Unix distribution.
22 numbered site tapes preserved on the TUHS Archive containing
progressive additions to V6 and V7 Unix: early networking, sfio
predecessors, community tools, and site-local kernel modifications.

Historically foundational for the Australian Unix community; particular
relevance for `heirloom-vi-darwin` (ex/vi refinements originating from
Sydney) and for AUUGN newsletter cross-references.

## Location on TUHS Archive

Root: `https://www.tuhs.org/Archive/Distributions/UNSW/`

## Tape enumeration (per the mirror)

| Tape | Vintage (approx) | Notes |
| ---: | :--- | :--- |
| 1    | ~1978  | Earliest tape; V6 base + initial AUSAM overlay |
| 2    | ~1979  | V6-based |
| 3    | ~1979  | V6-based |
| 4    | ~1980  | V6/V7 transition |
| 5    | ~1980  | V7-based |
| 6    | ~1980  | V7 additions |
| 7    | ~1981  | V7 continuation |
| 81   | ~1981  | Site tape numbering shift |
| 82   | ~1981  | |
| 83   | ~1982  | |
| 85   | ~1982  | |
| 86   | ~1983  | |
| 87   | ~1983  | |
| 88   | ~1983  | |
| 89   | ~1984  | |
| 90   | ~1984  | |
| 92   | ~1985  | |
| 93   | ~1985  | |
| 106  | ~1986  | Later numbering; possibly external contributor |
| 107  | ~1986  | |
| 108  | ~1987  | |
| 110  | ~1988  | Latest AUSAM tape preserved |

Each tape directory contains `record0.gz` (the raw tape record).

## Content typology

The AUSAM tapes contain:

- Site-local additions to V6/V7 (Sydney's own patches).
- Early networking work (predates BSD sockets).
- `sfio`-style stream I/O experiments.
- Australian-community shell + text-processing extensions.
- Documentation contributions later collected in AUUGN newsletters.

## Licensing

Covered by the Caldera 2002 Ancient UNIX licence grant (V6/V7 base) +
site-specific AUSAM contributions with UNSW's own overlay. Fetch
individual tapes and consult their READMEs.

## Cross-references

- AUUGN back-issues in `moonman81/heirloom-citations-darwin`
  (`tech-reports/auugn-index/`) document AUSAM tape contents.
- V6/V7 base ancestors: see `manifests/V6-donor-tapes.md` and
  `manifests/V7.md` in this repo.
- Sydney's Bob Kummerfeld + Ian Hayes contributions specifically
  relevant to `heirloom-vi-darwin`.

## Why this matters to Heirloom

Australian community Unix constellation. Illustrates that early Unix
evolution was global — not just Bell Labs + Berkeley + Sun — and that
the modern SVR4/POSIX lineage inherits from these community
site-tape contributions in ways that AT&T's official history often
elides.
