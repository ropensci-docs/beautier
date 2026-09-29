# Check if the object is a list of one or more clock models.

Will [stop](https://rdrr.io/r/base/stop.html) if the object is not a
list of one or more clock models.

## Usage

``` r
check_clock_models(clock_models)
```

## Arguments

- clock_models:

  the object to be checked if it is a list of one or more valid clock
  models

## Value

nothing. Will [stop](https://rdrr.io/r/base/stop.html) if the object is
not a list of one or more clock models.

## See also

Use
[create_clock_model](https://docs.ropensci.org/beautier/reference/create_clock_model.md)
to create a valid clock model

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
check_empty_beautier_folder()

check_clock_models(create_strict_clock_model())
check_clock_models(list(create_strict_clock_model()))
check_clock_models(
  list(create_strict_clock_model(), create_rln_clock_model())
)

check_empty_beautier_folder()
```
