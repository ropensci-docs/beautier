# Create a testing inference model.

Creates a simple inference model with a short MCMC chain, to be used in
testing.

## Usage

``` r
create_test_inference_model(
  site_model = beautier::create_jc69_site_model(),
  clock_model = beautier::create_strict_clock_model(),
  tree_prior = beautier::create_yule_tree_prior(),
  mrca_prior = NA,
  mcmc = beautier::create_test_mcmc(),
  beauti_options = beautier::create_beauti_options(),
  tipdates_filename = NA
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

- mrca_prior:

  a Most Recent Common Ancestor prior, as returned by
  [`create_mrca_prior`](https://docs.ropensci.org/beautier/reference/create_mrca_prior.md)

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

- beauti_options:

  one BEAUti options object, as returned by
  [`create_beauti_options`](https://docs.ropensci.org/beautier/reference/create_beauti_options.md)

- tipdates_filename:

  name of the file containing the tip dates. This file is assumed to
  have two columns, separated by a tab. The first column contains the
  taxa names, the second column contains the date.

## Value

an inference model

## See also

Use
[create_inference_model](https://docs.ropensci.org/beautier/reference/create_inference_model.md)
to create a regular inference model. Use
[create_test_ns_inference_model](https://docs.ropensci.org/beautier/reference/create_test_ns_inference_model.md)
to create an inference model to estimate the marginal likelihood with a
short MCMC, to be used in testing

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
if (is_on_ci()) {
  check_empty_beautier_folder()

  inference_model <- create_test_inference_model()

  beast2_input_file <- get_beautier_tempfilename()
  create_beast2_input_file_from_model(
    get_fasta_filename(),
    beast2_input_file,
    inference_model = inference_model
  )
  file.remove(beast2_input_file)

  remove_beautier_folder()
  check_empty_beautier_folder()
}
```
