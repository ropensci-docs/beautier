# Check if a `screenlog` is valid.

Will call [stop](https://rdrr.io/r/base/stop.html) if not.

## Usage

``` r
check_screenlog(screenlog)
```

## Arguments

- screenlog:

  a `screenlog`, as created by
  [create_screenlog](https://docs.ropensci.org/beautier/reference/create_screenlog.md)

## Value

No return value, called for side effects

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
check_empty_beautier_folder()

check_screenlog(create_test_screenlog())

check_empty_beautier_folder()
```
