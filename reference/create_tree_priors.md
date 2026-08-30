# Creates all supported tree priors, which is a list of the types returned by [`create_bd_tree_prior`](https://docs.ropensci.org/beautier/reference/create_bd_tree_prior.md), [`create_cbs_tree_prior`](https://docs.ropensci.org/beautier/reference/create_cbs_tree_prior.md), [`create_ccp_tree_prior`](https://docs.ropensci.org/beautier/reference/create_ccp_tree_prior.md), [`create_cep_tree_prior`](https://docs.ropensci.org/beautier/reference/create_cep_tree_prior.md) and [`create_yule_tree_prior`](https://docs.ropensci.org/beautier/reference/create_yule_tree_prior.md)

Creates all supported tree priors, which is a list of the types returned
by
[`create_bd_tree_prior`](https://docs.ropensci.org/beautier/reference/create_bd_tree_prior.md),
[`create_cbs_tree_prior`](https://docs.ropensci.org/beautier/reference/create_cbs_tree_prior.md),
[`create_ccp_tree_prior`](https://docs.ropensci.org/beautier/reference/create_ccp_tree_prior.md),
[`create_cep_tree_prior`](https://docs.ropensci.org/beautier/reference/create_cep_tree_prior.md)
and
[`create_yule_tree_prior`](https://docs.ropensci.org/beautier/reference/create_yule_tree_prior.md)

## Usage

``` r
create_tree_priors()
```

## Value

a list of tree_priors

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
check_empty_beautier_folder()

tree_priors <- create_tree_priors()
# TRUE
is_bd_tree_prior(tree_priors[[1]])
#> [1] TRUE
is_cbs_tree_prior(tree_priors[[2]])
#> [1] TRUE
is_ccp_tree_prior(tree_priors[[3]])
#> [1] TRUE
is_cep_tree_prior(tree_priors[[4]])
#> [1] TRUE
is_yule_tree_prior(tree_priors[[5]])
#> [1] TRUE

check_empty_beautier_folder()
```
