# fet-mirror

Unofficial source mirror of **FET (Free Timetabling Software)**, version 7.10.5.

- Original project and official releases: https://lalescu.ro/liviu/fet/
- Original author: Gheorghe Liviu Lalescu
- License: GNU Affero General Public License v3 (see `COPYING`)

This repository is **not affiliated with or endorsed by** the FET project.
It is a straight, unmodified copy of the source tree extracted from the
official release tarball `fet-7.10.5.tar.xz`, published at the link above.

## Provenance / integrity

The original release tarball's GPG signature (`fet-7.10.5.tar.xz.asc`) is
included in this repo and was verified against the author's public key
(fingerprint `521C 6E37 95F7 072D 5C64 F541 1AEE 2686 DC2E 2334`) before
mirroring:

```
gpg: Good signature from "Gheorghe Liviu Lalescu <liviu-gpg-key@lalescu.ro>"
```

## Building

FET uses Qt (>= 5.15, or Qt6) and CMake (>= 3.28) or qmake. See `README`
for full build instructions. A GitHub Actions workflow in this repo builds
the project on every push as a compile-check (there is no automated unit
test suite upstream — `examples/tests/*.fet` are manual timetabling
scenario files, not executable tests).
