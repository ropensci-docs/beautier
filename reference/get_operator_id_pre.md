# Get the prefix of operator IDs

Get the prefix of operator IDs

## Usage

``` r
get_operator_id_pre(tree_prior)
```

## Arguments

- tree_prior:

  a tree priors, as returned by
  [`create_tree_prior`](https://docs.ropensci.org/beautier/reference/create_tree_prior.md)

## Value

the prefix of operator IDs, similar to the name of a tree prior

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
check_empty_beautier_folder()

# BirthDeath
get_operator_id_pre(
  tree_prior = create_bd_tree_prior()
)
#> [1] "BirthDeath"

check_empty_beautier_folder()
```
