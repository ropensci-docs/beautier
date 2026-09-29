# Determine if the object is a valid constant coalescent Bayesian skyline prior

Determine if the object is a valid constant coalescent Bayesian skyline
prior

## Usage

``` r
is_cbs_tree_prior(x)
```

## Arguments

- x:

  an object, to be determined if it is a valid constant coalescent
  Bayesian skyline prior

## Value

\`TRUE\` if \`x\` is a valid constant coalescent Bayesian skyline prior,
\`FALSE\` otherwise

## See also

Use
[`create_cbs_tree_prior`](https://docs.ropensci.org/beautier/reference/create_cbs_tree_prior.md)
to create a valid coalescent Bayes skyline tree prior

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
check_empty_beautier_folder()

# TRUE
is_cbs_tree_prior(create_cbs_tree_prior())
#> [1] TRUE

# FALSE
is_cbs_tree_prior(create_bd_tree_prior())
#> [1] FALSE
is_cbs_tree_prior(create_ccp_tree_prior())
#> [1] FALSE
is_cbs_tree_prior(create_cep_tree_prior())
#> [1] FALSE
is_cbs_tree_prior(create_yule_tree_prior())
#> [1] FALSE

check_empty_beautier_folder()
```
