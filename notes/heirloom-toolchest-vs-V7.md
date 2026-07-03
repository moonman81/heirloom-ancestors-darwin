# Comparison note: heirloom-toolchest-darwin vs V7 (Bell Labs 1979)

## Scope

Structured comparison of the utilities in
`heirloom-toolchest-darwin` (2007 Ritter release,
`heirloom-070715`) against V7 (`v7.tar.gz` on TUHS).

## Status

Skeleton note — waiting for a local V7 extraction under
`/opt/heirloom/src/upstream-ancestors/v7/`.  Populate with actual
diffs when a study is done.

## Preliminary observations

- Heirloom's `nawk` (Aho/Weinberger/Kernighan new awk) has no
  direct V7 equivalent.  V7 shipped only the original AWK (which
  is what `heirloom-toolchest-darwin`'s `oawk` implements).
- V7's `ls` did not carry the `-h` (human-readable) or `-1`
  (one-per-line) flags that later became standard.  Compare
  V7 `ls.c` against `heirloom-toolchest-darwin/ls/ls.c`.
- V7's `cp` was one-shot only.  Ritter's toolchest port supports
  the SVR4 `-r` recursive form directly.

## References

- V7 manuals: <https://www.tuhs.org/Archive/Documentation/Manuals/UNIX-7th/>
