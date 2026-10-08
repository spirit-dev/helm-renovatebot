# DOX: test/

<!--TOC-->

______________________________________________________________________

**Table of Contents**

- [Purpose](#purpose)
- [Ownership](#ownership)
- [Local Contracts](#local-contracts)
- [Work Guidance](#work-guidance)
- [Verification](#verification)
- [Child DOX Index](#child-dox-index)

______________________________________________________________________

<!--TOC-->

## Purpose

Local manual testing of Renovate Bot against the real GitLab instance via Docker, bypassing the Helm deployment.

## Ownership

- Everything under `test/`

## Local Contracts

- `config.example.json` is the committed template; `config.json` holds real tokens and is gitignored.
- Keep the docker run command in `test/Readme.md` in sync with the image tag and config path.

## Work Guidance

- Run from repo root so the mounted path in `Readme.md` matches; adjust the volume path to your checkout before running.
- Use `LOG_LEVEL=debug` when debugging renovate behavior.

## Verification

- No automated verification; manual docker run only (see `Readme.md`).

## Child DOX Index

None. Flat directory (Readme.md, config.example.json).
