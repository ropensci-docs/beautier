# Determines if the argument is a double

Determines if the argument is a double

## Usage

``` r
is_one_double(x)
```

## Arguments

- x:

  the object to be determined of if it is one double

## Value

TRUE if the argument is one floating point value, FALSE otherwise

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
check_empty_beautier_folder()

# TRUE
is_one_double(314)
#> [1] TRUE
is_one_double(0)
#> [1] TRUE
is_one_double(-314)
#> [1] TRUE
is_one_double(3.14)
#> [1] TRUE

# FALSE
is_one_double(NULL)
#> [1] FALSE
is_one_double(NA)
#> [1] FALSE
is_one_double(Inf)
#> [1] FALSE
is_one_double("nonsense")
#> [1] FALSE
is_one_double(c())
#> [1] FALSE
is_one_double(c(1, 2))
#> [1] FALSE

check_empty_beautier_folder()
```
