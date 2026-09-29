# Determine if x consists out of IDs

Determine if x consists out of IDs

## Usage

``` r
are_ids(x)
```

## Arguments

- x:

  the object to check if it consists out of IDs

## Value

TRUE if x, or all elements of x, are IDs

## See also

to check one ID, use
[is_id](https://docs.ropensci.org/beautier/reference/is_id.md)

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
check_empty_beautier_folder()

# TRUE
are_ids("anthus_aco")
#> [1] TRUE
are_ids(c("anthus_aco", "anthus_nd2"))
#> [1] TRUE
are_ids(list("anthus_aco", "anthus_nd2"))
#> [1] TRUE
are_ids(c(1, 2))
#> [1] TRUE
are_ids(1)
#> [1] TRUE

# FALSE
are_ids(NULL)
#> [1] FALSE
are_ids(NA)
#> [1] FALSE
are_ids(c())
#> [1] FALSE
are_ids(ape::rcoal(3))
#> [1] FALSE
are_ids(c(ape::rcoal(3), ape::rcoal(4)))
#> [1] FALSE

check_empty_beautier_folder()
```
