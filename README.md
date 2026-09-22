# fet-mirror

Unofficial source mirror of **FET (Free Timetabling Software)**, version 7.10.5.

- Official project site / downloads: https://lalescu.ro/liviu/fet/
- Original author: Gheorghe Liviu Lalescu
- License: GNU Affero General Public License v3 (see `COPYING`)

This repository is **not affiliated with or endorsed by** the FET project.
It is a straight, unmodified copy of the source tree extracted from the
official release tarball, sourced exactly from:

- Author's own release-tarball repo: https://github.com/lalesculiviu/fet
  (commit [`891e987`](https://github.com/lalesculiviu/fet/commit/891e987188cb64ef590edcd9c38527124b0d113e),
  file `fet-7.10.5.tar.xz`)

## Provenance / integrity

The original release tarball's GPG signature (`fet-7.10.5.tar.xz.asc`) is
included in this repo and in the [v7.10.5 release](../../releases/tag/v7.10.5),
and was verified against the author's public key before mirroring:

```
gpg: Good signature from "Gheorghe Liviu Lalescu <liviu-gpg-key@lalescu.ro>"
Primary key fingerprint: 521C 6E37 95F7 072D 5C64 F541 1AEE 2686 DC2E 2334
```

The tarball was also scanned with VirusTotal (0/62 detections) before
mirroring.

## Building

FET uses Qt6 (>= 6.10) and CMake (>= 3.28), or Qt5 (>= 5.15) with qmake.
See `README.upstream` for full upstream build instructions.

CI (`.github/workflows/build.yml`) compiles both the full GUI target and
the command-line-only target (`-DCOMMAND_LINE_ONLY=ON`) on Linux, Windows
and macOS on every push, as a portability/regression check — there is no
automated unit test suite upstream (`examples/tests/*.fet` are manual
timetabling scenario files, not executable tests).

## Prebuilt binaries

The [v7.10.5 release](../../releases/tag/v7.10.5) includes, in addition to
the original signed source tarball:

- `fet-7.10.5-linux-x86_64.tar.gz` — built on `ubuntu-latest`
- `fet-7.10.5-windows-x86_64.zip` — built on `windows-latest`
- `fet-7.10.5-macos-x86_64.zip` — built on `macos-latest`

These are unofficial builds produced by this repo's own CI from the
unmodified upstream source, for convenience. For official, upstream-signed
installers, use https://lalescu.ro/liviu/fet/download.html instead.
