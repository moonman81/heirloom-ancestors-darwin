# Comparison note: heirloom-toolchest-darwin's bin/ vs ucb/ — the 32V hinge

## Why bin/ vs ucb/ exists

Above 32V, one Unix.  Below 32V, two lineages:
- AT&T → System III → SVR4 → OpenSolaris → heirloom-toolchest-darwin bin/.
- Berkeley → 1BSD → 2BSD → 3BSD → 4BSD → BSDs → heirloom-toolchest-darwin ucb/.

32V (Reiser & London, 1979) is where the two histories fork.

## Which utilities have both variants

`heirloom-toolchest-darwin` ships parallel variants for utilities that
had substantively different behaviour in the AT&T and Berkeley
lineages.  Examples: `ls`, `who`, `ps`, `df`, `chmod`, `echo`.

## Status

Preliminary — full per-utility diff pending a local 32V extraction.
