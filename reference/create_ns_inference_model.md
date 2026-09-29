# Create an inference model to measure the evidence of.

Create an inference model to measure the evidence of. To do so, the
inference model is created as usual (see
[create_inference_model](https://docs.ropensci.org/beautier/reference/create_inference_model.md)),
except for using a Nested Sampling MCMC (see
[create_ns_mcmc](https://docs.ropensci.org/beautier/reference/create_ns_mcmc.md))

## Usage

``` r
create_ns_inference_model(
  site_model = beautier::create_jc69_site_model(),
  clock_model = beautier::create_strict_clock_model(),
  tree_prior = beautier::create_yule_tree_prior(),
  mcmc = beautier::create_ns_mcmc()
)
```

## Arguments

- site_model:

  a site model, as returned by
  [`create_site_model`](https://docs.ropensci.org/beautier/reference/create_site_model.md)

- clock_model:

  a clock model, as returned by
  [`create_clock_model`](https://docs.ropensci.org/beautier/reference/create_clock_model.md)

- tree_prior:

  a tree priors, as returned by
  [`create_tree_prior`](https://docs.ropensci.org/beautier/reference/create_tree_prior.md)

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

an inference model

## See also

Use
[create_inference_model](https://docs.ropensci.org/beautier/reference/create_inference_model.md)
to create a regular inference model. Use
[create_test_ns_inference_model](https://docs.ropensci.org/beautier/reference/create_test_ns_inference_model.md)
to create an inference model to estimate the marginal likelihood with a
short MCMC, to be used in testing.

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
check_empty_beautier_folder()

inference_model <- create_ns_inference_model()

check_empty_beautier_folder()
```
