# Determine if the object is a valid `beauti_options`

Determine if the object is a valid `beauti_options`

## Usage

``` r
is_beauti_options(x)
```

## Arguments

- x:

  an object, to be determined if it is a `beauti_options`

## Value

[TRUE](https://rdrr.io/r/base/logical.html) if the object is a valid
`beauti_options`, [FALSE](https://rdrr.io/r/base/logical.html) otherwise

## See also

use
[create_beauti_options](https://docs.ropensci.org/beautier/reference/create_beauti_options.md)
to create a valid `beauti_options` object

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
check_empty_beautier_folder()

# TRUE
is_beauti_options(create_beauti_options())
#> [1] TRUE

# FALSE
is_beauti_options("nonsense")
#> [1] FALSE
is_beauti_options(NA)
#> [1] FALSE
is_beauti_options(NULL)
#> [1] FALSE
is_beauti_options("")
#> [1] FALSE
is_beauti_options(c())
#> [1] FALSE

check_empty_beautier_folder()
```
