# Get the number of parameters a tree prior has

Get the number of parameters a tree prior has

## Usage

``` r
get_tree_prior_n_params(tree_prior)
```

## Arguments

- tree_prior:

  a tree_prior, as created by
  [`create_tree_prior`](https://docs.ropensci.org/beautier/reference/create_tree_prior.md)

## Value

the number of parameters a tree prior has

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
check_empty_beautier_folder()

# birth_rate_distr is uniform, which has zero parameters
# death_rate_distr is uniform, which has zero parameters
get_tree_prior_n_params(create_bd_tree_prior())
#> [1] 0

# no distributions, no parameters
get_tree_prior_n_params(create_cbs_tree_prior())
#> [1] 0

# pop_size_distr is 1/x, which has zero parameters
get_tree_prior_n_params(create_ccp_tree_prior())
#> [1] 0

# pop_size_distr is 1/x, which has zero parameters
# growth_rate_distr is Laplace, which has two parameters
get_tree_prior_n_params(create_cep_tree_prior())
#> [1] 2

# birth_rate_distr is uniform, which has zero parameters
get_tree_prior_n_params(create_yule_tree_prior())
#> [1] 0

check_empty_beautier_folder()
```
