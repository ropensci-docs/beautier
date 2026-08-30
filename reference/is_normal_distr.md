# Determine if the object is a valid normal distribution as created by [`create_normal_distr`](https://docs.ropensci.org/beautier/reference/create_normal_distr.md)

Determine if the object is a valid normal distribution as created by
[`create_normal_distr`](https://docs.ropensci.org/beautier/reference/create_normal_distr.md)

## Usage

``` r
is_normal_distr(x)
```

## Arguments

- x:

  an object, to be determined if it is a valid normal distribution

## Value

TRUE if x is a valid normal distribution, FALSE otherwise

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
is_normal_distr(create_normal_distr())
#> [1] TRUE
# FALSE
is_normal_distr(create_one_div_x_distr())
#> [1] FALSE
is_normal_distr(NA)
#> [1] FALSE
is_normal_distr(NULL)
#> [1] FALSE
is_normal_distr("nonsense")
#> [1] FALSE

check_empty_beautier_folder()
```
