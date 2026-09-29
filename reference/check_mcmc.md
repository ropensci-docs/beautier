# Check if the MCMC is a valid MCMC object.

Calls `stop` if the MCMC is invalid

## Usage

``` r
check_mcmc(mcmc)
```

## Arguments

- mcmc:

  one MCMC. Use
  [`create_mcmc`](https://docs.ropensci.org/beautier/reference/create_mcmc.md)
  to create an MCMC. Use
  [`create_ns_mcmc`](https://docs.ropensci.org/beautier/reference/create_ns_mcmc.md)
  to create an MCMC for a Nested Sampling run. Use `check_mcmc` to check
  if an MCMC is valid. Use
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

## Examples

``` r
check_empty_beautier_folder()

check_mcmc(create_mcmc())

check_empty_beautier_folder()
```
