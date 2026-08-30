# Get the number of parameters a distribution uses

Get the number of parameters a distribution uses

## Usage

``` r
get_distr_n_params(distr)
```

## Arguments

- distr:

  a distribution, as created by
  [`create_distr`](https://docs.ropensci.org/beautier/reference/create_distr.md)
  or (preferable) its named functions

## Value

the number of parameters that distribution uses

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
check_empty_beautier_folder()

get_distr_n_params(create_beta_distr())
#> [1] 2
get_distr_n_params(create_exp_distr())
#> [1] 1
get_distr_n_params(create_gamma_distr())
#> [1] 2
get_distr_n_params(create_inv_gamma_distr())
#> [1] 2
get_distr_n_params(create_laplace_distr())
#> [1] 2
get_distr_n_params(create_log_normal_distr())
#> [1] 2
get_distr_n_params(create_normal_distr())
#> [1] 2
get_distr_n_params(create_one_div_x_distr())
#> [1] 0
get_distr_n_params(create_poisson_distr())
#> [1] 1
get_distr_n_params(create_uniform_distr())
#> [1] 0

check_empty_beautier_folder()
```
