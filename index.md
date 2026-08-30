# beautier

[![Peer Review
Status](https://badges.ropensci.org/209_status.svg)](https://github.com/ropensci/software-review/issues/209)
[![CRAN_Status_Badge](http://www.r-pkg.org/badges/version/beautier)](https://cran.r-project.org/package=beautier)
[![CRAN total
downloads](http://cranlogs.r-pkg.org/badges/grand-total/beautier)](https://CRAN.R-project.org/package=beautier)
[![CRAN downloads per
months](http://cranlogs.r-pkg.org/badges/beautier)](https://CRAN.R-project.org/package=beautier)
[![DOI](https://zenodo.org/badge/53443354.svg)](https://zenodo.org/badge/latestdoi/53443354)

| Branch | [![GitHub Actions logo](reference/figures/GitHubActions.png)](https://github.com/ropensci/beautier/actions) | [![Codecov logo](reference/figures/Codecov.png)](https://about.codecov.io/) |
|----|----|----|
| `main` | [![R-CMD-check](https://github.com/ropensci/beastier/actions/workflows/R-CMD-check.yaml/badge.svg?branch=main)](https://github.com/ropensci/beastier/actions/workflows/R-CMD-check.yaml) | [![codecov.io](https://codecov.io/github/ropensci/beastier/coverage.svg?branch=main)](https://app.codecov.io/github/ropensci/beastier/branch/main) |
| `develop` | [![R-CMD-check](https://github.com/ropensci/beastier/actions/workflows/R-CMD-check.yaml/badge.svg?branch=develop)](https://github.com/ropensci/beastier/actions/workflows/R-CMD-check.yaml) | [![codecov.io](https://codecov.io/github/ropensci/beastier/coverage.svg?branch=develop)](https://app.codecov.io/github/ropensci/beastier/branch/develop) |

`beautier` is `BEAUti` for R.

![beautier logo](reference/figures/beautier_logo.png)

beautier logo

The purpose of `beautier` is to create [a valid BEAST2 XML input
file](https://docs.ropensci.org/beautier/inst/extdata/2_4.xml) from a n
inference model. In this way, a scientific pipeline using `BEAST2` can
be fully scripted, instead of using `BEAUti`’s GUI.

`beautier` is part of the
[`babette`](https://github.com/ropensci/babette) package suite:

- [`beautier`](https://github.com/ropensci/beautier) create a BEAST2
  input (`.xml`) file from an inference model.
- [`tiebeaur`](https://github.com/richelbilderbeek/tiebeaur) creates an
  inference model from a BEAST2 input (`.xml`) file ⚠️ experimental ⚠️
- [`beastier`](https://github.com/ropensci/beastier) runs BEAST2
- [`tracerer`](https://github.com/ropensci/tracerer) allows to works
  with BEAST2 output (`.log`, `.trees`, etc) files.
- [`mauricer`](https://github.com/ropensci/mauricer) install BEAST2
  packages

Related R packages:

- [`beautier_on_windows`](https://github.com/richelbilderbeek/beautier_on_windows):
  verifies `beautier` builds on Windows
- [`lumier`](https://github.com/ropensci/lumier): Shiny app to help
  create the function call needed

## Examples

See [examples](https://docs.ropensci.org/beautier/doc/examples.md).

## Installation

`beautier` can be installed:

- Latest CRAN version: CRAN
- Latest stable version: GitHub, `main` branch
- Bleeding-edge version: GitHub, `develop` branch

### CRAN

For the latest CRAN version:

``` r

install.packages("beautier")
```

### GitHub, `main` branch

For the latest stable version:

``` r

remotes::install_github("ropensci/beautier")
```

### GitHub, `develop` branch

For the bleeding-edge version:

``` r

remotes::install_github("ropensci/beautier", ref = "develop")
```

## [FAQ](https://docs.ropensci.org/beautier/doc/faq.md)

See [FAQ](https://docs.ropensci.org/beautier/doc/faq.md).

## Supported

This works, and the interface is unlikely to change.

- 1 DNA alignment
- Site models:
  - JC69
  - HKY
  - TN93
  - GTR
- Clock models:
  - Strickt
  - Relaxed log-normal
- Tree models:
  - Yule
  - Birth-Death
  - Coalescent Bayesian Skyline
  - Coalescent Constant Population
  - Coalescent Exponential Population
- Handle missing data: simply use a dash (´-´) as a sequence in a FASTA
  file

## Experimental

This works partially, and the interface may change as well.

### Tip dating

The tip dates file is a file that needs to not have column, nor row
names. The columns need to be tab separated.

See [the example file
`G_VII_pre2003_dates_4.txt`](https://github.com/ropensci/beautier/blob/main/inst/extdata/G_VII_pre2003_dates_4.txt)
for an example, of which the first rows are shown here:

``` text
KF767106_Indonesia_1976_VII 1976
KF767104_Indonesia_1988_VII 1988
KF767105_Indonesia_1988_VII 1988
AY288998_Indonesia_1990_VII 1990
```

## Missing features/unsupported

`beautier` cannot do everything `BEAUti` can.

Here are some missing or (yet) unsupported features, some are linked to
an Issue:

- [Add offset to a
  distribution](https://github.com/ropensci/beautier/issues/130)
- Two or more DNA alignments
- Two or more site, clock or tree models
- [Two or more MRCA
  priors](https://github.com/ropensci/beautier/issues/131)
- Shared site, clock and/or tree models
- [Using an amino acid
  alignment](https://github.com/ropensci/beautier/issues/114)
- Support for hyper parameters
- Clock models
  - Relaxed exponential
  - Random local
- Tree priors
  - Calibrated Yule model
  - Coalescent Extended Bayesian Skyline
  - [Birth Death Skyline
    Serial](https://github.com/ropensci/beautier/issues/133)
- Initialization (this is a tab that is hidden by default in `BEAUti`)

## There is a feature I miss

See [CONTRIBUTING](https://docs.ropensci.org/beautier/CONTRIBUTING.md),
at `Submitting use cases`

## I want to collaborate

See [CONTRIBUTING](https://docs.ropensci.org/beautier/CONTRIBUTING.md),
at ‘Submitting code’

## I think I have found a bug

See [CONTRIBUTING](https://docs.ropensci.org/beautier/CONTRIBUTING.md),
at ‘Submitting bugs’

## There’s something else I want to say

Sure, just add an Issue. Or send an email.

## External links

- [BEAST2 GitHub](https://github.com/CompEvol/beast2)

## Files used by continuous integration scripts

| Filename | Descriptions |
|----|----|
| [`mlc_config.json`](https://docs.ropensci.org/beautier/mlc_config.json) | Configuration of the link checker, use `markdown-link-check --config mlc_config.json --quiet docs/**/*.md` to do link checking locally |
| [`.spellcheck.yml`](https://docs.ropensci.org/beautier/.spellcheck.yml) | Configuration of the spell checker, use `pyspelling -c .spellcheck.yml` to do spellcheck locally |
| [`.wordlist.txt`](https://docs.ropensci.org/beautier/.wordlist.txt) | Whitelisted words for the spell checker, use `pyspelling -c .spellcheck.yml` to do spellcheck locally |
| [`.markdownlint.jsonc`](https://docs.ropensci.org/beautier/.markdownlint.jsonc) | Configuration of the Markdown linter, use `markdownlint "**/*.md"` to do markdown linting locally. The name of this file is a default name. |
| [`.markdownlintignore`](https://docs.ropensci.org/beautier/.markdownlintignore) | Files ignored by the Markdown linter, use `markdownlint "**/*.md"` to do markdown linting locally. The name of this file is a default name. |

## References

Article about `babette`:

- Bilderbeek, Richèl JC, and Rampal S. Etienne. “`babette`: BEAUti 2,
  BEAST 2 and Tracer for R.” Methods in Ecology and Evolution (2018).
  <https://doi.org/10.1111/2041-210X.13032>

FASTA files `anthus_aco.fas` and `anthus_nd2.fas` from:

- Van Els, Paul, and Heraldo V. Norambuena. “A revision of species
  limits in Neotropical pipits Anthus based on multilocus genetic and
  vocal data.” Ibis.

FASTA file `G_VII_pre2003_msa.fas` from:

- Durr, PA; Wibowo, MH; Tabbu, CR; Asmara, W; Selleck, P; Wang, J; Broz,
  I; Graham, K.; Dimitrov, K and Afonso, C. (in preparation).
  Phylodynamics of Genotype VII Newcastle disease virus in Indonesia.
