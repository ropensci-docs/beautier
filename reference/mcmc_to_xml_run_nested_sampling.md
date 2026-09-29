# Converts an MCMC object to the run section's XML for a Nested-Sampling MCMC

Converts an MCMC object to the run section's XML for a Nested-Sampling
MCMC

## Usage

``` r
mcmc_to_xml_run_nested_sampling(mcmc)
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
check_empty_beautier_folder()

#  "<run id=\"mcmc\" spec=\"beast.gss.NS\" chainLength=\"1e+07\" "
#  "particleCount=\"1\" subChainLength=\"5000\" epsilon=\"1e-12\">"
mcmc_to_xml_run_nested_sampling(create_ns_mcmc())
#> [1] "<run id=\"mcmc\" spec=\"beast.gss.NS\" chainLength=\"1e+07\" particleCount=\"1\" subChainLength=\"5000\" epsilon=\"1e-12\">"

check_empty_beautier_folder()
```
