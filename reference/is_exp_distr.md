# Determine if the object is a valid exponential distribution as created by [`create_exp_distr`](https://docs.ropensci.org/beautier/reference/create_exp_distr.md)

Determine if the object is a valid exponential distribution as created
by
[`create_exp_distr`](https://docs.ropensci.org/beautier/reference/create_exp_distr.md)

## Usage

``` r
is_exp_distr(x)
```

## Arguments

- x:

  an object, to be determined if it is a valid exponential distribution

## Value

TRUE if x is a valid exponential distribution, FALSE otherwise

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
is_exp_distr(create_exp_distr())
#> [1] TRUE
# FALSE
is_exp_distr(create_gamma_distr())
#> [1] FALSE
is_exp_distr(NA)
#> [1] FALSE
is_exp_distr(NULL)
#> [1] FALSE
is_exp_distr("nonsense")
#> [1] FALSE

check_empty_beautier_folder()
```
