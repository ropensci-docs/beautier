# Determine if the object is a valid coalescent exponential population tree prior

Determine if the object is a valid coalescent exponential population
tree prior

## Usage

``` r
is_cep_tree_prior(x)
```

## Arguments

- x:

  an object, to be determined if it is a valid constant coalescent
  exponential population tree prior

## Value

TRUE if x is a valid coalescent exponential population tree prior, FALSE
otherwise

## See also

Use
[`create_cep_tree_prior`](https://docs.ropensci.org/beautier/reference/create_cep_tree_prior.md)
to create a valid coalescent exponential population tree prior

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
check_empty_beautier_folder()

  !beautier::is_cep_tree_prior(create_bd_tree_prior())
#> [1] TRUE
  !beautier::is_cep_tree_prior(create_cbs_tree_prior())
#> [1] TRUE
  !beautier::is_cep_tree_prior(create_ccp_tree_prior())
#> [1] TRUE
  is_cep_tree_prior(create_cep_tree_prior())
#> [1] TRUE
  !beautier::is_cep_tree_prior(create_yule_tree_prior())
#> [1] TRUE

check_empty_beautier_folder()
```
