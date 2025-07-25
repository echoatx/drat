## Installation

To install an R package hosted here in ECHO's DRAT R package archive, you must direct `install.packages` to install from the Austin ECHO DRAT repository (hosted using GitHub Pages on the public internet).

For example, to install the "ECHO" package use `install.packages` with the `repos` option limited to this repository only (to not bother searching CRAN, since the "ECHO" package won't be found there).

``` r
## install from the Austin ECHO DRAT Repository
install.packages("ECHO", repos = "https://echoatx.github.io/drat")
```

## Updating

To update the ECHO package, call `update.packages()`. Since *ECHO* was installed from a different repository than CRAN, and our DRAT repository is known to R from when it installed the ECHO package, you should not need to specify the repository again, but you may find it helpful to do so.

``` r
update.packages(repos = c(getOption("repos"), "https://echoatx.github.io/drat"))
```

To ease things, it is best to add the following to your user R profile settings.

``` r
options(repos = c(getOption("repos"), "echoatx" = "https://echoatx.github.io/drat"))
```
