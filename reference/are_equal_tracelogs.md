# Determine if two tracelogs are equal.

Will [stop](https://rdrr.io/r/base/stop.html) if the arguments are not
tracelogs.

## Usage

``` r
are_equal_tracelogs(tracelog_1, tracelog_2)
```

## Arguments

- tracelog_1:

  an tracelog, as created by
  [create_tracelog](https://docs.ropensci.org/beautier/reference/create_tracelog.md)

- tracelog_2:

  an tracelog, as created by
  [create_tracelog](https://docs.ropensci.org/beautier/reference/create_tracelog.md)

## Value

TRUE if the two tracelogs are equal

## See also

Use
[create_tracelog](https://docs.ropensci.org/beautier/reference/create_tracelog.md)
to create an tracelog

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
check_empty_beautier_folder()

tracelog_1 <- create_tracelog(log_every = 1000)
tracelog_2 <- create_tracelog(log_every = 314)
# TRUE
are_equal_tracelogs(tracelog_1, tracelog_1)
#> [1] TRUE
# FALSE
are_equal_tracelogs(tracelog_1, tracelog_2)
#> [1] FALSE

check_empty_beautier_folder()
```
