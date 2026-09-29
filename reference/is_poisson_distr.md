# Determine if the object is a valid Poisson distribution as created by [`create_poisson_distr`](https://docs.ropensci.org/beautier/reference/create_poisson_distr.md)

Determine if the object is a valid Poisson distribution as created by
[`create_poisson_distr`](https://docs.ropensci.org/beautier/reference/create_poisson_distr.md)

## Usage

``` r
is_poisson_distr(x)
```

## Arguments

- x:

  an object, to be determined if it is a valid Poisson distribution

## Value

TRUE if x is a valid Poisson distribution, FALSE otherwise

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
is_poisson_distr(create_poisson_distr())
#> [1] TRUE
# FALSE
is_poisson_distr(create_uniform_distr())
#> [1] FALSE
is_distr(NA)
#> [1] FALSE
is_distr(NULL)
#> [1] FALSE
is_distr("nonsense")
#> [1] FALSE

check_empty_beautier_folder()
```
