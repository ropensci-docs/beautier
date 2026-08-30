# Determine if the object is a valid distribution

Determine if the object is a valid distribution

## Usage

``` r
is_distr(x)
```

## Arguments

- x:

  an object, to be determined if it is a valid distribution

## Value

TRUE if x is a valid distribution, FALSE otherwise

## See also

use
[`is_beta_distr`](https://docs.ropensci.org/beautier/reference/is_beta_distr.md),
[`is_exp_distr`](https://docs.ropensci.org/beautier/reference/is_exp_distr.md),
[`is_gamma_distr`](https://docs.ropensci.org/beautier/reference/is_gamma_distr.md),
[`is_inv_gamma_distr`](https://docs.ropensci.org/beautier/reference/is_inv_gamma_distr.md),
[`is_laplace_distr`](https://docs.ropensci.org/beautier/reference/is_laplace_distr.md),
[`is_log_normal_distr`](https://docs.ropensci.org/beautier/reference/is_log_normal_distr.md),
[`is_normal_distr`](https://docs.ropensci.org/beautier/reference/is_normal_distr.md),
[`is_one_div_x_distr`](https://docs.ropensci.org/beautier/reference/is_one_div_x_distr.md),
[`is_poisson_distr`](https://docs.ropensci.org/beautier/reference/is_poisson_distr.md),
or
[`is_uniform_distr`](https://docs.ropensci.org/beautier/reference/is_uniform_distr.md),
to check for more specific distribution

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
check_empty_beautier_folder()

# TRUE
is_distr(create_beta_distr())
#> [1] TRUE
is_distr(create_exp_distr())
#> [1] TRUE
is_distr(create_gamma_distr())
#> [1] TRUE
is_distr(create_inv_gamma_distr())
#> [1] TRUE
is_distr(create_laplace_distr())
#> [1] TRUE
is_distr(create_log_normal_distr())
#> [1] TRUE
is_distr(create_normal_distr())
#> [1] TRUE
is_distr(create_one_div_x_distr())
#> [1] TRUE
is_distr(create_poisson_distr())
#> [1] TRUE
is_distr(create_uniform_distr())
#> [1] TRUE

# FALSE
is_distr(NA)
#> [1] FALSE
is_distr(NULL)
#> [1] FALSE
is_distr("nonsense")
#> [1] FALSE

check_empty_beautier_folder()
```
