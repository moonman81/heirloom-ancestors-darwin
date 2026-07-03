# heirloom-sh-darwin ← V7 /bin/sh

| heirloom-sh-darwin file           | V7 ancestor                          |
| :-------------------------------- | :----------------------------------- |
| `src/sh/main.c`                   | `usr/src/cmd/sh/main.c`              |
| `src/sh/word.c`                   | `usr/src/cmd/sh/word.c`              |
| `src/sh/expand.c`                 | `usr/src/cmd/sh/expand.c`            |
| `src/sh/macro.c`                  | `usr/src/cmd/sh/macro.c`             |
| `src/sh/jobs.c`                   | (post-V7 — added in SVR2/SVR3 by AT&T |
|                                   | for job control)                     |
| `src/sh/service.c`                | `usr/src/cmd/sh/service.c`           |

## Method

Diff heirloom-sh's `src/sh/*.c` against Spencer's V7 `usr/src/cmd/sh/*.c`
to establish direct-descent claims.  Documented per file when the
diff is done.

## Status

Skeleton table — populate as diffs are performed.
