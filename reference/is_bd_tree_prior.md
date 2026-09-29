# Determine if the object is a valid Birth Death tree prior

Determine if the object is a valid Birth Death tree prior

## Usage

``` r
is_bd_tree_prior(x)
```

## Arguments

- x:

  an object, to be determined if it is a valid birth death tree prior

## Value

TRUE if x is a valid birth death tree prior, FALSE otherwise

## See also

Use
[`create_bd_tree_prior`](https://docs.ropensci.org/beautier/reference/create_bd_tree_prior.md)
to create a valid Birth-Death tree prior

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
check_empty_beautier_folder()

  is_bd_tree_prior(create_bd_tree_prior())
#> [1] TRUE
  !is_bd_tree_prior(create_cbs_tree_prior())
#> [1] TRUE
  !is_bd_tree_prior(create_ccp_tree_prior())
#> [1] TRUE
  !is_bd_tree_prior(create_cep_tree_prior())
#> [1] TRUE
  !is_bd_tree_prior(create_yule_tree_prior())
#> [1] TRUE

check_empty_beautier_folder()
```
