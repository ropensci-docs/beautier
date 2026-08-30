# General function to create a distribution.

General function to create a distribution.

## Usage

``` r
is_one_string_that_is_a_number(x)
```

## Arguments

- x:

  the object that may be one string that may be a number

## Value

TRUE is \`x\` is one string that is a number

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
# TRUE
is_one_string_that_is_a_number("3.14")
#> [1] TRUE

# FALSE
is_one_string_that_is_a_number(c("3.14", "42"))
#> [1] FALSE
is_one_string_that_is_a_number("")
#> [1] FALSE
is_one_string_that_is_a_number(42)
#> [1] FALSE
is_one_string_that_is_a_number("nonsense")
#> [1] FALSE
```
