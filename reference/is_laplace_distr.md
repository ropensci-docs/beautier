# Determine if the object is a valid Laplace distribution, as created by [`create_laplace_distr`](https://docs.ropensci.org/beautier/reference/create_laplace_distr.md)

Determine if the object is a valid Laplace distribution, as created by
[`create_laplace_distr`](https://docs.ropensci.org/beautier/reference/create_laplace_distr.md)

## Usage

``` r
is_laplace_distr(x)
```

## Arguments

- x:

  an object, to be determined if it is a valid Laplace distribution

## Value

TRUE if x is a valid Laplace distribution, FALSE otherwise

## See also

use
[`is_distr`](https://docs.ropensci.org/beautier/reference/is_distr.md)
to see if x is any distribution

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
# TRUE
is_laplace_distr(create_laplace_distr())
#> [1] TRUE
# FALSE
is_laplace_distr(create_log_normal_distr())
#> [1] FALSE
is_laplace_distr(NA)
#> [1] FALSE
is_laplace_distr(NULL)
#> [1] FALSE
is_laplace_distr("nonsense")
#> [1] FALSE
```
