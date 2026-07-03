# Caldera 2001 OSUtils — awk, grep, libregex (LGPL)

Caldera International's August 2001 release of the historical Bell
Labs `awk`, `grep`, and Regular Expression Library under GPLv2+
(awk, grep) and LGPL (libregex).  The direct upstream ancestor from
which Ritter's Heirloom `nawk`/`grep` traces.

## Location on TUHS Archive

- `https://www.tuhs.org/Archive/Applications/Awk_Grep/osutils.tar.gz`
  (~100 KB)

## Content

- `osutils/awkgrep.tar.gz` — awk (with .y grammar) + grep sources
- `osutils/libregex.tar.gz` — regex library
- `osutils/Makefile` + `INSTALL` + `README` — Caldera's release notes

## Licensing

GPL v2 or later (awk, grep); LGPL (libregex).  Full copies of both
licences included in the tarball.

## Why this matters to Heirloom

- `heirloom-toolchest-darwin`'s `nawk/` is a fork of exactly this
  Caldera awk.  Provides the direct upstream ancestor for diff
  studies.
- `heirloom-toolchest-darwin`'s `grep/` is likewise descended.
- `libregex` semantics are what `heirloom-toolchest-darwin/libuxre/`
  reimplements.

## Comparison recommendation

Diff `heirloom-toolchest-darwin/nawk/*.c` against Caldera 2001
`awkgrep/awk/*.c` to catalogue Ritter's port-fixes on top of the
Caldera baseline.
