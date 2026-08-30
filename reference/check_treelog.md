# Check if a `treelog` is valid.

Will call [stop](https://rdrr.io/r/base/stop.html) if not.

## Usage

``` r
check_treelog(treelog)
```

## Arguments

- treelog:

  a `treelog`, as created by
  [create_treelog](https://docs.ropensci.org/beautier/reference/create_treelog.md)

## Value

No return value, called for side effects

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
check_empty_beautier_folder()

check_treelog(create_test_treelog())

check_empty_beautier_folder()
```
