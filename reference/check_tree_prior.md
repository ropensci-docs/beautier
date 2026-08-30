# Check if the tree prior is a valid tree prior

Calls `stop` if the tree priors are invalid

## Usage

``` r
check_tree_prior(tree_prior)
```

## Arguments

- tree_prior:

  a tree priors, as returned by
  [`create_tree_prior`](https://docs.ropensci.org/beautier/reference/create_tree_prior.md)

## Value

nothing

## See also

Use
[create_tree_prior](https://docs.ropensci.org/beautier/reference/create_tree_prior.md)
to create a valid tree prior

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
check_empty_beautier_folder()

check_tree_prior(create_yule_tree_prior())
#> NULL
check_tree_prior(create_bd_tree_prior())
#> NULL
check_tree_prior(create_cbs_tree_prior())
#> NULL
check_tree_prior(create_ccp_tree_prior())
#> NULL
check_tree_prior(create_cep_tree_prior())
#> NULL

# Can use list of one tree prior
check_tree_prior(list(create_yule_tree_prior()))
#> NULL

check_empty_beautier_folder()
```
