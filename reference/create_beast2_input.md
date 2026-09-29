# Create a BEAST2 XML input text

Create a BEAST2 XML input text

## Usage

``` r
create_beast2_input(
  input_filename,
  tipdates_filename = NA,
  site_model = beautier::create_jc69_site_model(),
  clock_model = beautier::create_strict_clock_model(),
  tree_prior = beautier::create_yule_tree_prior(),
  mrca_prior = NA,
  mcmc = beautier::create_mcmc(),
  beauti_options = beautier::create_beauti_options()
)
```

## Arguments

- input_filename:

  A FASTA filename. Use
  [`get_fasta_filename`](https://docs.ropensci.org/beautier/reference/get_fasta_filename.md)
  to obtain a testing FASTA filename.

- tipdates_filename:

  name of the file containing the tip dates. This file is assumed to
  have two columns, separated by a tab. The first column contains the
  taxa names, the second column contains the date.

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

## Value

a character vector of XML strings

## See also

Use
[create_beast2_input_from_model](https://docs.ropensci.org/beautier/reference/create_beast2_input_from_model.md)
to create the BEAST2 XML input text from an inference model Use
[create_beast2_input_file](https://docs.ropensci.org/beautier/reference/create_beast2_input_file.md)
to also save it to file.

[`create_beast2_input_file`](https://docs.ropensci.org/beautier/reference/create_beast2_input_file.md)
shows more examples

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
if (is_on_ci()) {
  create_beast2_input(
    input_filename = get_fasta_filename()
  )
}
```
