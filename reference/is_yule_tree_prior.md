# Determine if the object is a valid Yule tree prior,

Determine if the object is a valid Yule tree prior,

## Usage

``` r
is_yule_tree_prior(x)
```

## Arguments

- x:

  an object, to be determined if it is a valid Yule tree prior

## Value

TRUE if x is a valid Yule tree prior, FALSE otherwise

## See also

Use
[`create_yule_tree_prior`](https://docs.ropensci.org/beautier/reference/create_yule_tree_prior.md)
to create a valid Yule tree prior

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
check_empty_beautier_folder()

# TRUE
is_yule_tree_prior(create_yule_tree_prior())
#> [1] TRUE

# FALSE
is_yule_tree_prior(create_bd_tree_prior())
#> [1] FALSE
is_yule_tree_prior(create_cbs_tree_prior())
#> [1] FALSE
is_yule_tree_prior(create_ccp_tree_prior())
#> [1] FALSE
is_yule_tree_prior(create_cep_tree_prior())
#> [1] FALSE

check_empty_beautier_folder()
```
