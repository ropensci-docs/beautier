# Determine if the MCMC is a default MCMC

Determine if the MCMC is a default MCMC

## Usage

``` r
is_default_mcmc(mcmc)
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

TRUE if the MCMC is a default MCMC

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
if (is_on_ci()) {

  check_empty_beautier_folder()

  # TRUE: An MCMC created by 'create_mcmc' is default.
  is_default_mcmc(create_mcmc())

  # FALSE: An MCMC created by 'create_ns_mcmc' is not
  is_default_mcmc(create_ns_mcmc())

  check_empty_beautier_folder()
}
```
