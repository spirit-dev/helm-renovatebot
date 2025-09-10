# Renovate bot

[![GitLab Sync](https://img.shields.io/badge/gitlab_sync-renovatebot-blue?style=for-the-badge&logo=gitlab)](https://gitlab-internal.spirit-dev.net/github-mirror/helm-renovatebot) <!-- markdownlint-disable MD041 -->
[![GitHub Mirror](https://img.shields.io/badge/github_mirror-renovatebot-blue?style=for-the-badge&logo=github)](https://github.com/spirit-dev/helm-renovatebot)
[![App Status](https://argocd-internal.spirit-dev.net/api/badge?name=renovatebot-turingpi&revision=true&showAppName=true)](https://argocd-internal.spirit-dev.net/applications/renovatebot-turingpi)

<!--TOC-->

- [Resources](#resources)
- [Installation process](#installation-process)

<!--TOC-->

## Resources

Testing strategy / debugging can be found here

- ![test](test/Readme.md)

## Installation process

The installation is entirely managed by Argocd.

A `Makefile` is present here to ease the first and one-time deployment or in case of an issue.
The installation should be done in two steps:

```shell
#> make dry-run ENV=<ENV>
#> make install ENV=<ENV>
```
