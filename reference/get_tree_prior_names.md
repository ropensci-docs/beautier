# Get the tree prior names

Get the tree prior names

## Usage

``` r
get_tree_prior_names()
```

## Value

the tree prior names

## See also

Use
[create_tree_priors](https://docs.ropensci.org/beautier/reference/create_tree_priors.md)
to get all tree priors

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
check_empty_beautier_folder()

get_tree_prior_names()
#> [1] "birth_death"                    "coalescent_bayesian_skyline"   
#> [3] "coalescent_constant_population" "coalescent_exp_population"     
#> [5] "yule"                          

check_empty_beautier_folder()
```
