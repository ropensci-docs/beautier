# Create a GTR site model

Create a GTR site model

## Usage

``` r
create_gtr_site_model(
  id = NA,
  gamma_site_model = beautier::create_gamma_site_model(),
  rate_ac_prior_distr = beautier::create_gamma_distr(alpha = 0.05, beta =
    beautier::create_beta_param(value = "10.0")),
  rate_ag_prior_distr = beautier::create_gamma_distr(alpha = 0.05, beta =
    beautier::create_beta_param(value = "20.0")),
  rate_at_prior_distr = beautier::create_gamma_distr(alpha = 0.05, beta =
    beautier::create_beta_param(value = "10.0")),
  rate_cg_prior_distr = beautier::create_gamma_distr(alpha = 0.05, beta =
    beautier::create_beta_param(value = "10.0")),
  rate_gt_prior_distr = beautier::create_gamma_distr(alpha = 0.05, beta =
    beautier::create_beta_param(value = "10.0")),
  rate_ac_param = beautier::create_rate_ac_param(),
  rate_ag_param = beautier::create_rate_ag_param(),
  rate_at_param = beautier::create_rate_at_param(),
  rate_cg_param = beautier::create_rate_cg_param(),
  rate_ct_param = beautier::create_rate_ct_param(),
  rate_gt_param = beautier::create_rate_gt_param(),
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

- rate_ac_prior_distr:

  the AC rate prior distribution, as returned by
  [`create_distr`](https://docs.ropensci.org/beautier/reference/create_distr.md)

- rate_ag_prior_distr:

  the AG rate prior distribution, as returned by
  [`create_distr`](https://docs.ropensci.org/beautier/reference/create_distr.md)

- rate_at_prior_distr:

  the AT rate prior distribution, as returned by
  [`create_distr`](https://docs.ropensci.org/beautier/reference/create_distr.md)

- rate_cg_prior_distr:

  the CG rate prior distribution, as returned by
  [`create_distr`](https://docs.ropensci.org/beautier/reference/create_distr.md)

- rate_gt_prior_distr:

  the GT rate prior distribution, as returned by
  [`create_distr`](https://docs.ropensci.org/beautier/reference/create_distr.md)

- rate_ac_param:

  the 'rate AC' parameter, a numeric value. For advanced usage, use the
  structure as returned by
  [`create_rate_ac_param`](https://docs.ropensci.org/beautier/reference/create_rate_ac_param.md)

- rate_ag_param:

  the 'rate AG' parameter, a numeric value. For advanced usage, use the
  structure as returned by
  [`create_rate_ag_param`](https://docs.ropensci.org/beautier/reference/create_rate_ag_param.md)

- rate_at_param:

  the 'rate AT' parameter, a numeric value. For advanced usage, use the
  structure as returned by
  [`create_rate_at_param`](https://docs.ropensci.org/beautier/reference/create_rate_at_param.md)

- rate_cg_param:

  the 'rate CG' parameter, a numeric value. For advanced usage, use the
  structure as returned by
  [`create_rate_cg_param`](https://docs.ropensci.org/beautier/reference/create_rate_cg_param.md)

- rate_ct_param:

  the 'rate CT' parameter, a numeric value. For advanced usage, use the
  structure as returned by
  [`create_rate_ct_param`](https://docs.ropensci.org/beautier/reference/create_rate_ct_param.md)

- rate_gt_param:

  the 'rate GT' parameter, a numeric value. For advanced usage, use the
  structure as returned by
  [`create_rate_gt_param`](https://docs.ropensci.org/beautier/reference/create_rate_gt_param.md)

- freq_equilibrium:

  the frequency in which the rates are at equilibrium are either
  `estimated`, `empirical` or `all_equal`. `get_freq_equilibrium_names`
  returns the possible values for `freq_equilibrium`

- freq_param:

  a \`freq\` parameter, as created by
  [create_freq_param](https://docs.ropensci.org/beautier/reference/create_freq_param.md)

## Value

a GTR site_model

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
if (is_on_ci()) {

  gtr_site_model <- create_gtr_site_model(
    rate_ac_param = 1.2,
    rate_ag_param = 2.3,
    rate_at_param = 3.4,
    rate_cg_param = 4.5,
    rate_ct_param = 5.6,
    rate_gt_param = 6.7
  )

  beast2_input_file <- get_beautier_tempfilename()
  create_beast2_input_file(
    input_filename = get_fasta_filename(),
    beast2_input_file,
    site_model = gtr_site_model
  )
  file.remove(beast2_input_file)

  remove_beautier_folder()
}
```
