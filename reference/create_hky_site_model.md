# Create an HKY site model

Create an HKY site model

## Usage

``` r
create_hky_site_model(
  id = NA,
  kappa = "obsolete",
  kappa_param = beautier::create_kappa_param(value = "2.0"),
  gamma_site_model = beautier::create_gamma_site_model(),
  kappa_prior_distr = beautier::create_log_normal_distr(m =
    beautier::create_m_param(value = "1.0"), s = 1.25),
  freq_equilibrium = "estimated",
  freq_param = beautier::create_freq_param()
)
```

## Arguments

- id:

  the IDs of the alignment (can be extracted from the FASTA filename
  using
  [`get_alignment_id`](https://docs.ropensci.org/beautier/reference/get_alignment_id.md))

- kappa:

  obsoleted parameter. It is the value in the \`kappa_param\` argument

- kappa_param:

  a \`kappa\` parameter, as created by
  [create_kappa_param](https://docs.ropensci.org/beautier/reference/create_kappa_param.md)

- gamma_site_model:

  a gamma site model, as created by
  [create_gamma_site_model](https://docs.ropensci.org/beautier/reference/create_gamma_site_model.md)

- kappa_prior_distr:

  the distribution of the kappa prior, which is a log-normal
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

an HKY site_model

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
if (is_on_ci()) {

  hky_site_model <- create_hky_site_model()
  output_filename <- get_beautier_tempfilename()
  create_beast2_input_file(
    input_filename = get_fasta_filename(),
    output_filename = output_filename,
    site_model = hky_site_model
  )
  file.remove(output_filename)

  remove_beautier_folder()
}
```
