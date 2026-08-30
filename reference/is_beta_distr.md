# Determine if the object is a valid beta distribution, as created by [`create_beta_distr`](https://docs.ropensci.org/beautier/reference/create_beta_distr.md)

Determine if the object is a valid beta distribution, as created by
[`create_beta_distr`](https://docs.ropensci.org/beautier/reference/create_beta_distr.md)

## Usage

``` r
is_beta_distr(x)
```

## Arguments

- x:

  an object, to be determined if it is a valid beta distribution,

## Value

TRUE if x is a valid beta distribution, FALSE otherwise

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
is_beta_distr(create_beta_distr())
#> [1] TRUE
# FALSE
is_beta_distr(create_exp_distr())
#> [1] FALSE
is_beta_distr(NA)
#> [1] FALSE
is_beta_distr(NULL)
#> [1] FALSE
is_beta_distr("nonsense")
#> [1] FALSE

check_empty_beautier_folder()
```
