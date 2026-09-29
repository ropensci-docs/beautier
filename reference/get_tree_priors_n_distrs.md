# Get the number of distributions a tree prior has

Get the number of distributions a tree prior has

## Usage

``` r
get_tree_priors_n_distrs(tree_priors)
```

## Arguments

- tree_priors:

  one or more tree priors, as returned by
  [`create_tree_prior`](https://docs.ropensci.org/beautier/reference/create_tree_prior.md)

## Value

the number of distributions a tree prior has

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
check_empty_beautier_folder()

# Three distrubutions
get_tree_priors_n_distrs(
  list(
    create_bd_tree_prior(), # has two distributions
    create_ccp_tree_prior() # has one distribution
  )
)
#> [1] 3

check_empty_beautier_folder()
```
