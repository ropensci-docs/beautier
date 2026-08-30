# Get the number of parameters a list of tree priors has

Get the number of parameters a list of tree priors has

## Usage

``` r
get_tree_priors_n_params(tree_priors)
```

## Arguments

- tree_priors:

  one or more tree priors, as returned by
  [`create_tree_prior`](https://docs.ropensci.org/beautier/reference/create_tree_prior.md)

## Value

the number of parameters the tree priors have

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
check_empty_beautier_folder()

# Two
get_tree_priors_n_params(
  list(
    create_bd_tree_prior(), # zero
    create_cep_tree_prior() # two
  )
)
#> [1] 2

check_empty_beautier_folder()
```
