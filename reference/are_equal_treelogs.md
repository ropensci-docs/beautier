# Determine if two treelogs are equal.

Will [stop](https://rdrr.io/r/base/stop.html) if the arguments are not
treelogs.

## Usage

``` r
are_equal_treelogs(treelog_1, treelog_2)
```

## Arguments

- treelog_1:

  an treelog, as created by
  [create_treelog](https://docs.ropensci.org/beautier/reference/create_treelog.md)

- treelog_2:

  an treelog, as created by
  [create_treelog](https://docs.ropensci.org/beautier/reference/create_treelog.md)

## Value

TRUE if the two treelogs are equal

## See also

Use
[create_treelog](https://docs.ropensci.org/beautier/reference/create_treelog.md)
to create an treelog

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
check_empty_beautier_folder()

treelog_1 <- create_treelog(log_every = 1000)
treelog_2 <- create_treelog(log_every = 314)
# TRUE
are_equal_treelogs(treelog_1, treelog_1)
#> [1] TRUE
# FALSE
are_equal_treelogs(treelog_1, treelog_2)
#> [1] FALSE

check_empty_beautier_folder()
```
