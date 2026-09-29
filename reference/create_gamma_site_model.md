# Create a gamma site model, part of a site model

Create a gamma site model, part of a site model

## Usage

``` r
create_gamma_site_model(
  gamma_cat_count = "0",
  gamma_shape = "1.0",
  prop_invariant = "0.0",
  gamma_shape_prior_distr = NA,
  freq_equilibrium = "estimated",
  freq_prior_uniform_distr_id = 1000
)
```

## Arguments

- gamma_cat_count:

  the number of gamma categories, must be an integer with value zero or
  more

- gamma_shape:

  gamma curve shape parameter

- prop_invariant:

  the proportion invariant, must be a value from 0.0 to 1.0

- gamma_shape_prior_distr:

  the distribution of the gamma shape prior. `gamma_shape_prior_distr`
  must be `NA` for a `gamma_cat_count` of zero or one. For a
  `gamma_cat_count` of two or more, leaving `gamma_shape_prior_distr`
  equal to its default value of `NA`, a default distribution is used.
  Else `gamma_shape_prior_distr` must be a distribution, as can be
  created by
  [`create_distr`](https://docs.ropensci.org/beautier/reference/create_distr.md)

- freq_equilibrium:

  the frequency in which the rates are at equilibrium are either
  `estimated`, `empirical` or `all_equal`. `get_freq_equilibrium_names`
  returns the possible values for `freq_equilibrium`

- freq_prior_uniform_distr_id:

  the ID of the \`FrequenciesPrior\`'s uniform distribution

## Value

a gamma site model

## See also

Use `create_gamma_site_model` to create a gamma site model

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
if (is_on_ci()) {

  gamma_site_model <- create_gamma_site_model(prop_invariant = 0.5)

  site_model <- create_hky_site_model(gamma_site_model = gamma_site_model)

  beast2_input_file <- get_beautier_tempfilename()
  create_beast2_input_file(
    get_fasta_filename(),
    beast2_input_file,
    site_model = site_model
  )
  file.remove(beast2_input_file)

  remove_beautier_folder()
}
```
