# Check if the MCMC has the list elements with valid values for being a valid MCMC object.

Calls `stop` if a value is invalid

## Usage

``` r
check_mcmc_values(mcmc)
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

nothing

## See also

Use
[`create_mcmc`](https://docs.ropensci.org/beautier/reference/create_mcmc.md)
to create a valid MCMC

## Author

Richèl J.C. Bilderbeek
