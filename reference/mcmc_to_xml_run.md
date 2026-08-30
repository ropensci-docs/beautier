# Converts an MCMC object to the run section's XML

Converts an MCMC object to the run section's XML

## Usage

``` r
mcmc_to_xml_run(mcmc)
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

the XML as text

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
if (is_on_ci()) {

  check_empty_beautier_folder()

  # <run id=\"mcmc\" spec=\"MCMC\" chainLength=\"1e+07\">
  mcmc_to_xml_run(create_mcmc())

  check_empty_beautier_folder()
}
```
