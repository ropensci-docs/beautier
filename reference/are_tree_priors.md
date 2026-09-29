# Determine if x consists out of tree_priors objects

Determine if x consists out of tree_priors objects

## Usage

``` r
are_tree_priors(x)
```

## Arguments

- x:

  the object to check if it consists out of tree_priors objects

## Value

TRUE if x, or all elements of x, are tree_prior objects

## See also

Use
[create_yule_tree_prior](https://docs.ropensci.org/beautier/reference/create_yule_tree_prior.md)
to create a Yule tree prior

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
check_empty_beautier_folder()

yule_tree_prior <- create_yule_tree_prior()
bd_tree_prior <- create_bd_tree_prior()
both_tree_priors <- list(yule_tree_prior, bd_tree_prior)
# TRUE
are_tree_priors(yule_tree_prior)
#> [1] TRUE
# TRUE
are_tree_priors(bd_tree_prior)
#> [1] TRUE
# TRUE
are_tree_priors(both_tree_priors)
#> [1] TRUE

check_empty_beautier_folder()
```
