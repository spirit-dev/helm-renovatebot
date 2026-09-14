# Renovate bot



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
``
