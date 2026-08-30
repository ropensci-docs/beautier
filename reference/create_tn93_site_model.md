# Create a TN93 site model

Create a TN93 site model

## Usage

``` r
create_tn93_site_model(
  id = NA,
  gamma_site_model = beautier::create_gamma_site_model(),
  kappa_1_param = beautier::create_kappa_1_param(),
  kappa_2_param = beautier::create_kappa_2_param(),
  kappa_1_prior_distr = beautier::create_log_normal_distr(m = 1, s = 1.25),
  kappa_2_prior_distr = beautier::create_log_normal_distr(m = 1, s = 1.25),
  freq_equilibrium = "estimated",
  freq_param = beautier::create_freq_param()
)
```

## Arguments

- id:

  the IDs of the alignment (can be extracted from the FASTA filename
  using
  [`get_alignment_id`](https://docs.ropensci.org/beautier/reference/get_alignment_id.md))

- gamma_site_model:

  a gamma site model, as created by
  [create_gamma_site_model](https://docs.ropensci.org/beautier/reference/create_gamma_site_model.md)

- kappa_1_param:

  the 'kappa 1' parameter, a numeric value. For advanced usage, use the
  structure as returned by
  [`create_kappa_1_param`](https://docs.ropensci.org/beautier/reference/create_kappa_1_param.md)

- kappa_2_param:

  the 'kappa 2' parameter, a numeric value. For advanced usage, use the
  structure as returned by
  [`create_kappa_2_param`](https://docs.ropensci.org/beautier/reference/create_kappa_2_param.md)

- kappa_1_prior_distr:

  the distribution of the kappa 1 prior, which is a log-normal
  distribution (as created by
  [`create_log_normal_distr`](https://docs.ropensci.org/beautier/reference/create_log_normal_distr.md))
  by default

- kappa_2_prior_distr:

  the distribution of the kappa 2 prior, which is a log-normal
  distribution (as created by
  [`create_log_normal_distr`](https://docs.ropensci.org/beautier/reference/create_log_normal_distr.md))
  by default

- freq_equilibrium:

  the frequency in which the rates are at equilibrium are either
  `estimated`, `empirical` or `all_equal`. `get_freq_equilibrium_names`
  returns the possible values for `freq_equilibrium`

- freq_param:

  a \`freq\` parameter, as created by
  [create_freq_param](https://docs.ropensci.org/beautier/reference/create_freq_param.md)

## Value

a TN93 site_model

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
if (is_on_ci()) {

  tn93_site_model <- create_tn93_site_model(
    kappa_1_param = 2.0,
    kappa_2_param = 2.0
  )

  output_filename <- get_beautier_tempfilename()
  create_beast2_input_file(
    input_filename = get_fasta_filename(),
    output_filename = output_filename,
    site_model = tn93_site_model
  )
  file.remove(output_filename)

  remove_beautier_folder()
}
```
