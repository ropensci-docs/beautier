# Determines if the argument is one string

Determines if the argument is one string

## Usage

``` r
is_one_string(x)
```

## Arguments

- x:

  the object to be determined of if it is one string

## Value

TRUE if the argument is one string, FALSE otherwise

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
check_empty_beautier_folder()

# TRUE
is_one_string("This is one string")
#> [1] TRUE

# FALSE
is_one_string(NULL)
#> [1] FALSE
is_one_string(NA)
#> [1] FALSE
is_one_string(Inf)
#> [1] FALSE
is_one_string(314)
#> [1] FALSE
is_one_string(0)
#> [1] FALSE
is_one_string(-314)
#> [1] FALSE
is_one_string(3.14)
#> [1] FALSE
is_one_string(c("a", "b"))
#> [1] FALSE
is_one_string(is_one_string)
#> [1] FALSE
is_one_string(c())
#> [1] FALSE
is_one_string(c(1, 2))
#> [1] FALSE

check_empty_beautier_folder()
```
