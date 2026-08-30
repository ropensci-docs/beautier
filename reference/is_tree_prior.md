# Determine if an object is a valid tree prior

Determine if an object is a valid tree prior

## Usage

``` r
is_tree_prior(x)
```

## Arguments

- x:

  an object

## Value

TRUE if x is a valid tree_prior, FALSE otherwise

## See also

tree priors can be created by
[`create_tree_prior`](https://docs.ropensci.org/beautier/reference/create_tree_prior.md)

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
check_empty_beautier_folder()

# TRUE
is_tree_prior(create_bd_tree_prior())
#> [1] TRUE
is_tree_prior(create_yule_tree_prior())
#> [1] TRUE

# FALSE
is_tree_prior("nonsense")
#> [1] FALSE

check_empty_beautier_folder()
```
