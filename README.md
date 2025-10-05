
## rocker/r2u: Rocker Containers for r2u

### About r2u

This repository provides containers for [r2u](https://eddelbuettel.github.io/r2u/). It extends /
revisits the initial containers provided by the [r2u](https://eddelbuettel.github.io/r2u/) project.

The containers are uploaded for each of the supported releases under their respective release names
(focal, jammy, noble) and release versions (20.04, 22.04, 24.04).  Builds are for the amd64 platform
and (on 24.04 aka noble only) also for arm64.

### r2u4ci Variant

The `r2u4ci` container adds a few more commands used in standard GitHub Actions.  While the standard
`r2u` container can be used, this variants saves a few extra steps that would have to be taken each
time in the CI setup.

### Background

Please see [motivation](motivation.md) for how it fits in with other Rocker containers.

