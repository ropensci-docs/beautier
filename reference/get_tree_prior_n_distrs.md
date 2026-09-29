# Get the number of distributions a tree prior has

Get the number of distributions a tree prior has

## Usage

``` r
get_tree_prior_n_distrs(tree_prior)
```

## Arguments

- tree_prior:

  a tree priors, as returned by
  [`create_tree_prior`](https://docs.ropensci.org/beautier/reference/create_tree_prior.md)

## Value

the number of distributions a tree prior has

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
check_empty_beautier_folder()

# 2: birth_rate_distr and death_rate_distr
get_tree_prior_n_distrs(create_bd_tree_prior())
#> [1] 2

# 0:none
get_tree_prior_n_distrs(create_cbs_tree_prior())
#> [1] 0

# 1: pop_size_distr
get_tree_prior_n_distrs(create_ccp_tree_prior())
#> [1] 1

 # 2:pop_size_distr and growth_rate_distr
get_tree_prior_n_distrs(create_cep_tree_prior())
#> [1] 2

# 1: birth_rate_distr
get_tree_prior_n_distrs(create_yule_tree_prior())
#> [1] 1

check_empty_beautier_folder()
```
