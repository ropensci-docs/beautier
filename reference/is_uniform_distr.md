# Determine if the object is a valid uniform distribution as created by [`create_uniform_distr`](https://docs.ropensci.org/beautier/reference/create_uniform_distr.md)

Determine if the object is a valid uniform distribution as created by
[`create_uniform_distr`](https://docs.ropensci.org/beautier/reference/create_uniform_distr.md)

## Usage

``` r
is_uniform_distr(x)
```

## Arguments

- x:

  an object, to be determined if it is a valid uniform distribution

## Value

TRUE if x is a valid uniform distribution, FALSE otherwise

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
is_uniform_distr(create_uniform_distr())
#> [1] TRUE
# FALSE
is_uniform_distr(create_beta_distr())
#> [1] FALSE
is_uniform_distr(NA)
#> [1] FALSE
is_uniform_distr(NULL)
#> [1] FALSE
is_uniform_distr("nonsense")
#> [1] FALSE

check_empty_beautier_folder()
```
