# Determine if the object is a valid ID

Determine if the object is a valid ID

## Usage

``` r
is_id(x)
```

## Arguments

- x:

  an object, to be determined if it is a valid ID

## Value

TRUE if x is a valid ID, FALSE otherwise

## See also

to check multiple IDs, use
[are_ids](https://docs.ropensci.org/beautier/reference/are_ids.md)

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
check_empty_beautier_folder()

# TRUE
is_id("anthus_aco")
#> [1] TRUE
is_id(3)
#> [1] TRUE

# FALSE
is_id(ape::rcoal(3))
#> [1] FALSE
is_id(NULL)
#> [1] FALSE
is_id(NA)
#> [1] FALSE

check_empty_beautier_folder()
```
