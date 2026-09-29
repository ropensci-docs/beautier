# Determine if the object is a valid inverse-gamma distribution as created by [`create_inv_gamma_distr`](https://docs.ropensci.org/beautier/reference/create_inv_gamma_distr.md)

Determine if the object is a valid inverse-gamma distribution as created
by
[`create_inv_gamma_distr`](https://docs.ropensci.org/beautier/reference/create_inv_gamma_distr.md)

## Usage

``` r
is_inv_gamma_distr(x)
```

## Arguments

- x:

  an object, to be determined if it is a valid inverse-gamma
  distribution

## Value

TRUE if x is a valid inverse-gamma distribution, FALSE otherwise

## See also

use
[`is_distr`](https://docs.ropensci.org/beautier/reference/is_distr.md)
to see if x is any distribution

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
check_empty_beautier_folder()

# TRUE
is_inv_gamma_distr(create_inv_gamma_distr())
#> [1] TRUE
# FALSE
is_inv_gamma_distr(create_laplace_distr())
#> [1] FALSE
is_inv_gamma_distr(NA)
#> [1] FALSE
is_inv_gamma_distr(NULL)
#> [1] FALSE
is_inv_gamma_distr("nonsense")
#> [1] FALSE

check_empty_beautier_folder()
```
