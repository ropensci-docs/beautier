# Determine if two screenlogs are equal.

Will [stop](https://rdrr.io/r/base/stop.html) if the arguments are not
screenlogs.

## Usage

``` r
are_equal_screenlogs(screenlog_1, screenlog_2)
```

## Arguments

- screenlog_1:

  an screenlog, as created by
  [create_screenlog](https://docs.ropensci.org/beautier/reference/create_screenlog.md)

- screenlog_2:

  an screenlog, as created by
  [create_screenlog](https://docs.ropensci.org/beautier/reference/create_screenlog.md)

## Value

TRUE if the two screenlogs are equal

## See also

Use
[create_screenlog](https://docs.ropensci.org/beautier/reference/create_screenlog.md)
to create an screenlog

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
check_empty_beautier_folder()

screenlog_1 <- create_screenlog(log_every = 1000)
screenlog_2 <- create_screenlog(log_every = 314)
# TRUE
are_equal_screenlogs(screenlog_1, screenlog_1)
#> [1] TRUE
# FALSE
are_equal_screenlogs(screenlog_1, screenlog_2)
#> [1] FALSE

check_empty_beautier_folder()
```
