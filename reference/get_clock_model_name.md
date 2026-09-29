# Get the BEAUti name for a clock model

Will [stop](https://rdrr.io/r/base/stop.html) if the clock model is an
invalid clock model

## Usage

``` r
get_clock_model_name(clock_model)
```

## Arguments

- clock_model:

  a clock model, as returned by
  [`create_clock_model`](https://docs.ropensci.org/beautier/reference/create_clock_model.md)

## Value

name of the clock model

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
check_empty_beautier_folder()

# StrictClock
get_clock_model_name(create_strict_clock_model())
#> [1] "StrictClock"

# RelaxedClock
get_clock_model_name(create_rln_clock_model())
#> [1] "RelaxedClock"

check_empty_beautier_folder()
```
