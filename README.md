# heirloom-ancestors-darwin

**Museum-tier reference material** for the Heirloom Darwin port —
manifests + annotation notes for the primary-source ancestor code
that heirloom-*-darwin descends from.

> **Not authoritative.** This repo does NOT ship ancestor source code.
> It ships manifests + cross-reference notes that point at the TUHS
> Unix Heritage Archive.  Fetch source from TUHS under your own
> licence reading and drop it into `/opt/heirloom/src/upstream-ancestors/`
> if you want to work with it locally.

## Why this repo exists

The Heirloom project preserves SVR4 Unix behaviour on modern hardware.
Its own source lineage runs:

```
Bell Labs Research UNIX  →  System V / SVR4  →  OpenSolaris (2005)
    →  Gunnar Ritter Heirloom Project (2001-2008)
    →  moonman81 Darwin port (2026 — heirloom-*-darwin)
```

The ancestors of that lineage — V7, 32V, PWB, DWB 1.0, PCC, and the
early BSDs — are what heirloom-*-darwin is a descendant of.  They
are ALSO on the TUHS Archive, and studying them explains:

- Why `/opt/heirloom/bin/ls` (SVID3) differs from `/opt/heirloom/ucb/ls`
  (BSD).  Answer: 32V — the AT&T/BSD divergence point.
- Where `heirloom-sh-darwin`'s `src/sh/` semantics come from.
  Answer: V7 /bin/sh (Bourne 1978).
- Which macros in `heirloom-doctools-darwin` are pre-DWB vs post-DWB.
  Answer: diff heirloom-doctools/src/troff/ against DWB 1.0.

This repo is the ANNOTATION layer that connects the Heirloom-Darwin
port to those ancestors.

## Layout

```
manifests/          per-ancestor pointer manifests (V7.md, 32V.md,
                    DWB-1.0.md, PWB.md, PCC.md, 1BSD-2BSD-3BSD-4BSD.md).
                    Each describes: what's in it, where to fetch it,
                    licensing posture, why it matters to Heirloom.

notes/              per-comparison narrative notes:
                      heirloom-toolchest-vs-V7.md
                      heirloom-toolchest-vs-32V.md
                      heirloom-doctools-vs-DWB-1.0.md
                    Written as sources become locally available and
                    the diff is worth publishing.

cross-references/   pointers into which heirloom-*-darwin source files
                    directly descend from which ancestor files.
                    Enables provenance queries like
                      "which sibling repo has a heirloom-sh-darwin
                       src/sh/main.c ancestor?"
                    Answer:  V7 usr/src/cmd/sh/main.c.
```

## What this repo does NOT ship

- **No ancestor source code.**  The Caldera 2002 Ancient UNIX licence
  covers V1-V7 + 32V; the BSD material has its own overlay; DWB 1.0 is
  AT&T-licensed.  Rather than second-guess any of these, this repo
  provides pointers to TUHS.  Users fetch under their own licence
  reading.
- **No ancestor binaries.**  See `moonman81/heirloom-vi-darwin` for
  the same posture applied to Ritter's ex/vi.

## Recommended local layout

If you want ancestor sources for source-diff research:

```sh
mkdir -p /opt/heirloom/src/upstream-ancestors/
cd /opt/heirloom/src/upstream-ancestors/

# V7
curl -L https://www.tuhs.org/Archive/Distributions/Research/Henry_Spencer_v7/v7.tar.gz \
    -o v7.tar.gz
tar xzf v7.tar.gz -C v7/

# 32V
curl -L https://www.tuhs.org/Archive/Distributions/USDL/32V/32v_usr.tar.gz \
    -o 32v_usr.tar.gz
tar xzf 32v_usr.tar.gz -C 32V/

# DWB 1.0
curl -L https://www.tuhs.org/Archive/Applications/Documenters_Workbench/dwb_1.0.tar.gz \
    -o dwb_1.0.tar.gz
tar xzf dwb_1.0.tar.gz -C dwb-1.0/
```

The `/opt/heirloom/src/upstream-ancestors/` tree is not tracked by any
Heirloom repo.  It's a local read-only reference tree.

## Sibling repos

- <https://github.com/moonman81/heirloom-sh-darwin>
- <https://github.com/moonman81/heirloom-devtools-darwin>
- <https://github.com/moonman81/heirloom-toolchest-darwin>
- <https://github.com/moonman81/heirloom-doctools-darwin>
- <https://github.com/moonman81/heirloom-pkgtools-darwin>
- <https://github.com/moonman81/heirloom-workspace-darwin>
- <https://github.com/moonman81/heirloom-vi-darwin>
- <https://github.com/moonman81/heirloom-citations-darwin>
