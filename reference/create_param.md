# General function to create a parameter.

General function to create a parameter.

## Usage

``` r
create_param(name, id, value, ...)
```

## Arguments

- name:

  the parameters' name. Valid names can be found in `get_param_names`

- id:

  the parameter's ID

- value:

  value of the parameter

- ...:

  specific parameter parameters

## Value

a parameter

## Note

Prefer using the named functions
[`create_alpha_param`](https://docs.ropensci.org/beautier/reference/create_alpha_param.md),
[`create_beta_param`](https://docs.ropensci.org/beautier/reference/create_beta_param.md),
[`create_clock_rate_param`](https://docs.ropensci.org/beautier/reference/create_clock_rate_param.md),
[`create_kappa_1_param`](https://docs.ropensci.org/beautier/reference/create_kappa_1_param.md),
[`create_kappa_2_param`](https://docs.ropensci.org/beautier/reference/create_kappa_2_param.md),
[`create_lambda_param`](https://docs.ropensci.org/beautier/reference/create_lambda_param.md),
[`create_m_param`](https://docs.ropensci.org/beautier/reference/create_m_param.md),
[`create_mean_param`](https://docs.ropensci.org/beautier/reference/create_mean_param.md),
[`create_mu_param`](https://docs.ropensci.org/beautier/reference/create_mu_param.md),
[`create_rate_ac_param`](https://docs.ropensci.org/beautier/reference/create_rate_ac_param.md),
[`create_rate_ag_param`](https://docs.ropensci.org/beautier/reference/create_rate_ag_param.md),
[`create_rate_at_param`](https://docs.ropensci.org/beautier/reference/create_rate_at_param.md),
[`create_rate_cg_param`](https://docs.ropensci.org/beautier/reference/create_rate_cg_param.md),
[`create_rate_ct_param`](https://docs.ropensci.org/beautier/reference/create_rate_ct_param.md),
[`create_rate_gt_param`](https://docs.ropensci.org/beautier/reference/create_rate_gt_param.md),
[`create_s_param`](https://docs.ropensci.org/beautier/reference/create_s_param.md),
[`create_scale_param`](https://docs.ropensci.org/beautier/reference/create_scale_param.md),
and
[`create_sigma_param`](https://docs.ropensci.org/beautier/reference/create_sigma_param.md)

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
if (is_on_ci()) {

  # Create an alpha parameter
  alpha_param <- create_alpha_param()

  # Use the parameter in a distribution
  beta_distr <- create_beta_distr(
    alpha = alpha_param
  )

  # Use the distribution to create a BEAST2 input file
  beast2_input_file <- get_beautier_tempfilename()
  create_beast2_input_file(
    input_filename = get_fasta_filename(),
    beast2_input_file,
    tree_prior = create_yule_tree_prior(
      birth_rate_distr = beta_distr
    )
  )
  file.remove(beast2_input_file)

  remove_beautier_folder()
}
```
