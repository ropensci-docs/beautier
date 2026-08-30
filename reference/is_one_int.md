# Determines if the argument is a whole number

Determines if the argument is a whole number

## Usage

``` r
is_one_int(x, tolerance = .Machine$double.eps^0.5)
```

## Arguments

- x:

  the object to be determined of if it is one integer

- tolerance:

  tolerance to rounding errors

## Value

TRUE if the argument is one int, FALSE otherwise

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
check_empty_beautier_folder()

# TRUE
is_one_int(314)
#> [1] TRUE
is_one_int(0)
#> [1] TRUE
is_one_int(-314)
#> [1] TRUE
# FALSE
is_one_int(3.14)
#> [1] FALSE
is_one_int(NULL)
#> [1] FALSE
is_one_int(NA)
#> [1] FALSE
is_one_int(Inf)
#> [1] FALSE
is_one_int("nonsense")
#> [1] FALSE
is_one_int(c())
#> [1] FALSE
is_one_int(c(1, 2))
#> [1] FALSE

check_empty_beautier_folder()
```
