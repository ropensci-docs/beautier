# Check if the clock model is a valid clock model.

Calls `stop` if the clock model is invalid

## Usage

``` r
check_rln_clock_model(clock_model)
```

## Arguments

- clock_model:

  a clock model, as returned by
  [`create_clock_model`](https://docs.ropensci.org/beautier/reference/create_clock_model.md)

## Value

TRUE if `clock_model` is a valid clock model

## See also

Use
[create_clock_model](https://docs.ropensci.org/beautier/reference/create_clock_model.md)
to create a valid clock model

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
check_empty_beautier_folder()

check_rln_clock_model(create_rln_clock_model())

check_empty_beautier_folder()
```
