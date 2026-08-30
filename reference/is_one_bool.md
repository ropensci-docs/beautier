# Check if the argument is one boolean

Check if the argument is one boolean

## Usage

``` r
is_one_bool(x)
```

## Arguments

- x:

  the argument to be tested to be boolean

## Value

TRUE if the argument is one boolean, FALSE otherwise

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
check_empty_beautier_folder()

# TRUE
is_one_bool(TRUE)
#> [1] TRUE
is_one_bool(FALSE)
#> [1] TRUE

# FALSE
is_one_bool(NULL)
#> [1] FALSE
is_one_bool(NA)
#> [1] FALSE
is_one_bool(c())
#> [1] FALSE
is_one_bool("nonsense")
#> [1] FALSE
is_one_bool(is_one_bool)
#> [1] FALSE
is_one_bool(c(TRUE, FALSE))
#> [1] FALSE

check_empty_beautier_folder()
```
