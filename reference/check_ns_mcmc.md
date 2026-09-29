# Check if this an MCMC that uses Nested Sampling to estimate a marginal likelihood.

Will [stop](https://rdrr.io/r/base/stop.html) if not, else will do
nothing

## Usage

``` r
check_ns_mcmc(mcmc)
```

## Arguments

- mcmc:

  one MCMC. Use
  [`create_mcmc`](https://docs.ropensci.org/beautier/reference/create_mcmc.md)
  to create an MCMC. Use
  [`create_ns_mcmc`](https://docs.ropensci.org/beautier/reference/create_ns_mcmc.md)
  to create an MCMC for a Nested Sampling run. Use
  [`check_mcmc`](https://docs.ropensci.org/beautier/reference/check_mcmc.md)
  to check if an MCMC is valid. Use
  [`rename_mcmc_filenames`](https://docs.ropensci.org/beautier/reference/rename_mcmc_filenames.md)
  to rename the filenames in an MCMC.

## Value

No return value, called for side effects

## See also

use
[`create_ns_mcmc`](https://docs.ropensci.org/beautier/reference/create_ns_mcmc.md)
to create an MCMC that uses Nested Sampling to estimate a marginal
likelihood

## Author

Richèl J.C. Bilderbeek
