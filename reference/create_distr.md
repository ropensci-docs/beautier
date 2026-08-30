# General function to create a distribution.

General function to create a distribution.

## Usage

``` r
create_distr(name, id, value = NA, lower = NA, upper = NA, ...)
```

## Arguments

- name:

  the distribution name. Valid names can be found in `get_distr_names`

- id:

  the distribution's ID

- value:

  the initial value for the MCMC

- lower:

  the lower bound, the lowest possible value

- upper:

  an upper limit of the uniform distribution. If the upper limits needs
  to be infinity, set `upper` to `Inf`.

- ...:

  specific distribution parameters

## Value

a distribution

## Note

Prefer using the named functions
[`create_beta_distr`](https://docs.ropensci.org/beautier/reference/create_beta_distr.md),
[`create_exp_distr`](https://docs.ropensci.org/beautier/reference/create_exp_distr.md),
[`create_gamma_distr`](https://docs.ropensci.org/beautier/reference/create_gamma_distr.md),
[`create_inv_gamma_distr`](https://docs.ropensci.org/beautier/reference/create_inv_gamma_distr.md),
[`create_laplace_distr`](https://docs.ropensci.org/beautier/reference/create_laplace_distr.md),
[`create_log_normal_distr`](https://docs.ropensci.org/beautier/reference/create_log_normal_distr.md),
[`create_normal_distr`](https://docs.ropensci.org/beautier/reference/create_normal_distr.md),
[`create_one_div_x_distr`](https://docs.ropensci.org/beautier/reference/create_one_div_x_distr.md),
[`create_poisson_distr`](https://docs.ropensci.org/beautier/reference/create_poisson_distr.md)
and
[`create_uniform_distr`](https://docs.ropensci.org/beautier/reference/create_uniform_distr.md)

See
[`create_beta_distr`](https://docs.ropensci.org/beautier/reference/create_beta_distr.md),
[`create_exp_distr`](https://docs.ropensci.org/beautier/reference/create_exp_distr.md),
[`create_gamma_distr`](https://docs.ropensci.org/beautier/reference/create_gamma_distr.md),
[`create_inv_gamma_distr`](https://docs.ropensci.org/beautier/reference/create_inv_gamma_distr.md),
[`create_laplace_distr`](https://docs.ropensci.org/beautier/reference/create_laplace_distr.md),
[`create_log_normal_distr`](https://docs.ropensci.org/beautier/reference/create_log_normal_distr.md),
[`create_normal_distr`](https://docs.ropensci.org/beautier/reference/create_normal_distr.md),
[`create_one_div_x_distr`](https://docs.ropensci.org/beautier/reference/create_one_div_x_distr.md),
[`create_poisson_distr`](https://docs.ropensci.org/beautier/reference/create_poisson_distr.md)
and
[`create_uniform_distr`](https://docs.ropensci.org/beautier/reference/create_uniform_distr.md)
for examples how to use those distributions

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
if (is_on_ci()) {

  # Use any distribution
  distr <- create_beta_distr()

  beast2_input_file <- get_beautier_tempfilename()
  create_beast2_input_file(
    input_filename = get_fasta_filename(),
    beast2_input_file,
    tree_prior = create_yule_tree_prior(
      birth_rate_distr = distr
    )
  )
  file.remove(beast2_input_file)

  remove_beautier_folder()
}
```
