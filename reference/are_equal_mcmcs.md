# Determine if two MCMCs are equal.

Will [stop](https://rdrr.io/r/base/stop.html) if the arguments are not
MCMCs.

## Usage

``` r
are_equal_mcmcs(mcmc_1, mcmc_2)
```

## Arguments

- mcmc_1:

  an MCMC, as created by
  [`create_mcmc`](https://docs.ropensci.org/beautier/reference/create_mcmc.md)

- mcmc_2:

  an MCMC, as created by
  [`create_mcmc`](https://docs.ropensci.org/beautier/reference/create_mcmc.md)

## Value

TRUE if the two MCMCs are equal

## See also

Use
[`create_mcmc`](https://docs.ropensci.org/beautier/reference/create_mcmc.md)
to create an MCMC

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
if (is_on_ci()) {

  check_empty_beautier_folder()

  mcmc_1 <- create_mcmc(chain_length = 1000)
  mcmc_2 <- create_mcmc(chain_length = 314)
  # TRUE
  are_equal_mcmcs(mcmc_1, mcmc_1)
  # FALSE
  are_equal_mcmcs(mcmc_1, mcmc_2)

  check_empty_beautier_folder()
}
```
