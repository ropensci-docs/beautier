# Determine if an object is one empty string

Determine if an object is one empty string

## Usage

``` r
is_one_empty_string(x)
```

## Arguments

- x:

  the object that may be one string that may be empty

## Value

TRUE is \`x\` is one string that is empty

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
# TRUE
is_one_empty_string("")
#> [1] TRUE

# FALSE
is_one_empty_string("3.14")
#> [1] FALSE
is_one_empty_string(c("", ""))
#> [1] FALSE
is_one_empty_string(42)
#> [1] FALSE
is_one_empty_string("nonsense")
#> [1] FALSE
```
