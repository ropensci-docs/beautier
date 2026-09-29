# Determine if the object is a valid 1/x distribution, as created by [`create_one_div_x_distr`](https://docs.ropensci.org/beautier/reference/create_one_div_x_distr.md)

Determine if the object is a valid 1/x distribution, as created by
[`create_one_div_x_distr`](https://docs.ropensci.org/beautier/reference/create_one_div_x_distr.md)

## Usage

``` r
is_one_div_x_distr(x)
```

## Arguments

- x:

  an object, to be determined if it is a valid 1/x distribution

## Value

TRUE if x is a valid 1/x distribution, FALSE otherwise

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
is_one_div_x_distr(create_one_div_x_distr())
#> [1] TRUE
# FALSE
is_one_div_x_distr(create_poisson_distr())
#> [1] FALSE
is_one_div_x_distr(NA)
#> [1] FALSE
is_one_div_x_distr(NULL)
#> [1] FALSE
is_one_div_x_distr("nonsense")
#> [1] FALSE

check_empty_beautier_folder()
```
