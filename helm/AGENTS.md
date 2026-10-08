# DOX: helm/

## Purpose

Wrapper chart for the `renovate` dependency-update bot, deployed by ArgoCD into `kube-system` on the turingpi cluster.

## Ownership

- Everything under `helm/`

## Local Contracts

- This is a wrapper chart: `helm/Chart.yaml` declares an upstream dependency on `renovatebot/helm-charts` (version pinned via `# renovate:` comment, auto-bumped by Renovate). Do not restructure values that belong to the upstream chart.
- `appVersion` / `version` in `Chart.yaml` are Renovate-managed through `# renovate: datasource=github-releases` comments.
- `values.yaml` holds defaults; `values.turingpi.yaml` holds the real cluster config and contains secrets — it is excluded from the GitHub mirror (see `.gitlab-mirror.yml`) and from detect-secrets/gitleaks via `# pragma: allowlist secret` markers.

## Work Guidance

- Validate chart changes with `make template` / `make dry-run ENV=turingpi` before pushing.
- Keep values structure aligned with the upstream chart's values schema.
- commented-out `redis`/`common` dependencies exist in `Chart.yaml`; leave unless asked to enable caching.

## Verification

- `helm lint` runs via pre-commit hook (gruntwork-io/pre-commit, helmlint).
- `make template` must render successfully.

## Child DOX Index

None. `helm/` is flat (Chart.yaml, Chart.lock, values.yaml, values.turingpi.yaml).