# Determine if the object is a valid constant coalescence population tree prior

Determine if the object is a valid constant coalescence population tree
prior

## Usage

``` r
is_ccp_tree_prior(x)
```

## Arguments

- x:

  an object, to be determined if it is a valid constant coalescence
  population tree prior

## Value

TRUE if x is a valid constant coalescence population tree prior, FALSE
otherwise

## See also

Use
[`create_ccp_tree_prior`](https://docs.ropensci.org/beautier/reference/create_ccp_tree_prior.md)
to create a valid constant coalescence population tree prior

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
check_empty_beautier_folder()
  !is_ccp_tree_prior(create_bd_tree_prior())
#> [1] TRUE
  !is_ccp_tree_prior(create_cbs_tree_prior())
#> [1] TRUE
  is_ccp_tree_prior(create_ccp_tree_prior())
#> [1] TRUE
  !is_ccp_tree_prior(create_cep_tree_prior())
#> [1] TRUE
  !is_ccp_tree_prior(create_yule_tree_prior())
#> [1] TRUE
check_empty_beautier_folder()
```
