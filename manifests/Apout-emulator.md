# Apout — user-mode V7 PDP-11 emulator (Warren Toomey)

Apout runs original PDP-11 V7 binaries as user-space processes on
modern Unix.  Enables literal side-by-side testing between
heirloom-*-darwin tools and their V7 ancestors.

## Location on TUHS Archive

- `https://www.tuhs.org/Archive/Applications/Tools/Emulators/Apout/apout2.3beta1.tar.gz`

## Why this matters to Heirloom

- Enables live behavioural diffing:
    `echo "test" | /opt/heirloom/bin/sort` vs
    `echo "test" | apout /v7/usr/bin/sort`.
- Directly demonstrates the preservation-fidelity claim of the
  Heirloom Project.
- Foundation for a `heirloom-tests-darwin` repo if a live-comparison
  harness is ever built.

## Darwin port status

Not yet ported.  Sender agent estimated 3-5 days of engineering.
Skipped for the initial extension pass; noted for future work.

## Licensing

BSD-style; see the tarball's own COPYRIGHT.
