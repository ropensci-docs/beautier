# Creates all supported clock models, which is a list of the types returned by [`create_rln_clock_model`](https://docs.ropensci.org/beautier/reference/create_rln_clock_model.md), and [`create_strict_clock_model`](https://docs.ropensci.org/beautier/reference/create_strict_clock_model.md)

Creates all supported clock models, which is a list of the types
returned by
[`create_rln_clock_model`](https://docs.ropensci.org/beautier/reference/create_rln_clock_model.md),
and
[`create_strict_clock_model`](https://docs.ropensci.org/beautier/reference/create_strict_clock_model.md)

## Usage

``` r
create_clock_models()
```

## Value

a list of site_models

## See also

Use
[create_clock_model](https://docs.ropensci.org/beautier/reference/create_clock_model.md)
to create a clock model

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
check_empty_beautier_folder()

clock_models <- create_clock_models()
is_rln_clock_model(clock_models[[1]])
#> [1] TRUE
is_strict_clock_model(clock_models[[2]])
#> [1] TRUE

check_empty_beautier_folder()
```
